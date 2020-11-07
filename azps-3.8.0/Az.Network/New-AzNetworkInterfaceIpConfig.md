---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 80ffb0adf7703553d22cf991ad84a1af3b8e229c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942137"
---
# <span data-ttu-id="d0451-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0451-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d0451-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0451-102">SYNOPSIS</span></span>
<span data-ttu-id="d0451-103">Cria uma configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d0451-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="d0451-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0451-104">SYNTAX</span></span>

### <span data-ttu-id="d0451-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0451-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0451-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0451-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0451-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0451-107">DESCRIPTION</span></span>
<span data-ttu-id="d0451-108">O cmdlet **New-AzNetworkInterfaceIpConfig** cria uma configuração de IP de interface de rede do Azure para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d0451-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="d0451-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0451-109">EXAMPLES</span></span>

### <span data-ttu-id="d0451-110">1: criar uma configuração de IP com um endereço IP público para uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="d0451-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="d0451-111">Os dois primeiros comandos obtêm uma rede virtual chamada myvnet e uma sub-rede chamada mysubnet, respectivamente, que foi criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d0451-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="d0451-112">Eles são armazenados em $vnet e $Subnet, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d0451-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="d0451-113">O terceiro comando obtém um endereço IP público criado anteriormente chamado PIP1.</span><span class="sxs-lookup"><span data-stu-id="d0451-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="d0451-114">O comando avançar cria uma nova configuração de IP chamada "IPConfig-1" como a configuração de IP principal com um endereço IP público associado a ela.</span><span class="sxs-lookup"><span data-stu-id="d0451-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="d0451-115">O último comando cria uma interface de rede chamada mynic1 usando esta configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="d0451-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="d0451-116">2: criar uma configuração de IP com um endereço IP privado</span><span class="sxs-lookup"><span data-stu-id="d0451-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="d0451-117">Os dois primeiros comandos obtêm uma rede virtual chamada myvnet e uma sub-rede chamada mysubnet, respectivamente, que foi criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d0451-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="d0451-118">Eles são armazenados em $vnet e $Subnet, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d0451-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="d0451-119">O terceiro comando cria uma nova configuração de IP chamada "IPConfig-2" com um endereço IP privado 10.0.0.5 associado a ele.</span><span class="sxs-lookup"><span data-stu-id="d0451-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="d0451-120">O último comando cria uma interface de rede chamada mynic1 usando esta configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="d0451-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="d0451-121">OS</span><span class="sxs-lookup"><span data-stu-id="d0451-121">PARAMETERS</span></span>

### <span data-ttu-id="d0451-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0451-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="d0451-123">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d0451-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d0451-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d0451-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="d0451-125">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d0451-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d0451-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d0451-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="d0451-127">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d0451-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d0451-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d0451-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="d0451-129">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d0451-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d0451-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0451-130">-DefaultProfile</span></span>
<span data-ttu-id="d0451-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0451-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0451-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0451-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="d0451-133">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d0451-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d0451-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d0451-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="d0451-135">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d0451-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d0451-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="d0451-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="d0451-137">Especifica uma coleção de referências de regra NAT de balanceamento de carga de entrada às quais essa IPConfiguration de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d0451-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="d0451-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="d0451-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="d0451-139">Especifica uma coleção de referências de regra NAT (conversão de endereço de rede) de balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d0451-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d0451-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0451-140">-Name</span></span>
<span data-ttu-id="d0451-141">Especifica o nome da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d0451-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="d0451-142">-Principal</span><span class="sxs-lookup"><span data-stu-id="d0451-142">-Primary</span></span>
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

### <span data-ttu-id="d0451-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0451-143">-PrivateIpAddress</span></span>
<span data-ttu-id="d0451-144">Especifica o endereço IP estático da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d0451-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="d0451-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d0451-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="d0451-146">Especifica a versão de endereço IP de uma configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d0451-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="d0451-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d0451-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0451-148">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="d0451-148">IPv4</span></span>
- <span data-ttu-id="d0451-149">IPv4</span><span class="sxs-lookup"><span data-stu-id="d0451-149">IPv6</span></span>

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

### <span data-ttu-id="d0451-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0451-150">-PublicIpAddress</span></span>
<span data-ttu-id="d0451-151">Especifica um objeto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="d0451-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="d0451-152">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d0451-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="d0451-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d0451-153">-PublicIpAddressId</span></span>
<span data-ttu-id="d0451-154">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d0451-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="d0451-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="d0451-155">-Subnet</span></span>
<span data-ttu-id="d0451-156">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="d0451-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="d0451-157">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="d0451-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="d0451-158">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="d0451-158">-SubnetId</span></span>
<span data-ttu-id="d0451-159">Especifica uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="d0451-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="d0451-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0451-160">CommonParameters</span></span>
<span data-ttu-id="d0451-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0451-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0451-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0451-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0451-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0451-163">INPUTS</span></span>

### <span data-ttu-id="d0451-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="d0451-164">System.String[]</span></span>

### <span data-ttu-id="d0451-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="d0451-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="d0451-166">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="d0451-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="d0451-167">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="d0451-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="d0451-168">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="d0451-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="d0451-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0451-169">OUTPUTS</span></span>

### <span data-ttu-id="d0451-170">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0451-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="d0451-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0451-171">NOTES</span></span>
* <span data-ttu-id="d0451-172">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="d0451-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d0451-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0451-173">RELATED LINKS</span></span>

[<span data-ttu-id="d0451-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0451-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d0451-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0451-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d0451-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0451-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d0451-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d0451-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
