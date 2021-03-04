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
# <span data-ttu-id="40e04-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="40e04-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="40e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40e04-102">SYNOPSIS</span></span>
<span data-ttu-id="40e04-103">Adiciona uma configuração IP de interface de rede a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="40e04-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="40e04-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="40e04-104">SYNTAX</span></span>

### <span data-ttu-id="40e04-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="40e04-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40e04-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="40e04-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40e04-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="40e04-107">DESCRIPTION</span></span>
<span data-ttu-id="40e04-108">O cmdlet **Add-AzNetworkInterfaceIpConfig** adiciona uma configuração IP de interface de rede a uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="40e04-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="40e04-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40e04-109">EXAMPLES</span></span>

### <span data-ttu-id="40e04-110">Exemplo 1: Adicionar uma nova configuração IP com um grupo de segurança de aplicativos</span><span class="sxs-lookup"><span data-stu-id="40e04-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="40e04-111">Neste exemplo, criamos uma nova interface de rede MyNetworkInterface que pertence a uma sub-rede na nova rede virtual MyVNET.</span><span class="sxs-lookup"><span data-stu-id="40e04-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="40e04-112">Também criamos um grupo de segurança de aplicativo vazio MyASG para associar às configurações IP na interface de rede.</span><span class="sxs-lookup"><span data-stu-id="40e04-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="40e04-113">Depois que ambos os objetos são criados, vinculamos a configuração IP padrão ao objeto MyASG.</span><span class="sxs-lookup"><span data-stu-id="40e04-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="40e04-114">Por fim, criamos uma nova configuração IP na interface de rede também vinculada ao objeto do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40e04-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="40e04-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="40e04-115">PARAMETERS</span></span>

### <span data-ttu-id="40e04-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40e04-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="40e04-117">Especifica uma coleção de referências de pool de endereços de back-end do gateway de aplicativo ao qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="40e04-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="40e04-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="40e04-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="40e04-119">Especifica uma coleção de referências de pool de endereços de back-end do gateway de aplicativo ao qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="40e04-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="40e04-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="40e04-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="40e04-121">Especifica uma coleção de referências de grupo de segurança de aplicativos às quais essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="40e04-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="40e04-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="40e04-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="40e04-123">Especifica uma coleção de referências de grupo de segurança de aplicativos às quais essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="40e04-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="40e04-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e04-124">-DefaultProfile</span></span>
<span data-ttu-id="40e04-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="40e04-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e04-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="40e04-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="40e04-127">Especifica uma coleção de referências de pool de endereços de back-end do balanceador de carga ao qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="40e04-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="40e04-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="40e04-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="40e04-129">Especifica uma coleção de referências de pool de endereços de back-end do balanceador de carga ao qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="40e04-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="40e04-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="40e04-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="40e04-131">Especifica uma coleção de referências de regra NAT (conversão de endereço de rede de entrada) do balanceador de carga à qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="40e04-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="40e04-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="40e04-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="40e04-133">Especifica uma coleção de referências de regra NAT de entrada do balanceador de carga às quais essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="40e04-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="40e04-134">-Name</span><span class="sxs-lookup"><span data-stu-id="40e04-134">-Name</span></span>
<span data-ttu-id="40e04-135">Especifica o nome da configuração IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="40e04-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="40e04-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="40e04-136">-NetworkInterface</span></span>
<span data-ttu-id="40e04-137">Especifica um **objeto NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="40e04-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="40e04-138">Este cmdlet adiciona uma configuração IP de interface de rede ao objeto especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="40e04-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="40e04-139">-Primary</span><span class="sxs-lookup"><span data-stu-id="40e04-139">-Primary</span></span>
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

### <span data-ttu-id="40e04-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="40e04-140">-PrivateIpAddress</span></span>
<span data-ttu-id="40e04-141">Especifica o endereço IP estático da configuração IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="40e04-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="40e04-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="40e04-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="40e04-143">Especifica a versão de endereço IP de uma configuração IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="40e04-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="40e04-144">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="40e04-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40e04-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="40e04-145">IPv4</span></span>
- <span data-ttu-id="40e04-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="40e04-146">IPv6</span></span>

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

### <span data-ttu-id="40e04-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="40e04-147">-PublicIpAddress</span></span>
<span data-ttu-id="40e04-148">Especifica um **objeto PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="40e04-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="40e04-149">Este cmdlet cria uma referência a um Endereço IP público para associar a essa configuração IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="40e04-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="40e04-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="40e04-150">-PublicIpAddressId</span></span>
<span data-ttu-id="40e04-151">Este cmdlet cria uma referência a um Endereço IP público para associar a essa configuração IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="40e04-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="40e04-152">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="40e04-152">-Subnet</span></span>
<span data-ttu-id="40e04-153">Especifica um **objeto Subnet.**</span><span class="sxs-lookup"><span data-stu-id="40e04-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="40e04-154">Este cmdlet cria uma referência a uma sub-rede na qual essa configuração IP da interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="40e04-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="40e04-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="40e04-155">-SubnetId</span></span>
<span data-ttu-id="40e04-156">Este cmdlet cria uma referência a uma sub-rede na qual essa configuração IP da interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="40e04-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="40e04-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e04-157">CommonParameters</span></span>
<span data-ttu-id="40e04-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e04-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e04-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e04-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e04-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40e04-160">INPUTS</span></span>

### <span data-ttu-id="40e04-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="40e04-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="40e04-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="40e04-162">System.String[]</span></span>

### <span data-ttu-id="40e04-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="40e04-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="40e04-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="40e04-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="40e04-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="40e04-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="40e04-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="40e04-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="40e04-167">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="40e04-167">OUTPUTS</span></span>

### <span data-ttu-id="40e04-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="40e04-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="40e04-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="40e04-169">NOTES</span></span>
* <span data-ttu-id="40e04-170">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="40e04-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="40e04-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40e04-171">RELATED LINKS</span></span>

[<span data-ttu-id="40e04-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="40e04-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="40e04-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="40e04-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="40e04-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="40e04-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="40e04-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="40e04-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
