---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: e5bbe82276cb356da1e5a66c45145c7daa1d8769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430126"
---
# Set-AzureRmApplicationGatewayFrontendIPConfig

## Sinopse
Modifica uma configuração de endereço IP front-end.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SetByResourceId
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmApplicationGatewayFrontendIPConfig** atualiza uma configuração de IP de front-end.
Um gateway de aplicativo dá suporte a dois tipos de endereços IP front-end: 
- Endereços IP públicos
- Endereços IP privados para os quais a configuração usa balanceamento de carga interno (ILB) um gateway de aplicativo pode ter no máximo um endereço IP público e um endereço IP privado.
Um endereço IP público e um endereço IP privado devem ser adicionados separadamente como endereços IP de front-end.

## EXEMPLOS

### Exemplo 1: definir um IP público como IP front-end de um gateway de aplicativo
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

O primeiro comando cria um objeto de endereço IP público e o armazena na variável $PublicIp.
O segundo comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.
O terceiro comando atualiza a configuração de IP de front-end chamada FrontEndIp01, para o gateway em $AppGw, usando o endereço armazenado no $PublicIp.

### Exemplo 2: definir um IP privado estático como o IP de front-end de um gateway de aplicativo
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.
O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.
O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.
O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando e o endereço IP privado 10.0.1.1.

### Exemplo 3: definir um IP privado dinâmico como o IP de front-end de um gateway de aplicativo
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.
O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.
O terceiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.
O quarto comando adiciona uma configuração de IP de front-end chamada FrontendIP02 usando $Subnet do segundo comando.

## OS

### -ApplicationGateway
Especifica um objeto do gateway do aplicativo no qual modificar a configuração de IP de front-end.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da configuração de IP de front-end que esse cmdlet modifica.

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

### -PrivateIPAddress
Especifica o endereço IP privado.
Se especificado, esse IP é alocado estaticamente da sub-rede.

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

### -PublicIPAddress
Especifica o endereço IP público.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
Especifica a ID do endereço IP público.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
Especifica a sub-rede que o gateway do aplicativo usa.
Especifique esse parâmetro se o gateway usar um endereço IP particular.
Se o endereço *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.
Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnetid
Especifica a identificação de sub-rede.
Especifique esse parâmetro se o gateway usar um endereço IP particular.
Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer a essa sub-rede.
Se *PrivateIPAddress* não for especificado, um dos endereços IP dessa sub-rede será retirado dinamicamente como o endereço IP de front-end do gateway do aplicativo.

```yaml
Type: System.String
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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway
Parâmetros: ApplicationGateway (ByValue)

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmApplicationGatewayFrontendIPConfig](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[Add-AzureRmApplicationGatewayFrontendIPConfig](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[Get-AzureRmApplicationGatewayFrontendIPConfig](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[New-AzureRmApplicationGatewayFrontendIPConfig](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[Remove-AzureRmApplicationGatewayFrontendIPConfig](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)


