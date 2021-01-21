---
title: Gerenciar recursos do Azure com Invoke-AzRestMethod
description: Como usar o Azure PowerShell para gerenciar recursos com o cmdlet Invoke-AzRestMethod.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5fdb8543630198d141d42626dc3a8b85f0bcdaa7
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573459"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="eccb8-103">Gerenciar recursos do Azure com Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="eccb8-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="eccb8-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) é um cmdlet do Azure PowerShell que foi introduzido no módulo Az do PowerShell versão 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="eccb8-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="eccb8-105">Ele permite que você faça solicitações HTTP personalizadas para o ponto de extremidade do ARM (Gerenciamento de Recursos do Azure) usando o contexto Az.</span><span class="sxs-lookup"><span data-stu-id="eccb8-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="eccb8-106">Esse cmdlet é útil quando você deseja gerenciar os serviços do Azure para recursos que ainda não estão disponíveis no módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eccb8-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="eccb8-107">Como usar Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="eccb8-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="eccb8-108">Por exemplo, você pode permitir o acesso ao ACR (Registro de Contêiner do Azure) somente para redes específicas ou negar o acesso público.</span><span class="sxs-lookup"><span data-stu-id="eccb8-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="eccb8-109">A partir da versão 4.5.0 do módulo Az PowerShell, esse recurso ainda não está disponível no [módulo Az.ContainerRegistry do PowerShell](/powershell/module/Az.ContainerRegistry/).</span><span class="sxs-lookup"><span data-stu-id="eccb8-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="eccb8-110">No entanto, ele pode ser gerenciado, enquanto isso, com `Invoke-AzRestMethod`.</span><span class="sxs-lookup"><span data-stu-id="eccb8-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="eccb8-111">Usar Invoke-AzRestMethod com operações GET</span><span class="sxs-lookup"><span data-stu-id="eccb8-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="eccb8-112">O seguinte exemplo demonstra como usar o cmdlet `Invoke-AzRestMethod` com uma operação GET:</span><span class="sxs-lookup"><span data-stu-id="eccb8-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

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

<span data-ttu-id="eccb8-113">Para permitir a máxima flexibilidade, a maioria dos parâmetros para `Invoke-AzRestMethod` é opcional.</span><span class="sxs-lookup"><span data-stu-id="eccb8-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="eccb8-114">No entanto, quando você estiver gerenciando recursos em um grupo de recursos, provavelmente você precisará fornecer a ID completa para o recurso ou parâmetros como o grupo de recursos, o provedor de recursos e o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="eccb8-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="eccb8-115">Os parâmetros `ResourceType` e `Name` podem receber vários valores ao direcionar recursos que exigem mais de um nome.</span><span class="sxs-lookup"><span data-stu-id="eccb8-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="eccb8-116">Por exemplo, para manipular uma pesquisa salva em um workspace do Log Analytics, os parâmetros são semelhantes ao seguinte exemplo: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span><span class="sxs-lookup"><span data-stu-id="eccb8-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="eccb8-117">Usando um mapeamento com base na posição na matriz, o cmdlet constrói o seguinte recurso: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span><span class="sxs-lookup"><span data-stu-id="eccb8-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="eccb8-118">O parâmetro `APIVersion` permite que você use uma versão de API específica, incluindo versões prévias.</span><span class="sxs-lookup"><span data-stu-id="eccb8-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="eccb8-119">As versões de API com suporte para provedores de recursos do Azure podem ser encontradas no repositório GitHub [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).</span><span class="sxs-lookup"><span data-stu-id="eccb8-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="eccb8-120">Você pode encontrar a definição para a versão 2019-12-01-preview do ACR no seguinte local: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span><span class="sxs-lookup"><span data-stu-id="eccb8-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="eccb8-121">Usar Invoke-AzRestMethod com operações PATCH</span><span class="sxs-lookup"><span data-stu-id="eccb8-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="eccb8-122">Desabilite o acesso público ao ACR existente chamado `myacr` no grupo de recursos `myresourcegroup` usando o cmdlet `Invoke-AzRestMethod`.</span><span class="sxs-lookup"><span data-stu-id="eccb8-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="eccb8-123">Para desabilitar o acesso à rede pública, você precisa fazer uma chamada **PATCH** à API que altera o valor do parâmetro `publicNetwokAccess`, conforme mostrado no seguinte exemplo:</span><span class="sxs-lookup"><span data-stu-id="eccb8-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

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

<span data-ttu-id="eccb8-124">A propriedade `Payload` é uma cadeia de caracteres JSON que mostra o caminho da propriedade a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="eccb8-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="eccb8-125">Todos os parâmetros dessa API são descritos no arquivo **rest-api-spec** associado a essa API.</span><span class="sxs-lookup"><span data-stu-id="eccb8-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="eccb8-126">A definição específica do parâmetro publicNetworkAccess pode ser encontrada no [arquivo JSON de registro de contêiner](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) para a versão 2019-12-01-preview da API.</span><span class="sxs-lookup"><span data-stu-id="eccb8-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="eccb8-127">Para permitir o acesso somente ao registro de um endereço IP específico, o conteúdo precisa ser modificado, conforme mostrado no seguinte exemplo:</span><span class="sxs-lookup"><span data-stu-id="eccb8-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

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

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="eccb8-128">Comparação com Get-AzResource, New-AzResource e Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="eccb8-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="eccb8-129">Os cmdlets `*-AzResource` permitem que você personalize a chamada à API REST para o Azure especificando o tipo de recurso, a versão da API e as propriedades a serem atualizadas.</span><span class="sxs-lookup"><span data-stu-id="eccb8-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="eccb8-130">No entanto, as propriedades precisam ser criadas primeiro como um `PSObject`.</span><span class="sxs-lookup"><span data-stu-id="eccb8-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="eccb8-131">Esse processo adiciona um nível extra de complexidade e pode facilmente se tornar complicado.</span><span class="sxs-lookup"><span data-stu-id="eccb8-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="eccb8-132">`Invoke-AzRestMethod` oferece uma forma mais simples de gerenciar os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="eccb8-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="eccb8-133">Conforme mostrado no exemplo anterior, você pode criar uma cadeia de caracteres JSON e usá-la para personalizar a chamada à API REST sem precisar criar nenhum `PSObjects`.</span><span class="sxs-lookup"><span data-stu-id="eccb8-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="eccb8-134">Se você já conhece os cmdlets `*-AzResource`, pode continuar usando-os.</span><span class="sxs-lookup"><span data-stu-id="eccb8-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="eccb8-135">Não temos planos para interromper o suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="eccb8-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="eccb8-136">Com `Invoke-AzRestMethod`, adicionamos um novo cmdlet ao kit de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="eccb8-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="eccb8-137">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="eccb8-137">See Also</span></span>

* [<span data-ttu-id="eccb8-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="eccb8-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="eccb8-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="eccb8-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="eccb8-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="eccb8-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
