---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9427a79c607d56fcc9ce7a39fa24bfa3e301cfc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892075"
---
# <span data-ttu-id="54f5c-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54f5c-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="54f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="54f5c-103">Atualiza uma configuração IP para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="54f5c-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="54f5c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="54f5c-104">SYNTAX</span></span>

### <span data-ttu-id="54f5c-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="54f5c-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54f5c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="54f5c-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54f5c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="54f5c-107">DESCRIPTION</span></span>
<span data-ttu-id="54f5c-108">O cmdlet **Set-AzNetworkInterfaceIpConfig** atualiza uma configuração de IP para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="54f5c-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="54f5c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54f5c-109">EXAMPLES</span></span>

### <span data-ttu-id="54f5c-110">1: Alterar o endereço IP de uma configuração IP</span><span class="sxs-lookup"><span data-stu-id="54f5c-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="54f5c-111">Os dois primeiros comandos obter uma rede virtual chamada myvnet e uma sub-rede chamada mysubnet e armazená-la nas variáveis $vnet e $subnet respectivamente.</span><span class="sxs-lookup"><span data-stu-id="54f5c-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="54f5c-112">O terceiro comando obtém a interface de rede nic1 associada à configuração ip que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="54f5c-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="54f5c-113">O terceiro comando define o endereço IP privado da configuração IP principal ipconfig1 como 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="54f5c-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="54f5c-114">Por fim, o último comando atualiza a interface de rede garantindo que as alterações tenham sido feitas com êxito.</span><span class="sxs-lookup"><span data-stu-id="54f5c-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="54f5c-115">2: Associar uma configuração IP a um grupo de segurança de aplicativos</span><span class="sxs-lookup"><span data-stu-id="54f5c-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="54f5c-116">Neste exemplo, a variável $asg contém uma referência a um grupo de segurança de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="54f5c-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="54f5c-117">O quarto comando obtém a interface de rede nic1 associada à configuração IP que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="54f5c-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="54f5c-118">O Set-AzNetworkInterfaceIpConfig define o endereço IP privado da configuração IP principal ipconfig1 como 10.0.0.11 e cria uma associação com o grupo de segurança do aplicativo recuperado.</span><span class="sxs-lookup"><span data-stu-id="54f5c-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="54f5c-119">Por fim, o último comando atualiza a interface de rede garantindo que as alterações tenham sido feitas com êxito.</span><span class="sxs-lookup"><span data-stu-id="54f5c-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="54f5c-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="54f5c-120">PARAMETERS</span></span>

### <span data-ttu-id="54f5c-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="54f5c-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="54f5c-122">Especifica uma coleção de referências de pool de endereços de back-end do gateway de aplicativo ao qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="54f5c-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54f5c-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="54f5c-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="54f5c-124">Especifica uma coleção de referências de pool de endereços de back-end do gateway de aplicativo ao qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="54f5c-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54f5c-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54f5c-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="54f5c-126">Especifica uma coleção de referências de grupo de segurança de aplicativos às quais essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="54f5c-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54f5c-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="54f5c-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="54f5c-128">Especifica uma coleção de referências de grupo de segurança de aplicativos às quais essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="54f5c-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54f5c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f5c-129">-DefaultProfile</span></span>
<span data-ttu-id="54f5c-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="54f5c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54f5c-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="54f5c-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="54f5c-132">Especifica uma coleção de referências de pool de endereços de back-end do balanceador de carga ao qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="54f5c-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54f5c-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="54f5c-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="54f5c-134">Especifica uma coleção de referências de pool de endereços de back-end do balanceador de carga ao qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="54f5c-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54f5c-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="54f5c-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="54f5c-136">Especifica uma coleção de referências de regra NAT (conversão de endereço de rede de entrada) do balanceador de carga à qual essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="54f5c-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54f5c-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="54f5c-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="54f5c-138">Especifica uma coleção de referências de regra NAT de entrada do balanceador de carga às quais essa configuração IP da interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="54f5c-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54f5c-139">-Name</span><span class="sxs-lookup"><span data-stu-id="54f5c-139">-Name</span></span>
<span data-ttu-id="54f5c-140">Especifica o nome da configuração IP de rede para a qual este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="54f5c-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="54f5c-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="54f5c-141">-NetworkInterface</span></span>
<span data-ttu-id="54f5c-142">Especifica um **objeto NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="54f5c-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="54f5c-143">Este cmdlet adiciona uma configuração IP de interface de rede ao objeto especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="54f5c-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="54f5c-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="54f5c-144">-Primary</span></span>
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

### <span data-ttu-id="54f5c-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="54f5c-145">-PrivateIpAddress</span></span>
<span data-ttu-id="54f5c-146">Especifica o endereço IP estático da configuração IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="54f5c-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="54f5c-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="54f5c-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="54f5c-148">Especifica a versão de endereço IP de uma configuração IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="54f5c-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="54f5c-149">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="54f5c-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54f5c-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="54f5c-150">IPv4</span></span>
- <span data-ttu-id="54f5c-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="54f5c-151">IPv6</span></span>

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

### <span data-ttu-id="54f5c-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54f5c-152">-PublicIpAddress</span></span>
<span data-ttu-id="54f5c-153">Especifica um **objeto PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="54f5c-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="54f5c-154">Este cmdlet cria uma referência a um Endereço IP público para associar a essa configuração IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="54f5c-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="54f5c-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="54f5c-155">-PublicIpAddressId</span></span>
<span data-ttu-id="54f5c-156">Este cmdlet cria uma referência a um Endereço IP público para associar a essa configuração IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="54f5c-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="54f5c-157">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="54f5c-157">-Subnet</span></span>
<span data-ttu-id="54f5c-158">Especifica um **objeto Subnet.**</span><span class="sxs-lookup"><span data-stu-id="54f5c-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="54f5c-159">Este cmdlet cria uma referência a uma sub-rede na qual essa configuração IP da interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="54f5c-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="54f5c-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="54f5c-160">-SubnetId</span></span>
<span data-ttu-id="54f5c-161">Este cmdlet cria uma referência a uma sub-rede na qual essa configuração IP da interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="54f5c-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="54f5c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f5c-162">CommonParameters</span></span>
<span data-ttu-id="54f5c-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f5c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f5c-164">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f5c-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f5c-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54f5c-165">INPUTS</span></span>

### <span data-ttu-id="54f5c-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="54f5c-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="54f5c-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="54f5c-167">System.String[]</span></span>

### <span data-ttu-id="54f5c-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="54f5c-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="54f5c-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="54f5c-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="54f5c-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="54f5c-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="54f5c-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="54f5c-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="54f5c-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="54f5c-172">OUTPUTS</span></span>

### <span data-ttu-id="54f5c-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="54f5c-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="54f5c-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="54f5c-174">NOTES</span></span>
* <span data-ttu-id="54f5c-175">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="54f5c-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="54f5c-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54f5c-176">RELATED LINKS</span></span>

[<span data-ttu-id="54f5c-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54f5c-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54f5c-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54f5c-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54f5c-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54f5c-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54f5c-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54f5c-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
