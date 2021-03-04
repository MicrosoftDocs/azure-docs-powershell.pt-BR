---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 47ad7c00c2db310003dcc87b20405d05ec7f1f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892837"
---
# Add-AzNetworkInterfaceIpConfig

## SYNOPSIS
Adiciona uma configuração IP de interface de rede a uma interface de rede.

## SINTAXE

### SetByResource (Padrão)
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Add-AzNetworkInterfaceIpConfig** adiciona uma configuração IP de interface de rede a uma interface de rede do Azure.

## EXEMPLOS

### Exemplo 1: Adicionar uma nova configuração IP com um grupo de segurança de aplicativos
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

Neste exemplo, criamos uma nova interface de rede MyNetworkInterface que pertence a uma sub-rede na nova rede virtual MyVNET. Também criamos um grupo de segurança de aplicativo vazio MyASG para associar às configurações IP na interface de rede. Depois que ambos os objetos são criados, vinculamos a configuração IP padrão ao objeto MyASG. Por fim, criamos uma nova configuração IP na interface de rede também vinculada ao objeto do grupo de segurança do aplicativo.

## PARÂMETROS

### -ApplicationGatewayBackendAddressPool
Especifica uma coleção de referências de pool de endereços de back-end do gateway de aplicativo ao qual essa configuração IP da interface de rede pertence.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationGatewayBackendAddressPoolId
Especifica uma coleção de referências de pool de endereços de back-end do gateway de aplicativo ao qual essa configuração IP da interface de rede pertence.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroup
Especifica uma coleção de referências de grupo de segurança de aplicativos às quais essa configuração IP da interface de rede pertence.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroupId
Especifica uma coleção de referências de grupo de segurança de aplicativos às quais essa configuração IP da interface de rede pertence.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -LoadBalancerBackendAddressPool
Especifica uma coleção de referências de pool de endereços de back-end do balanceador de carga ao qual essa configuração IP da interface de rede pertence.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolId
Especifica uma coleção de referências de pool de endereços de back-end do balanceador de carga ao qual essa configuração IP da interface de rede pertence.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRule
Especifica uma coleção de referências de regra NAT (conversão de endereço de rede de entrada) do balanceador de carga à qual essa configuração IP da interface de rede pertence.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRuleId
Especifica uma coleção de referências de regra NAT de entrada do balanceador de carga às quais essa configuração IP da interface de rede pertence.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Especifica o nome da configuração IP da interface de rede.

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

### -NetworkInterface
Especifica um **objeto NetworkInterface.**
Este cmdlet adiciona uma configuração IP de interface de rede ao objeto especificado por esse parâmetro.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Primary
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddress
Especifica o endereço IP estático da configuração IP da interface de rede.

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

### -PrivateIpAddressVersion
Especifica a versão de endereço IP de uma configuração IP de interface de rede.
Os valores aceitáveis para este parâmetro são:
- IPv4
- IPv6

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Especifica um **objeto PublicIPAddress.**
Este cmdlet cria uma referência a um Endereço IP público para associar a essa configuração IP da interface de rede.

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

### -PublicIpAddressId
Este cmdlet cria uma referência a um Endereço IP público para associar a essa configuração IP da interface de rede.

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

### -Sub-rede
Especifica um **objeto Subnet.**
Este cmdlet cria uma referência a uma sub-rede na qual essa configuração IP da interface de rede é criada.

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

### -SubnetId
Este cmdlet cria uma referência a uma sub-rede na qual essa configuração IP da interface de rede é criada.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

### System.String[]

### Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]

### Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## NOTES
* Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking

## LINKS RELACIONADOS

[Get-AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)

[New-AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[Remove-AzNetworkInterfaceIpConfig](./Remove-AzNetworkInterfaceIpConfig.md)

[Set-AzNetworkInterfaceIpConfig](./Set-AzNetworkInterfaceIpConfig.md)
