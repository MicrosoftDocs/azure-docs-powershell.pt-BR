---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115211"
---
# Add-AzExpressRouteCircuitAuthorization

## Sinopse
Adiciona uma autorização de circuito do ExpressRoute.

## Sintaxe

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O **cmdlet Add-AzExpressRoute CircuitAuthorization** adiciona uma autorização a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual). **O Add-AzExpressRoute CircuitAuthorization** adiciona uma nova autorização a um circuito e, ao mesmo tempo, gera a chave de autorização correspondente. Essas teclas podem ser exibidas a qualquer momento executando o cmdlet Get-AzExpressRouteCircuitAuthorization e, conforme necessário, podem ser copiadas e encaminhadas para o proprietário da rede apropriado.
Observe que, depois de executar **o Add-AzExpressRoute CircuitAuthorization,** você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a chave. Se você não ligar para **Set-AzExpressRoute Circuit,** a autorização será adicionada ao circuito, mas não será habilitada para uso.

## Exemplos

### Exemplo 1: Adicionar uma autorização ao circuito do ExpressRoute especificado
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Os comandos neste exemplo adicionam uma nova autorização a um circuito do ExpressRoute existente. O primeiro comando usa **Get-AzExpressRoute Circuit** para criar uma referência de objeto a um circuito chamado Contoso Circuit. Essa referência de objeto é armazenada em uma variável chamada $Circuit.
No segundo comando, o cmdlet **Add-AzExpressRoute CircuitAuthorization** é usado para adicionar uma nova autorização (Contoso CircuitAuthorization) ao circuito do ExpressRoute. Esse comando adiciona a autorização, mas não ativa essa autorização. A ativação de uma autorização requer **o Set-AzExpressRoute Circuit** mostrado no comando final no exemplo.

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
Especifica o circuito do ExpressRoute ao que este cmdlet adiciona a autorização.

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
Especifica o nome da autorização de circuito a ser adicionado.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit

## Notas

## LINKS RELACIONADOS

[Get-AzExpressRoute Circuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRoute CircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRoute CircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRoute CircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRoute Circuit](./Set-AzExpressRouteCircuit.md)
