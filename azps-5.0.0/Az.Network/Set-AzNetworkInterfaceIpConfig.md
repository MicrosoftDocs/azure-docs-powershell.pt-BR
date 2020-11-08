---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117588"
---
# <span data-ttu-id="7278a-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7278a-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="7278a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7278a-102">SYNOPSIS</span></span>
<span data-ttu-id="7278a-103">Atualiza uma configuração de IP para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7278a-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="7278a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7278a-104">SYNTAX</span></span>

### <span data-ttu-id="7278a-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7278a-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7278a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7278a-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7278a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7278a-107">DESCRIPTION</span></span>
<span data-ttu-id="7278a-108">O cmdlet **set-AzNetworkInterfaceIpConfig** atualiza uma configuração de IP para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7278a-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="7278a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7278a-109">EXAMPLES</span></span>

### <span data-ttu-id="7278a-110">1: alterando o endereço IP de uma configuração de IP</span><span class="sxs-lookup"><span data-stu-id="7278a-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7278a-111">Os primeiros dois comandos obtêm uma rede virtual chamada myvnet e uma sub-rede chamada mysubnet e a armazenam nas variáveis $vnet e $subnet respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7278a-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="7278a-112">O terceiro comando obtém a interface de rede NIC1 associada à configuração de IP que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="7278a-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="7278a-113">O terceiro comando define o endereço IP privado da configuração de IP primário ipconfig1 para 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="7278a-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="7278a-114">Por fim, o último comando atualiza a interface de rede garantindo que as alterações tenham sido feitas com êxito.</span><span class="sxs-lookup"><span data-stu-id="7278a-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="7278a-115">2: associando uma configuração de IP a um grupo de segurança de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7278a-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7278a-116">Neste exemplo, a variável $asg contém uma referência a um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7278a-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="7278a-117">O quarto comando obtém a interface de rede NIC1 associada à configuração de IP que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="7278a-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="7278a-118">O Set-AzNetworkInterfaceIpConfig define o endereço IP privado da configuração de IP primário ipconfig1 como 10.0.0.11 e cria uma associação com o grupo de segurança de aplicativos recuperados.</span><span class="sxs-lookup"><span data-stu-id="7278a-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="7278a-119">Por fim, o último comando atualiza a interface de rede garantindo que as alterações tenham sido feitas com êxito.</span><span class="sxs-lookup"><span data-stu-id="7278a-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="7278a-120">OS</span><span class="sxs-lookup"><span data-stu-id="7278a-120">PARAMETERS</span></span>

### <span data-ttu-id="7278a-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7278a-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="7278a-122">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="7278a-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7278a-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7278a-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="7278a-124">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="7278a-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7278a-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7278a-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="7278a-126">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="7278a-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7278a-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7278a-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="7278a-128">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="7278a-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7278a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7278a-129">-DefaultProfile</span></span>
<span data-ttu-id="7278a-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7278a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7278a-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7278a-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="7278a-132">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="7278a-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7278a-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7278a-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="7278a-134">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="7278a-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7278a-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="7278a-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="7278a-136">Especifica uma coleção de referências de regra NAT (conversão de endereço de rede) de balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="7278a-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7278a-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="7278a-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="7278a-138">Especifica uma coleção de referências de regra NAT de balanceamento de carga de entrada às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="7278a-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7278a-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="7278a-139">-Name</span></span>
<span data-ttu-id="7278a-140">Especifica o nome da configuração de IP de rede para a qual esse cmdlet se define.</span><span class="sxs-lookup"><span data-stu-id="7278a-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="7278a-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7278a-141">-NetworkInterface</span></span>
<span data-ttu-id="7278a-142">Especifica um objeto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="7278a-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="7278a-143">Esse cmdlet adiciona uma configuração de IP de interface de rede ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7278a-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="7278a-144">-Principal</span><span class="sxs-lookup"><span data-stu-id="7278a-144">-Primary</span></span>
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

### <span data-ttu-id="7278a-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7278a-145">-PrivateIpAddress</span></span>
<span data-ttu-id="7278a-146">Especifica o endereço IP estático da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7278a-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="7278a-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7278a-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7278a-148">Especifica a versão de endereço IP de uma configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7278a-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="7278a-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7278a-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7278a-150">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="7278a-150">IPv4</span></span>
- <span data-ttu-id="7278a-151">IPv4</span><span class="sxs-lookup"><span data-stu-id="7278a-151">IPv6</span></span>

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

### <span data-ttu-id="7278a-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7278a-152">-PublicIpAddress</span></span>
<span data-ttu-id="7278a-153">Especifica um objeto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="7278a-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="7278a-154">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7278a-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7278a-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7278a-155">-PublicIpAddressId</span></span>
<span data-ttu-id="7278a-156">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7278a-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7278a-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7278a-157">-Subnet</span></span>
<span data-ttu-id="7278a-158">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="7278a-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="7278a-159">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="7278a-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7278a-160">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="7278a-160">-SubnetId</span></span>
<span data-ttu-id="7278a-161">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="7278a-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7278a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7278a-162">CommonParameters</span></span>
<span data-ttu-id="7278a-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7278a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7278a-164">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7278a-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7278a-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7278a-165">INPUTS</span></span>

### <span data-ttu-id="7278a-166">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7278a-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="7278a-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="7278a-167">System.String[]</span></span>

### <span data-ttu-id="7278a-168">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="7278a-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="7278a-169">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="7278a-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="7278a-170">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="7278a-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="7278a-171">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="7278a-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="7278a-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7278a-172">OUTPUTS</span></span>

### <span data-ttu-id="7278a-173">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7278a-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7278a-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7278a-174">NOTES</span></span>
* <span data-ttu-id="7278a-175">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="7278a-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7278a-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7278a-176">RELATED LINKS</span></span>

[<span data-ttu-id="7278a-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7278a-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7278a-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7278a-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7278a-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7278a-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7278a-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7278a-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
