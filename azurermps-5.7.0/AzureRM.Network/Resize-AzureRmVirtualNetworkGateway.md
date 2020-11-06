---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 92de7fae42a0cf065518cfa8125c76ceb64f8f47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610369"
---
# Resize-AzureRmVirtualNetworkGateway

## Sinopse
Redimensiona um gateway de rede virtual existente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Resize-AzureRmVirtualNetworkGateway** permite que você altere a SKU (unidade de manutenção de estoque) para um gateway de rede virtual.
Os SKUs determinam os recursos de um gateway, incluindo itens como throughput e o número máximo de túneis de IP permitidos.
O Azure é compatível com os SKUs Basic, Standard, High-Performance, VpnGw1, VpnGw2 e VpnGw3 (às vezes chamado de SKUs pequenos, médios e grandes).
Para obter informações detalhadas sobre os recursos de cada tipo de SKU, consulte https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .

Lembre-se de que os SKUs são diferentes em preços e recursos.
Para obter mais informações, consulte https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## EXEMPLOS

### Exemplo 1: alterar o tamanho de um gateway de rede virtual
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Este exemplo altera o tamanho de um gateway de rede virtual chamado ContosoVirtualGateway.

O primeiro comando cria uma referência de objeto para ContosoVirtualGateway; Essa referência de objeto é armazenada em uma variável chamada $Gateway.

Em seguida, o segundo comando usa o cmdlet **Resize-AzureRmVirtualNetworkGateway** para definir a propriedade *GatewaySku* como Basic.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GatewaySku
Especifica o novo tipo de SKU do gateway.
Os valores aceitáveis para esse parâmetro são:

- Basic
- Oficial
- Alto desempenho
- VpnGw1
- VpnGw2
- VpnGw3

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Especifica uma referência de objeto ao gateway de rede virtual a ser redimensionado.
Você pode criar essa referência de objeto usando o Get-AzureRmVirtualNetworkGateway e especificando o nome do gateway.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

###  
Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## EXIBE

###  
Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## INFORMA
Não é possível redimensionar os SKUs Basic/Standard/HighPerformance para os novos SKUs VpnGw1/VpnGw2/VpnGw3. Consulte https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways para obter instruções.

## LINKS RELACIONADOS

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


