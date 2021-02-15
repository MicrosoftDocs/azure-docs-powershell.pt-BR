---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112903"
---
# Get-AzExpressRouteCircuitAuthorization

## Sinopse
Obtém informações sobre as autorizações de circuito do ExpressRoute.

## Sintaxe

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzExpressRoute CircuitAuthorization** obtém informações sobre as autorizações atribuídas a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual). As chaves de autorização, bem como outras informações sobre a autorização, podem ser visualizadas a qualquer momento executando **Get-AzExpressRoute CircuitAuthorization.**

## Exemplos

### Exemplo 1: Obter todas as autorizações do ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Esses comandos retornam informações sobre todas as autorizações do ExpressRoute associadas a um circuito do ExpressRoute. O primeiro comando usa o cmdlet **Get-AzExpressRoute Circuit** para criar uma referência de objeto a um circuito chamado Contoso Circuit; essa referência de objeto é armazenada na variável $Circuit. O segundo comando usa essa referência de objeto e o cmdlet **Get-AzExpressRoute CircuitAuthorization** para retornar informações sobre as autorizações associadas à Contoso Circuit.

### Exemplo 2: Obter todas as autorizações do ExpressRoute usando o cmdlet Where-Object ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Esses comandos representam uma variação nos comandos usados no Exemplo 1. Nesse caso, no entanto, as informações são retornadas apenas para as autorizações que estão disponíveis para uso (ou seja, para autorizações que não foram atribuídas a uma rede virtual). Para fazer isso, as informações de autorização de circuito são retornadas no comando 2 e são canaldas para o cmdlet **Where-Object.**
**Where-Object,** then picks out only the authorizations where *the AuthorizationUseStatus* property is set to Available. Para listar apenas as autorizações que não estão disponíveis, use esta sintaxe para a cláusula Where: `{$_.AuthorizationUseStatus -ne "Available"}`

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

### -ExpressRoute Circuit
Especifica a autorização de circuito do ExpressRoute.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da autorização de circuito do ExpressRoute que este cmdlet obtém.
-Nome "Contoso CircuitAuthorization"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSExpressRoute CircuitAuthorization

## Notas

## LINKS RELACIONADOS

[Add-AzExpressRoute CircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRoute Circuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRoute CircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRoute CircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
