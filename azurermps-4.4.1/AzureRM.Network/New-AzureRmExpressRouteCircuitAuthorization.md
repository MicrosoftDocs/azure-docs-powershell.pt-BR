---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2fec428adb2ba8621d09a1f0ae5e762cdbe4b913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609985"
---
# New-AzureRmExpressRouteCircuitAuthorization

## Sinopse
Cria uma autorização de circuito do ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmExpressRouteCircuitAuthorization** cria uma autorização de circuito que pode ser adicionada a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar uma rede ao circuito. Só pode haver uma autorização por rede virtual.

Depois de criar um circuito do ExpressRoute, você pode usar **Add-AzureRmExpressRouteCircuitAuthorization** para adicionar uma autorização para esse circuito.
Você também pode usar **New-AzureRmExpressRouteCircuitAuthorization** para criar uma autorização que pode ser adicionada a um novo circuito ao mesmo tempo em que o circuito é criado.

## EXEMPLOS

### Exemplo 1: criar uma nova autorização de circuito
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Esse comando cria uma nova autorização de circuito chamada ContosoCircuitAuthorization e, em seguida, armazena esse objeto em uma variável chamada $Authorization. Salvar o objeto em uma variável é importante: embora **New-AzureRmExpressRouteCircuitAuthorization** possa criar uma autorização de circuito, ele não pode adicionar essa autorização a uma rota de circuito. Em vez disso, o $Authorization variável é usado New-AzureRmExpressRouteCircuit durante a criação de um circuito do ExpressRoute com nova marca.

Para obter mais informações, consulte a documentação do cmdlet New-AzureRmExpressRouteCircuit.

## OS

### -Nome
Especifica um nome exclusivo para a nova autorização de circuito do ExpressRoute.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita entrada em pipeline.

## EXIBE

### PSExpressRouteCircuitAuthorization
Esse cmdlet cria instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

