---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429524"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## Sinopse
Define o site padrão para um gateway de rede virtual.

## SYNTAX

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzVirtualNetworkGatewayDefaultSite** atribui um site padrão de encapsulamento forçado a um gateway de rede virtual.
O tunelamento forçado fornece uma maneira de redirecionar o tráfego associado à Internet das máquinas virtuais do Azure para a sua rede local; Isso permite que você inspecione e audite o tráfego antes de liberá-lo.
O encapsulamento forçado é executado usando um encapsulamento de rede virtual privada (VPN); Esse encapsulamento exige um site padrão, um gateway local onde todo o tráfego associado à Internet do Azure é redirecionado.
**Set-AzVirtualNetworkGatewayDefaultSite** fornece uma maneira de alterar o site padrão atribuído a um gateway.

## EXEMPLOS

### Exemplo 1: atribuir um site padrão a um gateway de rede virtual
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

Este exemplo atribui um site padrão a um gateway de rede virtual chamado ContosoVirtualGateway.
O primeiro comando cria uma referência de objeto para um gateway local chamado ContosoLocalGateway.
Essa referência de objeto armazenada na variável chamada $LocalGateway representa o gateway a ser configurado como o site padrão.
Em seguida, o segundo comando cria uma referência de objeto para o gateway de rede virtual e armazena o resultado na variável chamada $VirtualGateway.
O terceiro comando usa o cmdlet **set-AzVirtualNetworkGatewayDefaultSite** para atribuir o site padrão ao ContosoVirtualGateway.

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

### -GatewayDefaultSite
Especifica uma referência de objeto para o gateway de rede local a ser atribuído como o site padrão para a rede virtual especificada.
Você pode usar o cmdlet Get-AzLocalNetworkGateway para criar uma referência de objeto para um gateway local.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Especifica uma referência de objeto para o gateway de rede virtual em que o site padrão será atribuído.
Você pode criar uma referência de objeto para um gateway de rede virtual usando **Get-AzVirtualNetworkGateway** e especificando o nome do gateway.
A variável $VirtualGateway pode ser usada como o valor do parâmetro para o parâmetro *VirtualNetworkGateway* :

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

### Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## INFORMA

## LINKS RELACIONADOS

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


