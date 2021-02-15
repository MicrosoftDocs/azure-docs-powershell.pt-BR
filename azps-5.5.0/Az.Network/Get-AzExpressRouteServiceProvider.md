---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115189"
---
# Get-AzExpressRouteServiceProvider

## Sinopse
Obtém uma lista de provedores de serviços do ExpressRoute e seus atributos.

## Sintaxe

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzExpressRouteServiceProvider** recupera uma lista de provedores de serviços do ExpressRoute e seus atributos. O atributo inclui opções de localização e largura de banda.

## Exemplos

### Exemplo 1: Obter uma lista de provedor de serviços com locais no "Vale do Silício"
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider

## Notas

## LINKS RELACIONADOS

[Tabela Get-AzExpressRoute CircuitARPTable](Get-AzExpressRouteCircuitARPTable.md)

[Get-AzExpressRoute CircuitRouteTable](Get-AzExpressRouteCircuitRouteTable.md)

[Get-AzExpressRoute CircuitRouteTableSummary](Get-AzExpressRouteCircuitRouteTableSummary.md)

[Get-AzExpressRoute CircuitStat](./Get-AzExpressRouteCircuitStat.md)
