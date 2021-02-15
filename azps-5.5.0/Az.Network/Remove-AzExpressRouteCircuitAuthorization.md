---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114661"
---
# Remove-AzExpressRouteCircuitAuthorization

## Sinopse
Remove uma autorização de configuração existente do ExpressRoute.

## Sintaxe

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Remove-AzExpressRoute CircuitAuthorization** remove uma autorização atribuída a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam sua rede local ao Azure usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito. Só pode haver uma autorização por rede virtual. A qualquer momento, no entanto, o proprietário do circuito pode usar **Remove-AzExpressRoute CircuitAuthorization** para remover a autorização atribuída a uma rede virtual. Quando isso acontece, a rede virtual correspondente não é mais capaz de usar o circuito do ExpressRoute para se conectar ao Azure.

## Exemplos

### Exemplo 1: Remover uma autorização de circuito de um circuito do ExpressRoute
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Este exemplo remove uma autorização de circuito de um circuito do ExpressRoute. O primeiro comando usa o cmdlet **Get-AzExpressRoute Circuit** para criar uma referência de objeto a um circuito do ExpressRoute chamado Contoso Circuit e armazena o resultado na variável chamada $Circuit.
O segundo comando marca a autorização de circuito Contoso CircuitAuthorization para remoção.
O terceiro comando usa o cmdlet Set-AzExpressRouteCircuit para confirmar a remoção do circuito do ExpressRoute armazenado na variável $Circuit.

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
Especifica o objeto ExpressRoute Circuit que este cmdlet remove.

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
Especifica o nome da autorização de circuito que este cmdlet remove.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit

## Notas

## LINKS RELACIONADOS

[Add-AzExpressRoute CircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRoute Circuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRoute CircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRoute CircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRoute Circuit](./Set-AzExpressRouteCircuit.md)
