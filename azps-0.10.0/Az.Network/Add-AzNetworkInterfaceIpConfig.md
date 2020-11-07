---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0c244248a01038f6b22ec6037a1320df131d4b18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775627"
---
# <span data-ttu-id="d5248-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d5248-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d5248-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5248-102">SYNOPSIS</span></span>
<span data-ttu-id="d5248-103">Adiciona uma configuração de IP de interface de rede a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d5248-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="d5248-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5248-104">SYNTAX</span></span>

### <span data-ttu-id="d5248-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5248-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5248-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5248-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5248-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5248-107">DESCRIPTION</span></span>
<span data-ttu-id="d5248-108">O cmdlet **Add-AzNetworkInterfaceIpConfig** adiciona uma configuração de IP de interface de rede a uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5248-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="d5248-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5248-109">EXAMPLES</span></span>

### <span data-ttu-id="d5248-110">Exemplo 1: adicionar uma nova configuração de IP com um grupo de segurança de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d5248-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzNetworkInterface
```

<span data-ttu-id="d5248-111">Neste exemplo, criamos uma nova interface de rede mynetworkinterface que pertence a uma sub-rede na nova rede virtual MyVNET.</span><span class="sxs-lookup"><span data-stu-id="d5248-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="d5248-112">Também criamos um MyASG de grupo de segurança de aplicativo vazio para associar às configurações de IP na interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d5248-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="d5248-113">Após a criação dos dois objetos, vinculamos a configuração de IP padrão ao objeto MyASG.</span><span class="sxs-lookup"><span data-stu-id="d5248-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="d5248-114">Em seguida, criamos uma nova configuração de IP na interface de rede também vinculada ao objeto do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5248-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="d5248-115">OS</span><span class="sxs-lookup"><span data-stu-id="d5248-115">PARAMETERS</span></span>

### <span data-ttu-id="d5248-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5248-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="d5248-117">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d5248-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d5248-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d5248-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="d5248-119">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d5248-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d5248-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d5248-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="d5248-121">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d5248-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d5248-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d5248-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="d5248-123">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d5248-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d5248-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5248-124">-DefaultProfile</span></span>
<span data-ttu-id="d5248-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5248-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5248-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5248-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="d5248-127">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d5248-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d5248-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d5248-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="d5248-129">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d5248-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d5248-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="d5248-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="d5248-131">Especifica uma coleção de referências de regra NAT (conversão de endereço de rede) de balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d5248-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d5248-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="d5248-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="d5248-133">Especifica uma coleção de referências de regra NAT de balanceamento de carga de entrada às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="d5248-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d5248-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5248-134">-Name</span></span>
<span data-ttu-id="d5248-135">Especifica o nome da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d5248-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="d5248-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d5248-136">-NetworkInterface</span></span>
<span data-ttu-id="d5248-137">Especifica um objeto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="d5248-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="d5248-138">Esse cmdlet adiciona uma configuração de IP de interface de rede ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d5248-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5248-139">-Principal</span><span class="sxs-lookup"><span data-stu-id="d5248-139">-Primary</span></span>
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

### <span data-ttu-id="d5248-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5248-140">-PrivateIpAddress</span></span>
<span data-ttu-id="d5248-141">Especifica o endereço IP estático da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d5248-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="d5248-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d5248-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="d5248-143">Especifica a versão de endereço IP de uma configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d5248-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="d5248-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d5248-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d5248-145">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="d5248-145">IPv4</span></span>
- <span data-ttu-id="d5248-146">IPv4</span><span class="sxs-lookup"><span data-stu-id="d5248-146">IPv6</span></span>

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

### <span data-ttu-id="d5248-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5248-147">-PublicIpAddress</span></span>
<span data-ttu-id="d5248-148">Especifica um objeto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="d5248-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="d5248-149">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d5248-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="d5248-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d5248-150">-PublicIpAddressId</span></span>
<span data-ttu-id="d5248-151">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d5248-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="d5248-152">-Subnet</span><span class="sxs-lookup"><span data-stu-id="d5248-152">-Subnet</span></span>
<span data-ttu-id="d5248-153">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="d5248-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="d5248-154">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="d5248-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="d5248-155">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="d5248-155">-SubnetId</span></span>
<span data-ttu-id="d5248-156">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="d5248-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="d5248-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5248-157">CommonParameters</span></span>
<span data-ttu-id="d5248-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5248-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5248-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5248-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5248-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5248-160">INPUTS</span></span>

### <span data-ttu-id="d5248-161">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d5248-161">PSNetworkInterface</span></span>
<span data-ttu-id="d5248-162">O parâmetro ' NetworkInterface ' aceita o valor do tipo ' PSNetworkInterface ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d5248-162">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="d5248-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5248-163">OUTPUTS</span></span>

### <span data-ttu-id="d5248-164">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d5248-164">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d5248-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5248-165">NOTES</span></span>
* <span data-ttu-id="d5248-166">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="d5248-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d5248-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5248-167">RELATED LINKS</span></span>

[<span data-ttu-id="d5248-168">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d5248-168">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d5248-169">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d5248-169">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d5248-170">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d5248-170">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d5248-171">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d5248-171">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


