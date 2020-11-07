---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 7776bb57215ce3cb9b4291a0a71fdb01e028491e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775382"
---
# <span data-ttu-id="19862-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19862-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="19862-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19862-102">SYNOPSIS</span></span>
<span data-ttu-id="19862-103">Cria uma configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="19862-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="19862-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19862-104">SYNTAX</span></span>

### <span data-ttu-id="19862-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="19862-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19862-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="19862-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19862-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19862-107">DESCRIPTION</span></span>
<span data-ttu-id="19862-108">O cmdlet **New-AzNetworkInterfaceIpConfig** cria uma configuração de IP de interface de rede do Azure para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="19862-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="19862-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19862-109">EXAMPLES</span></span>

### <span data-ttu-id="19862-110">1: criar uma configuração de IP com um endereço IP público para uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="19862-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="19862-111">Os dois primeiros comandos obtêm uma rede virtual chamada myvnet e uma sub-rede chamada mysubnet, respectivamente, que foi criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="19862-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="19862-112">Eles são armazenados em $vnet e $Subnet, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="19862-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="19862-113">O terceiro comando obtém um endereço IP público criado anteriormente chamado PIP1.</span><span class="sxs-lookup"><span data-stu-id="19862-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="19862-114">O comando avançar cria uma nova configuração de IP chamada "IPConfig-1" como a configuração de IP principal com um endereço IP público associado a ela.</span><span class="sxs-lookup"><span data-stu-id="19862-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="19862-115">O último comando cria uma interface de rede chamada mynic1 usando esta configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="19862-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="19862-116">2: criar uma configuração de IP com um endereço IP privado</span><span class="sxs-lookup"><span data-stu-id="19862-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="19862-117">Os dois primeiros comandos obtêm uma rede virtual chamada myvnet e uma sub-rede chamada mysubnet, respectivamente, que foi criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="19862-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="19862-118">Eles são armazenados em $vnet e $Subnet, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="19862-118">These are stored in $vnet and $Subnet respectively.</span></span>  <span data-ttu-id="19862-119">O terceiro comando cria uma nova configuração de IP chamada "IPConfig-2" com um endereço IP privado 10.0.0.5 associado a ele.</span><span class="sxs-lookup"><span data-stu-id="19862-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="19862-120">O último comando cria uma interface de rede chamada mynic1 usando esta configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="19862-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="19862-121">OS</span><span class="sxs-lookup"><span data-stu-id="19862-121">PARAMETERS</span></span>

### <span data-ttu-id="19862-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="19862-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="19862-123">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="19862-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19862-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="19862-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="19862-125">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="19862-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19862-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19862-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="19862-127">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="19862-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19862-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="19862-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="19862-129">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="19862-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19862-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19862-130">-DefaultProfile</span></span>
<span data-ttu-id="19862-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19862-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19862-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="19862-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="19862-133">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="19862-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19862-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="19862-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="19862-135">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="19862-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19862-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="19862-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="19862-137">Especifica uma coleção de referências de regra NAT de balanceamento de carga de entrada às quais essa IPConfiguration de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="19862-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19862-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="19862-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="19862-139">Especifica uma coleção de referências de regra NAT (conversão de endereço de rede) de balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="19862-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19862-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="19862-140">-Name</span></span>
<span data-ttu-id="19862-141">Especifica o nome da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="19862-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="19862-142">-Principal</span><span class="sxs-lookup"><span data-stu-id="19862-142">-Primary</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19862-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="19862-143">-PrivateIpAddress</span></span>
<span data-ttu-id="19862-144">Especifica o endereço IP estático da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="19862-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="19862-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="19862-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="19862-146">Especifica a versão de endereço IP de uma configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="19862-146">Specifies the IP address version of a network interface IP configuration.</span></span>

<span data-ttu-id="19862-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="19862-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19862-148">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="19862-148">IPv4</span></span>
- <span data-ttu-id="19862-149">IPv4</span><span class="sxs-lookup"><span data-stu-id="19862-149">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19862-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="19862-150">-PublicIpAddress</span></span>
<span data-ttu-id="19862-151">Especifica um objeto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="19862-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="19862-152">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="19862-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="19862-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="19862-153">-PublicIpAddressId</span></span>
<span data-ttu-id="19862-154">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="19862-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="19862-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="19862-155">-Subnet</span></span>
<span data-ttu-id="19862-156">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="19862-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="19862-157">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="19862-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="19862-158">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="19862-158">-SubnetId</span></span>
<span data-ttu-id="19862-159">Especifica uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="19862-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="19862-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19862-160">CommonParameters</span></span>
<span data-ttu-id="19862-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19862-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19862-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19862-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19862-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19862-163">INPUTS</span></span>

## <span data-ttu-id="19862-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19862-164">OUTPUTS</span></span>

### <span data-ttu-id="19862-165">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="19862-165">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="19862-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19862-166">NOTES</span></span>
* <span data-ttu-id="19862-167">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="19862-167">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="19862-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19862-168">RELATED LINKS</span></span>

[<span data-ttu-id="19862-169">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19862-169">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="19862-170">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19862-170">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="19862-171">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19862-171">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="19862-172">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="19862-172">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


