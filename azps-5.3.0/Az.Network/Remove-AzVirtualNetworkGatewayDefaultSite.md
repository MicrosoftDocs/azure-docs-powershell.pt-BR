---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434668"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## Sinopse
Remove o site padrão de um gateway de rede virtual.

## SYNTAX

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** remove o site padrão de encapsulamento forçado de um gateway de rede virtual.
O tunelamento forçado fornece uma maneira de redirecionar o tráfego associado à Internet das máquinas virtuais do Azure para a sua rede local; Isso permite que você inspecione e audite o tráfego antes de liberá-lo.
O encapsulamento forçado é executado usando um encapsulamento de rede virtual privada (VPN); Esse encapsulamento exige um site padrão, um gateway local onde todo o tráfego associado à Internet do Azure é redirecionado.
**Remove-AzVirtualNetworkGatewayDefaultSite** remove o site padrão atribuído a um gateway.
Se fizer isso, você precisará usar o Set-AzVirtualNetworkGatewayDefaultSite para atribuir um novo site padrão antes que o gateway possa ser usado para encapsulamento forçado.

## EXEMPLOS

### Exemplo 1: remover o site padrão atribuído a um gateway de rede virtual
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

Este exemplo remove o site padrão atribuído atualmente a um gateway de rede virtual chamado ContosoVirtualGateway.
O primeiro comando usa **Get-AzVirtualNetworkGateway** para criar uma referência de objeto para o gateway; Essa referência de objeto é armazenada em uma variável chamada $Gateway.
Em seguida, o segundo comando usa **Remove-AzVirtualNetworkGatewayDefaultSite** para remover o site padrão atribuído a esse gateway.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Especifica uma referência de objeto para o gateway de rede virtual que contém o site padrão a ser removido.
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## INFORMA

## LINKS RELACIONADOS

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


