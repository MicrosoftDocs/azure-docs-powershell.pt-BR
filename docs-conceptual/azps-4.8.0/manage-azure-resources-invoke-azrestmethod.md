---
title: Gerenciar recursos do Azure com Invoke-AzRestMethod
description: Como usar o Azure PowerShell para gerenciar recursos com o cmdlet Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 55d7cc06178257a9288e2d27f810d1180369ddc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001645"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Gerenciar recursos do Azure com Invoke-AzRestMethod

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) é um cmdlet do Azure PowerShell que foi introduzido no módulo Az do PowerShell versão 4.4.0. Ele permite que você faça solicitações HTTP personalizadas para o ponto de extremidade do ARM (Gerenciamento de Recursos do Azure) usando o contexto Az.

Esse cmdlet é útil quando você deseja gerenciar os serviços do Azure para recursos que ainda não estão disponíveis no módulo Az do PowerShell.

## <a name="how-to-use-invoke-azrestmethod"></a>Como usar Invoke-AzRestMethod

Por exemplo, você pode permitir o acesso ao ACR (Registro de Contêiner do Azure) somente para redes específicas ou negar o acesso público. A partir da versão 4.5.0 do módulo Az PowerShell, esse recurso ainda não está disponível no [módulo Az.ContainerRegistry do PowerShell](/powershell/module/Az.ContainerRegistry/). No entanto, ele pode ser gerenciado, enquanto isso, com `Invoke-AzRestMethod`.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>Usar Invoke-AzRestMethod com operações GET

O seguinte exemplo demonstra como usar o cmdlet `Invoke-AzRestMethod` com uma operação GET:

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

Para permitir a máxima flexibilidade, a maioria dos parâmetros para `Invoke-AzRestMethod` é opcional.
No entanto, quando você estiver gerenciando recursos em um grupo de recursos, provavelmente você precisará fornecer a ID completa para o recurso ou parâmetros como o grupo de recursos, o provedor de recursos e o tipo de recurso.

Os parâmetros `ResourceType` e `Name` podem receber vários valores ao direcionar recursos que exigem mais de um nome. Por exemplo, para manipular uma pesquisa salva em um workspace do Log Analytics, os parâmetros são semelhantes ao seguinte exemplo: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.

Usando um mapeamento com base na posição na matriz, o cmdlet constrói o seguinte recurso: `Id:'/workspaces/my-la/savedsearches/my-search'`.

O parâmetro `APIVersion` permite que você use uma versão de API específica, incluindo versões prévias. As versões de API com suporte para provedores de recursos do Azure podem ser encontradas no repositório GitHub [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).

Você pode encontrar a definição para a versão 2019-12-01-preview do ACR no seguinte local: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>Usar Invoke-AzRestMethod com operações PATCH

Desabilite o acesso público ao ACR existente chamado `myacr` no grupo de recursos `myresourcegroup` usando o cmdlet `Invoke-AzRestMethod`.

Para desabilitar o acesso à rede pública, você precisa fazer uma chamada **PATCH** à API que altera o valor do parâmetro `publicNetwokAccess`, conforme mostrado no seguinte exemplo:

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

A propriedade `Payload` é uma cadeia de caracteres JSON que mostra o caminho da propriedade a ser modificada.

Todos os parâmetros dessa API são descritos no arquivo **rest-api-spec** associado a essa API.
A definição específica do parâmetro publicNetworkAccess pode ser encontrada no [arquivo JSON de registro de contêiner](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) para a versão 2019-12-01-preview da API.

Para permitir o acesso somente ao registro de um endereço IP específico, o conteúdo precisa ser modificado, conforme mostrado no seguinte exemplo:

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Comparação com Get-AzResource, New-AzResource e Remove-AzResource

Os cmdlets `*-AzResource` permitem que você personalize a chamada à API REST para o Azure especificando o tipo de recurso, a versão da API e as propriedades a serem atualizadas. No entanto, as propriedades precisam ser criadas primeiro como um `PSObject`. Esse processo adiciona um nível extra de complexidade e pode facilmente se tornar complicado.

`Invoke-AzRestMethod` oferece uma forma mais simples de gerenciar os recursos do Azure. Conforme mostrado no exemplo anterior, você pode criar uma cadeia de caracteres JSON e usá-la para personalizar a chamada à API REST sem precisar criar nenhum `PSObjects`.

Se você já conhece os cmdlets `*-AzResource`, pode continuar usando-os. Não temos planos para interromper o suporte a eles. Com `Invoke-AzRestMethod`, adicionamos um novo cmdlet ao kit de ferramentas.

## <a name="see-also"></a>Consulte Também

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
