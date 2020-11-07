---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: a4a40f67eef901cd1e93ac004fa01a3224ab222e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775383"
---
# <span data-ttu-id="bc616-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bc616-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="bc616-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc616-102">SYNOPSIS</span></span>
<span data-ttu-id="bc616-103">Cria uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-103">Creates a network interface.</span></span>

## <span data-ttu-id="bc616-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc616-104">SYNTAX</span></span>

### <span data-ttu-id="bc616-105">SetByIpConfigurationResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="bc616-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc616-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="bc616-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc616-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc616-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc616-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bc616-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc616-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc616-109">DESCRIPTION</span></span>
<span data-ttu-id="bc616-110">O cmdlet **New-AzNetworkInterface** cria uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc616-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="bc616-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc616-111">EXAMPLES</span></span>

### <span data-ttu-id="bc616-112">Exemplo 1: criar uma interface de rede do Azure</span><span class="sxs-lookup"><span data-stu-id="bc616-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="bc616-113">Esse comando cria uma interface de rede chamada NetworkInterface001 com um endereço IP particular atribuído dinamicamente do Subnet1 na rede virtual chamada VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="bc616-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="bc616-114">O comando também atribui dois servidores DNS à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="bc616-115">O recurso filho da IPConfiguration será criado automaticamente usando o nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="bc616-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="bc616-116">Exemplo 2: criar uma interface de rede do Azure usando um objeto de configuração de IP</span><span class="sxs-lookup"><span data-stu-id="bc616-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="bc616-117">Este exemplo cria uma nova interface de rede usando um objeto de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="bc616-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="bc616-118">O objeto de configuração de IP especifica um endereço IPv4 privado estático.</span><span class="sxs-lookup"><span data-stu-id="bc616-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="bc616-119">O primeiro comando cria uma configuração de IP de interface de rede chamada IPConfig1 e armazena a configuração na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="bc616-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="bc616-120">O segundo comando cria uma interface de rede chamada NetworkInterface1 que usa a configuração de IP da interface de rede armazenada na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="bc616-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="bc616-121">OS</span><span class="sxs-lookup"><span data-stu-id="bc616-121">PARAMETERS</span></span>

### <span data-ttu-id="bc616-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bc616-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="bc616-123">Especifica um objeto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="bc616-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="bc616-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bc616-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="bc616-125">Especifica a ID de um objeto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="bc616-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="bc616-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bc616-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="bc616-127">Especifica uma coleção de referências do grupo de segurança do aplicativo à qual a configuração de IP da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="bc616-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="bc616-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bc616-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="bc616-129">Especifica uma coleção de referências do grupo de segurança do aplicativo à qual a configuração de IP da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="bc616-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="bc616-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc616-130">-AsJob</span></span>
<span data-ttu-id="bc616-131">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bc616-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc616-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc616-132">-DefaultProfile</span></span>
<span data-ttu-id="bc616-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc616-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc616-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="bc616-134">-DnsServer</span></span>
<span data-ttu-id="bc616-135">Especifica o servidor DNS para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-135">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="bc616-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="bc616-137">Permite a rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="bc616-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="bc616-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="bc616-138">-EnableIPForwarding</span></span>
<span data-ttu-id="bc616-139">Indica que esse cmdlet habilita o encaminhamento de IP para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="bc616-140">O encaminhamento de IP permite que uma máquina virtual receba tráfego endereçado a outros destinos.</span><span class="sxs-lookup"><span data-stu-id="bc616-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="bc616-141">-Force</span><span class="sxs-lookup"><span data-stu-id="bc616-141">-Force</span></span>
<span data-ttu-id="bc616-142">Força a criação da interface de rede mesmo que já exista uma interface de rede com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="bc616-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="bc616-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="bc616-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="bc616-144">Especifica o rótulo de nome DNS interno para a nova interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc616-145">-IpConfiguration</span></span>
<span data-ttu-id="bc616-146">Especifica a configuração de IP que este cmdlet usa para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bc616-147">-IpConfigurationName</span></span>
<span data-ttu-id="bc616-148">Especifica o nome de uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="bc616-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bc616-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="bc616-150">Especifica um objeto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="bc616-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="bc616-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bc616-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="bc616-152">Especifica a ID de um objeto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="bc616-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="bc616-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="bc616-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="bc616-154">Especifica uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="bc616-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="bc616-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="bc616-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="bc616-156">Especifica a ID de uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="bc616-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="bc616-157">-Local</span><span class="sxs-lookup"><span data-stu-id="bc616-157">-Location</span></span>
<span data-ttu-id="bc616-158">Especifica a região para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc616-159">-Name</span></span>
<span data-ttu-id="bc616-160">Especifica o nome da interface de rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="bc616-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bc616-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="bc616-162">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="bc616-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bc616-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="bc616-164">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc616-165">-PrivateIpAddress</span></span>
<span data-ttu-id="bc616-166">Especifica um endereço IP IPv4 estático a ser atribuído a essa interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc616-167">-PublicIpAddress</span></span>
<span data-ttu-id="bc616-168">Especifica um objeto **PublicIPAddress** para atribuir a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bc616-169">-PublicIpAddressId</span></span>
<span data-ttu-id="bc616-170">Especifica a ID de um objeto **PublicIPAddress** a ser atribuído a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc616-171">-ResourceGroupName</span></span>
<span data-ttu-id="bc616-172">Especifica o nome de um grupo de recursos ao qual a interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="bc616-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-173">-Subnet</span><span class="sxs-lookup"><span data-stu-id="bc616-173">-Subnet</span></span>
<span data-ttu-id="bc616-174">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="bc616-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="bc616-175">Esse cmdlet cria uma interface de rede para a sub-rede que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bc616-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-176">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="bc616-176">-SubnetId</span></span>
<span data-ttu-id="bc616-177">Especifica a ID da sub-rede para a qual criar uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bc616-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-178">-Marca</span><span class="sxs-lookup"><span data-stu-id="bc616-178">-Tag</span></span>
<span data-ttu-id="bc616-179">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bc616-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bc616-180">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="bc616-180">For example:</span></span>

<span data-ttu-id="bc616-181">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bc616-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-182">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc616-182">-Confirm</span></span>
<span data-ttu-id="bc616-183">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc616-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc616-184">-WhatIf</span></span>
<span data-ttu-id="bc616-185">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc616-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc616-186">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc616-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc616-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc616-187">CommonParameters</span></span>
<span data-ttu-id="bc616-188">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc616-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc616-189">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc616-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc616-190">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc616-190">INPUTS</span></span>

## <span data-ttu-id="bc616-191">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc616-191">OUTPUTS</span></span>

### <span data-ttu-id="bc616-192">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bc616-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="bc616-193">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc616-193">NOTES</span></span>

## <span data-ttu-id="bc616-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc616-194">RELATED LINKS</span></span>

[<span data-ttu-id="bc616-195">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bc616-195">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="bc616-196">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bc616-196">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="bc616-197">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bc616-197">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
