---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785712"
---
# Get-AzureRmExpressRouteServiceProvider

## Sinopse
Obtém uma lista de provedores de serviços do ExpressRoute e seus atributos.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmExpressRouteServiceProvider** recupera uma lista de provedores de serviços do ExpressRoute e seus atributos. Inclua as opções de localização e largura de banda.

## EXEMPLOS

### Exemplo 1: obter uma lista de provedores de serviços com locais em "vale do silício"
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
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

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmExpressRouteCircuitARPTable](Get-AzureRmExpressRouteCircuitARPTable.md)

[Get-AzureRmExpressRouteCircuitRouteTable](Get-AzureRmExpressRouteCircuitRouteTable.md)

[Get-AzureRmExpressRouteCircuitRouteTableSummary](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[Get-AzureRmExpressRouteCircuitStats](Get-AzureRmExpressRouteCircuitStats.md)
