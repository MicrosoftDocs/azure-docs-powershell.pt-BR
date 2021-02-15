---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114616"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## Sinopse
Define o site padrão para um gateway de rede virtual.

## Sintaxe

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** atribui um site padrão de túnel forçado a um gateway de rede virtual.
O túnel forçado fornece uma maneira de redirecionar o tráfego vinculado à Internet de máquinas virtuais do Azure para sua rede local; isso permite inspecionar e auditar o tráfego antes de liberá-lo.
O túnel forçado é realizado usando um túnel de rede virtual privada (VPN); esse túnel requer um site padrão, um gateway local onde todo o tráfego vinculado à Internet do Azure é redirecionado.
**O Set-AzVirtualNetworkGatewayDefaultSite** fornece uma maneira de alterar o site padrão atribuído a um gateway.

## Exemplos

### Exemplo 1: Atribuir um site padrão a um gateway de rede virtual
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

Este exemplo atribui um site padrão a um gateway de rede virtual chamado ContosoVirtualGateway.
O primeiro comando cria uma referência de objeto a um gateway local chamado ContosoLocalGateway.
Essa referência de objeto armazenada na variável chamada $LocalGateway representa o gateway a ser configurado como o site padrão.
O segundo comando cria uma referência de objeto para o gateway de rede virtual e armazena o resultado na variável chamada $VirtualGateway.
O terceiro comando usa o cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** para atribuir o site padrão à ContosoVirtualGateway.

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

### -GatewayDefaultSite
Especifica uma referência de objeto ao gateway de rede local a ser atribuído como o site padrão para a rede virtual especificada.
Você pode usar o cmdlet Get-AzLocalNetworkGateway para criar uma referência de objeto a um gateway local.

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
Especifica uma referência de objeto ao gateway de rede virtual onde o site padrão será atribuído.
Você pode criar uma referência de objeto a um gateway de rede virtual usando o **Get-AzVirtualNetworkGateway** e especificando o nome do gateway.
A variável $VirtualGateway pode ser usada como o valor de parâmetro para o parâmetro *VirtualNetworkGateway:*

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

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## Notas

## LINKS RELACIONADOS

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


