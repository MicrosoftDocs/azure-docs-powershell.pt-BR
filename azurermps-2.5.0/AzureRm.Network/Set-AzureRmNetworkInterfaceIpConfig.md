---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: f37f6fe6211ab05b94249b924eb76c4b98d05082
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786255"
---
# <span data-ttu-id="6b6d0-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b6d0-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="6b6d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6d0-103">Define o estado da meta para uma configuração de IP da interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b6d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b6d0-104">SYNTAX</span></span>

### <span data-ttu-id="6b6d0-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="6b6d0-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b6d0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b6d0-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b6d0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b6d0-107">DESCRIPTION</span></span>
<span data-ttu-id="6b6d0-108">O cmdlet **set-AzureRmNetworkInterfaceIpConfig** define o estado da meta para uma configuração de IP da interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="6b6d0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b6d0-109">EXAMPLES</span></span>

### <span data-ttu-id="6b6d0-110">1: alterando o endereço IP de uma configuração de IP</span><span class="sxs-lookup"><span data-stu-id="6b6d0-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="6b6d0-111">Os primeiros dois comandos obtêm uma rede virtual chamada myvnet e uma sub-rede chamada mysubnet e a armazenam nas variáveis $vnet e $subnet respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="6b6d0-112">O terceiro comando obtém a interface de rede NIC1 associada à configuração de IP que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="6b6d0-113">O terceiro comando define o endereço IP privado da configuração de IP primário ipconfig1 para 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="6b6d0-114">Por fim, o último comando atualiza a interface de rede garantindo que as alterações tenham sido feitas com êxito.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="6b6d0-115">2: associando uma configuração de IP a um aplicativo de segurança groupp</span><span class="sxs-lookup"><span data-stu-id="6b6d0-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="6b6d0-116">Neste exemplo, a variável $asg contém uma referência a um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="6b6d0-117">O quarto comando obtém a interface de rede NIC1 associada à configuração de IP que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="6b6d0-118">O Set-AzureRmNetworkInterfaceIpConfig define o endereço IP privado da configuração de IP primário ipconfig1 como 10.0.0.11 e cria uma associação com o grupo de segurança de aplicativos recuperados.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="6b6d0-119">Por fim, o último comando atualiza a interface de rede garantindo que as alterações tenham sido feitas com êxito.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="6b6d0-120">OS</span><span class="sxs-lookup"><span data-stu-id="6b6d0-120">PARAMETERS</span></span>

### <span data-ttu-id="6b6d0-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6b6d0-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="6b6d0-122">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b6d0-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6b6d0-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="6b6d0-124">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b6d0-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6b6d0-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="6b6d0-126">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b6d0-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6b6d0-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="6b6d0-128">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b6d0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6d0-129">-DefaultProfile</span></span>
<span data-ttu-id="6b6d0-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b6d0-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6b6d0-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="6b6d0-132">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b6d0-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6b6d0-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="6b6d0-134">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b6d0-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="6b6d0-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="6b6d0-136">Especifica uma coleção de referências de regra NAT (conversão de endereço de rede) de balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b6d0-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="6b6d0-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="6b6d0-138">Especifica uma coleção de referências de regra NAT de balanceamento de carga de entrada às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="6b6d0-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b6d0-139">-Name</span></span>
<span data-ttu-id="6b6d0-140">Especifica o nome da configuração de IP de rede para a qual esse cmdlet se define.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="6b6d0-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b6d0-141">-NetworkInterface</span></span>
<span data-ttu-id="6b6d0-142">Especifica um objeto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="6b6d0-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="6b6d0-143">Esse cmdlet adiciona uma configuração de IP de interface de rede ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b6d0-144">-Principal</span><span class="sxs-lookup"><span data-stu-id="6b6d0-144">-Primary</span></span>
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

### <span data-ttu-id="6b6d0-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b6d0-145">-PrivateIpAddress</span></span>
<span data-ttu-id="6b6d0-146">Especifica o endereço IP estático da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="6b6d0-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6b6d0-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="6b6d0-148">Especifica a versão de endereço IP de uma configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="6b6d0-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6b6d0-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b6d0-150">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="6b6d0-150">IPv4</span></span>
- <span data-ttu-id="6b6d0-151">IPv4</span><span class="sxs-lookup"><span data-stu-id="6b6d0-151">IPv6</span></span>

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

### <span data-ttu-id="6b6d0-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b6d0-152">-PublicIpAddress</span></span>
<span data-ttu-id="6b6d0-153">Especifica um objeto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="6b6d0-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="6b6d0-154">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="6b6d0-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="6b6d0-155">-PublicIpAddressId</span></span>
<span data-ttu-id="6b6d0-156">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="6b6d0-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6b6d0-157">-Subnet</span></span>
<span data-ttu-id="6b6d0-158">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="6b6d0-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="6b6d0-159">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="6b6d0-160">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="6b6d0-160">-SubnetId</span></span>
<span data-ttu-id="6b6d0-161">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="6b6d0-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6d0-162">CommonParameters</span></span>
<span data-ttu-id="6b6d0-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b6d0-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6d0-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6d0-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6d0-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b6d0-165">INPUTS</span></span>

### <span data-ttu-id="6b6d0-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b6d0-166">PSNetworkInterface</span></span>
<span data-ttu-id="6b6d0-167">O parâmetro ' NetworkInterface ' aceita o valor do tipo ' PSNetworkInterface ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6b6d0-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="6b6d0-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b6d0-168">OUTPUTS</span></span>

### <span data-ttu-id="6b6d0-169">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6b6d0-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6b6d0-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b6d0-170">NOTES</span></span>
* <span data-ttu-id="6b6d0-171">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="6b6d0-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6b6d0-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b6d0-172">RELATED LINKS</span></span>

[<span data-ttu-id="6b6d0-173">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b6d0-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6b6d0-174">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b6d0-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6b6d0-175">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b6d0-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6b6d0-176">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6b6d0-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


