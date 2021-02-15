---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111585"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## Sinopse
Remove o site padrão de um gateway de rede virtual.

## Sintaxe

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** remove o site padrão de túnel forçado de um gateway de rede virtual.
O túnel forçado fornece uma maneira de redirecionar o tráfego vinculado à Internet de máquinas virtuais do Azure para sua rede local; isso permite inspecionar e auditar o tráfego antes de liberá-lo.
O túnel forçado é realizado usando um túnel de rede virtual privada (VPN); esse túnel requer um site padrão, um gateway local onde todo o tráfego vinculado à Internet do Azure é redirecionado.
**Remove-AzVirtualNetworkGatewayDefaultSite** remove o site padrão atribuído a um gateway.
Se você fizer isso, precisará usar o Set-AzVirtualNetworkGatewayDefaultSite para atribuir um novo site padrão antes que o gateway possa ser usado para túnel forçado.

## Exemplos

### Exemplo 1: Remover o site padrão atribuído a um gateway de rede virtual
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

Este exemplo remove o site padrão atualmente atribuído a um gateway de rede virtual chamado ContosoVirtualGateway.
O primeiro comando usa **Get-AzVirtualNetworkGateway** para criar uma referência de objeto ao gateway; essa referência de objeto é armazenada em uma variável chamada $Gateway.
O segundo comando usa **Remove-AzVirtualNetworkGatewayDefaultSite** para remover o site padrão atribuído a esse gateway.

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

### -VirtualNetworkGateway
Especifica uma referência de objeto ao gateway de rede virtual que contém o site padrão a ser removido.
Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzVirtualNetworkGateway e especificando o nome do gateway.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## Notas

## LINKS RELACIONADOS

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


