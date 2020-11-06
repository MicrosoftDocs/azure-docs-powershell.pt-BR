---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 8714882128733a2f86bbc526db2f6f4c0548357a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600410"
---
# New-AzApplicationGatewayFrontendIPConfig

## Sinopse
Cria uma configuração de IP de front-end para um gateway de aplicativo.

## SYNTAX

### SetByResourceId
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzApplicationGatewayFrontendIPConfig** cria um CONFIGURATON de IP front-end para um gateway do aplicativo do Azure.
Um gateway de aplicativo dá suporte a dois tipos de configuração de IP front-end: 
- Endereços IP públicos--endereços IP privados usando o balanceamento de carga interno (ILB).
 Um gateway de aplicativo pode ter no máximo um endereço IP público e um endereço IP privado.
O endereço IP público e o endereço IP privado devem ser adicionados separadamente como endereços IP de front-end.

## EXEMPLOS

### Exemplo 1: criar uma configuração de IP de front-end usando um objeto de recurso de IP público
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

O primeiro comando cria um objeto de recurso de IP público e o armazena na variável $PublicIP.
O segundo comando usa $PublicIP para criar uma nova configuração de IP de front-end chamada FrontEndIP01 e a armazena na variável $FrontEnd.

### Exemplo 2: criar um IP privado estático como o endereço IP de front-end
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.
O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.
O terceiro comando cria uma configuração de IP de front-end chamada FrontEndIP02 usando $Subnet do segundo comando e do 10.0.1.1 de endereço IP privado e, em seguida, armazena-o na variável $FrontEnd.

### Exemplo 3: criar um IP privado dinâmico como o endereço IP de front-end
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

O primeiro comando obtém uma rede virtual chamada VNet01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $VNet.
O segundo comando obtém uma configuração de sub-rede chamada Subnet01 usando $VNet do primeiro comando e a armazena na variável $Subnet.
O terceiro comando cria uma configuração de IP de front-end chamada FrontEndIP03 usando $Subnet do segundo comando e armazena-o na variável $FrontEnd.

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

### -Nome
Especifica o nome da configuração de IP de front-end que este cmdlet cria.

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
Especifica o endereço IP privado que esse cmdlet associa ao endereço IP front-end do gateway do aplicativo.
Isso pode ser especificado apenas se uma sub-rede for especificada.
Este IP é alocado estaticamente da sub-rede.

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
Especifica o objeto de endereço IP público que esse cmdlet associa ao endereço IP de front-end do gateway do aplicativo.

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
Especifica a identificação do endereço IP público que esse cmdlet associa ao IP de front-end do gateway do aplicativo.

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
Especifica o objeto de sub-rede que este cmdlet associa ao endereço IP de front-end do gateway do aplicativo.
Se você especificar esse parâmetro, ele indicará que o gateway usa um endereço IP privado.
Se o parâmetro *PrivateIPAddresss* for especificado, ele deve pertencer à sub-rede especificada por esse parâmetro.
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
Especifica a ID de sub-rede que esse cmdlet associa à configuração de IP de front-end do gateway do aplicativo.
Se você especificar o parâmetro *subnet* , isso significa que o gateway usa um endereço IP privado.
Se o parâmetro *PrivateIPAddress* for especificado, ele deve pertencer à sub-rede especificada pela *sub-rede*.
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

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration

## INFORMA

## LINKS RELACIONADOS

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-AzApplicationGatewayFrontendIPConfig](./Set-AzApplicationGatewayFrontendIPConfig.md)


