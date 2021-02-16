---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 31ec0453b0ce64c27d1bb37d4bf6c0f100a8c760
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100416185"
---
# Resize-AzVirtualNetworkGateway

## Sinopse
Resize um gateway de rede virtual existente.

## Sintaxe

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O **cmdlet Resize-AzVirtualNetworkGateway** permite que você altere a unidade de armazenamento de ações (SKU) para um gateway de rede virtual.
As SKUs determinam os recursos de um gateway, incluindo coisas como produtividade e o número máximo de túnel IP permitido.
O Azure oferece suporte a VpnGw1, VpnGw2, VpnGw3, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (às vezes chamados de SKUs Pequenas, Médias e Grandes).
Para obter informações detalhadas sobre os recursos de cada tipo de SKU, consulte https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Lembre-se de que as SKUs são diferentes no preço, bem como nos recursos.
Para obter mais informações, consulte https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## Exemplos

### Exemplo 1: Alterar o tamanho de um gateway de rede virtual
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Este exemplo altera o tamanho de um gateway de rede virtual chamado ContosoVirtualGateway.
O primeiro comando cria uma referência de objeto para ContosoVirtualGateway; essa referência de objeto é armazenada em uma variável chamada $Gateway.
O segundo comando usa o cmdlet **Resize-AzVirtualNetworkGateway** para definir a propriedade *GatewaySku* como Basic.

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

### -GatewaySku
Especifica o novo tipo de SKU do gateway.
Os valores aceitáveis para este parâmetro são:
- Basic
- Padrão
- Alto desempenho
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Especifica uma referência de objeto ao gateway de rede virtual a ser resized.
Você pode criar essa referência de objeto usando o Get-AzVirtualNetworkGateway e especificando o nome do gateway.

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

### System.String

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## Notas
Não é possível reutilizar de SKUs Basic/Standard/HighPerformance para as novas SKUs VpnGw1/VpnGw2/VpnGw3. O resize ainda não é permitido de/para VpnGw1AZ/VpnGw2AZ/VpnGw3AZ ou ErGw1AZ/ErGw2AZ/ErGw3AZ. O resize só é permitido dentro da 'série' SKU, por exemplo, o VpnGw1AZ pode ser resized para/de VpnGw2AZ/VpnGw3AZ e ErGw1AZ pode ser resized para/a partir de ErGw2AZ/ErGw3AZ. Confira https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways as instruções.

## LINKS RELACIONADOS

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

