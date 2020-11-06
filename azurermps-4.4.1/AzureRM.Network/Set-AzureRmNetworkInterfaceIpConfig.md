---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 6bf01750543fa5564e9490ad85d84cc258f10f4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602431"
---
# <span data-ttu-id="f643c-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f643c-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="f643c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f643c-102">SYNOPSIS</span></span>
<span data-ttu-id="f643c-103">Define o estado da meta para uma configuração de IP da interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="f643c-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f643c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f643c-104">SYNTAX</span></span>

### <span data-ttu-id="f643c-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f643c-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="f643c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f643c-106">SetByResourceId</span></span>
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

## <span data-ttu-id="f643c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f643c-107">DESCRIPTION</span></span>
<span data-ttu-id="f643c-108">O cmdlet **set-AzureRmNetworkInterfaceIpConfig** define o estado da meta para uma configuração de IP da interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="f643c-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="f643c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f643c-109">EXAMPLES</span></span>

### <span data-ttu-id="f643c-110">1: alterando o endereço IP de uma configuração de IP</span><span class="sxs-lookup"><span data-stu-id="f643c-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="f643c-111">Os primeiros dois comandos obtêm uma rede virtual chamada myvnet e uma sub-rede chamada mysubnet e a armazenam nas variáveis $vnet e $subnet respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f643c-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="f643c-112">O terceiro comando obtém a interface de rede NIC1 associada à configuração de IP que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="f643c-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="f643c-113">O terceiro comando define o endereço IP privado da configuração de IP primário ipconfig1 para 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="f643c-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="f643c-114">Por fim, o último comando atualiza a interface de rede garantindo que as alterações tenham sido feitas com êxito.</span><span class="sxs-lookup"><span data-stu-id="f643c-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="f643c-115">2: associando uma configuração de IP a um aplicativo de segurança groupp</span><span class="sxs-lookup"><span data-stu-id="f643c-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="f643c-116">Neste exemplo, a variável $asg contém uma referência a um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f643c-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="f643c-117">O quarto comando obtém a interface de rede NIC1 associada à configuração de IP que precisa ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="f643c-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="f643c-118">O Set-AzureRmNetworkInterfaceIpConfig define o endereço IP privado da configuração de IP primário ipconfig1 como 10.0.0.11 e cria uma associação com o grupo de segurança de aplicativos recuperados.</span><span class="sxs-lookup"><span data-stu-id="f643c-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="f643c-119">Por fim, o último comando atualiza a interface de rede garantindo que as alterações tenham sido feitas com êxito.</span><span class="sxs-lookup"><span data-stu-id="f643c-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="f643c-120">OS</span><span class="sxs-lookup"><span data-stu-id="f643c-120">PARAMETERS</span></span>

### <span data-ttu-id="f643c-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f643c-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="f643c-122">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="f643c-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f643c-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f643c-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="f643c-124">Especifica uma coleção de referências de pool de endereços back-end de gateway do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="f643c-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f643c-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f643c-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="f643c-126">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="f643c-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f643c-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f643c-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="f643c-128">Especifica uma coleção de referências do grupo de segurança do aplicativo às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="f643c-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f643c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f643c-129">-DefaultProfile</span></span>
<span data-ttu-id="f643c-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f643c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f643c-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f643c-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="f643c-132">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="f643c-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f643c-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f643c-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="f643c-134">Especifica uma coleção de referências de pool de endereços back-end do balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="f643c-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f643c-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f643c-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="f643c-136">Especifica uma coleção de referências de regra NAT (conversão de endereço de rede) de balanceador de carga às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="f643c-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f643c-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="f643c-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="f643c-138">Especifica uma coleção de referências de regra NAT de balanceamento de carga de entrada às quais essa configuração de IP de interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="f643c-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f643c-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="f643c-139">-Name</span></span>
<span data-ttu-id="f643c-140">Especifica o nome da configuração de IP de rede para a qual esse cmdlet se define.</span><span class="sxs-lookup"><span data-stu-id="f643c-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="f643c-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f643c-141">-NetworkInterface</span></span>
<span data-ttu-id="f643c-142">Especifica um objeto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="f643c-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="f643c-143">Esse cmdlet adiciona uma configuração de IP de interface de rede ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f643c-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="f643c-144">-Principal</span><span class="sxs-lookup"><span data-stu-id="f643c-144">-Primary</span></span>
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

### <span data-ttu-id="f643c-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f643c-145">-PrivateIpAddress</span></span>
<span data-ttu-id="f643c-146">Especifica o endereço IP estático da configuração de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f643c-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="f643c-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f643c-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="f643c-148">Especifica a versão de endereço IP de uma configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f643c-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="f643c-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f643c-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f643c-150">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="f643c-150">IPv4</span></span>
- <span data-ttu-id="f643c-151">IPv4</span><span class="sxs-lookup"><span data-stu-id="f643c-151">IPv6</span></span>

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

### <span data-ttu-id="f643c-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f643c-152">-PublicIpAddress</span></span>
<span data-ttu-id="f643c-153">Especifica um objeto **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="f643c-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="f643c-154">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f643c-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="f643c-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f643c-155">-PublicIpAddressId</span></span>
<span data-ttu-id="f643c-156">Esse cmdlet cria uma referência a um endereço IP público para associar a essa configuração de IP de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f643c-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="f643c-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f643c-157">-Subnet</span></span>
<span data-ttu-id="f643c-158">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="f643c-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="f643c-159">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="f643c-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="f643c-160">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="f643c-160">-SubnetId</span></span>
<span data-ttu-id="f643c-161">Esse cmdlet cria uma referência a uma sub-rede na qual essa configuração de IP de interface de rede é criada.</span><span class="sxs-lookup"><span data-stu-id="f643c-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="f643c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f643c-162">CommonParameters</span></span>
<span data-ttu-id="f643c-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f643c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f643c-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f643c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f643c-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f643c-165">INPUTS</span></span>

### <span data-ttu-id="f643c-166">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f643c-166">PSNetworkInterface</span></span>
<span data-ttu-id="f643c-167">O parâmetro ' NetworkInterface ' aceita o valor do tipo ' PSNetworkInterface ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f643c-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="f643c-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f643c-168">OUTPUTS</span></span>

### <span data-ttu-id="f643c-169">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f643c-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f643c-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f643c-170">NOTES</span></span>
* <span data-ttu-id="f643c-171">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="f643c-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f643c-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f643c-172">RELATED LINKS</span></span>

[<span data-ttu-id="f643c-173">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f643c-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f643c-174">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f643c-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f643c-175">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f643c-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f643c-176">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f643c-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


