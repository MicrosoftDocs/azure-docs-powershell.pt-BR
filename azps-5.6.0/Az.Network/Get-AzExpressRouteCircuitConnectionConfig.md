---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c8d35373c2891b9f0d3ac76ded8b4e9808f32f33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890782"
---
# Get-AzExpressRouteCircuitConnectionConfig

## SYNOPSIS
Obtém uma configuração de conexão de circuito ExpressRoute associada ao Peering Privado do ExpressRouteCircuit.

## SINTAXE

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzExpressRouteCircuitConnectionConfig** recupera a configuração de uma conexão de circuito associada ao Private Peering para um circuito ExpressRoute.

## EXEMPLOS

### Exemplo 1: Exibir a configuração de conexão de circuito para um circuito ExpressRoute
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### Exemplo 2: Obter recurso de conexão de circuito associado a um Circuito ExpressRoute usando a canalização
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -ExpressRouteCircuit
O objeto de circuito ExpressRoute que contém a configuração de conexão de circuito.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
O nome da configuração de conexão do circuito a ser recuperado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection

## NOTES

## LINKS RELACIONADOS

[Get-AzExpressRouteCircuit](Get-AzExpressRouteCircuit.md)

[Add-AzExpressRouteCircuitConnectionConfig](Add-AzExpressRouteCircuitConnectionConfig.md)

[Remove-AzExpressRouteCircuitConnectionConfig](Remove-AzExpressRouteCircuitConnectionConfig.md)

[Set-AzExpressRouteCircuitConnectionConfig](Set-AzExpressRouteCircuitConnectionConfig.md)

[New-AzExpressRouteCircuitConnectionConfig](New-AzExpressRouteCircuitConnectionConfig.md)