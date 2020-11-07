---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0ECE4232-EA5D-46A0-8260-69646E27FA9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 646aaa2ec5d39089627caa97e74990ac3ce43b5c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785921"
---
# Add-AzureRmApplicationGatewayFrontendIPConfig

## Sinopse
Adiciona uma configuração de IP de front-end a um gateway de aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SetByResourceId
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmApplicationGatewayFrontendIPConfig** adiciona uma configuração de IP de front-end a um gateway de aplicativo.
Um gateway de aplicativo dá suporte a dois tipos de configurações de IP front-end: 

- Endereços IP públicos
- Endereços IP particulares usando balanceamento de carga interna (ILB)

Um gateway de aplicativo pode ter no máximo um IP público e um IP privado.
Adicione o endereço IP público e o endereço IP privado como IPs de front-end separados.

## EXEMPLOS

### Exemplo 1: adicionar um IP público como o endereço IP de front-end
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

O primeiro comando cria um objeto de endereço IP público e o armazena na variável $PublicIp.
O segundo comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.
O terceiro comando adiciona a configuração de IP de front-end chamada FrontEndIp01, para o gateway em $AppGw, usando o endereço armazenado no $PublicIp.

### Exemplo 2: adicionar um IP privado estático como o endereço IP de front-end
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.
O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.
O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.
O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1.

### Exemplo 3: adicionar um IP privado dinâmico como o endereço IP de front-end
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.
O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.
O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.
O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando.

## OS

### -ApplicationGateway
Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma configuração de IP de front-end.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -Nome
Especifica o nome da configuração de IP de front-end a ser adicionada.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddress
Especifica o endereço IP privado a ser adicionado como um IP front-end para o gateway do aplicativo.
Se especificado, esse IP é alocado estaticamente da sub-rede.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
Especifica o endereço IP público que esse cmdlet adiciona como um endereço IP front-end para o gateway do aplicativo.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Especifica a ID do endereço IP público que esse cmdlet adiciona como um endereço IP front-end para o gateway do aplicativo.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Especifica a sub-rede que esse cmdlet adiciona como configuração de IP de front-end.
Se você especificar esse parâmetro, ele implica que o gateway do aplicativo dá suporte a uma configuração baseada em IP privado.
Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.
Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnetid
Especifica a identificação de sub-rede que esse cmdlet adiciona como a configuração de IP de front-end.
Passar sub-rede implica IP privado.
Se o parâmetro *PrivateIPAddresss* for especificado, ele deve pertencer a essa sub-rede.
Caso contrário, um dos IP desta sub-rede será retirado dinamicamente como o IP front-end do gateway do aplicativo.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmApplicationGatewayFrontendIPConfig](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[New-AzureRmApplicationGatewayFrontendIPConfig](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[Remove-AzureRmApplicationGatewayFrontendIPConfig](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[Set-AzureRmApplicationGatewayFrontendIPConfig](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


