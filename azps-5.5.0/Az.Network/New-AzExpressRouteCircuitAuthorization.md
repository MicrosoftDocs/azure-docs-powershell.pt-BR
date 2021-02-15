---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114140"
---
# New-AzExpressRouteCircuitAuthorization

## Sinopse
Cria uma autorização de circuito do ExpressRoute.

## Sintaxe

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzExpressRoute CircuitAuthorization** cria uma autorização de circuito que pode ser adicionada a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar uma rede ao circuito. Só é possível uma autorização por rede virtual.
Depois de criar um circuito do ExpressRoute, você pode usar **o Add-AzExpressRoute CircuitAuthorization** para adicionar uma autorização a esse circuito.
Como alternativa, você pode usar o **New-AzExpressRoute CircuitAuthorization** para criar uma autorização que pode ser adicionada a um novo circuito ao mesmo tempo em que o circuito é criado.

## Exemplos

### Exemplo 1: Criar uma nova autorização de circuito
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Esse comando cria uma nova autorização de circuito chamada Contoso CircuitAuthorization e armazena esse objeto em uma variável chamada $Authorization. Salvar o objeto em uma variável é importante: embora o **New-AzExpressRoute CircuitAuthorization** possa criar uma autorização de circuito, ele não pode adicionar essa autorização a uma rota de circuito. Em vez disso, a variável $Authorization é usada New-AzExpressRouteCircuit criar um novo circuito do ExpressRoute.
Para obter mais informações, consulte a documentação do cmdlet New-AzExpressRouteCircuit dados.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSExpressRoute CircuitAuthorization

## Notas

## LINKS RELACIONADOS

[Add-AzExpressRoute CircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRoute CircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRoute CircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

