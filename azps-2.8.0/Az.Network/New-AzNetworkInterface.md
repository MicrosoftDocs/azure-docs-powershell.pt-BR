---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 63f7dc9fd60e8ef4de77790f2fb66b8143c72b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772358"
---
# <span data-ttu-id="09c26-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09c26-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="09c26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09c26-102">SYNOPSIS</span></span>
<span data-ttu-id="09c26-103">Cria uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-103">Creates a network interface.</span></span>

## <span data-ttu-id="09c26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09c26-104">SYNTAX</span></span>

### <span data-ttu-id="09c26-105">SetByIpConfigurationResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="09c26-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c26-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="09c26-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c26-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="09c26-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09c26-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="09c26-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09c26-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09c26-109">DESCRIPTION</span></span>
<span data-ttu-id="09c26-110">O cmdlet **New-AzNetworkInterface** cria uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="09c26-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="09c26-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09c26-111">EXAMPLES</span></span>

### <span data-ttu-id="09c26-112">Exemplo 1: criar uma interface de rede do Azure</span><span class="sxs-lookup"><span data-stu-id="09c26-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="09c26-113">Esse comando cria uma interface de rede chamada NetworkInterface001 com um endereço IP particular atribuído dinamicamente do Subnet1 na rede virtual chamada VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="09c26-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="09c26-114">O comando também atribui dois servidores DNS à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="09c26-115">O recurso filho da IPConfiguration será criado automaticamente usando o nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="09c26-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="09c26-116">Exemplo 2: criar uma interface de rede do Azure usando um objeto de configuração de IP</span><span class="sxs-lookup"><span data-stu-id="09c26-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="09c26-117">Este exemplo cria uma nova interface de rede usando um objeto de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="09c26-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="09c26-118">O objeto de configuração de IP especifica um endereço IPv4 privado estático.</span><span class="sxs-lookup"><span data-stu-id="09c26-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="09c26-119">O primeiro comando cria uma configuração de IP de interface de rede chamada IPConfig1 e armazena a configuração na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="09c26-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="09c26-120">O segundo comando cria uma interface de rede chamada NetworkInterface1 que usa a configuração de IP da interface de rede armazenada na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="09c26-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="09c26-121">OS</span><span class="sxs-lookup"><span data-stu-id="09c26-121">PARAMETERS</span></span>

### <span data-ttu-id="09c26-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="09c26-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="09c26-123">Especifica um objeto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="09c26-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="09c26-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="09c26-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="09c26-125">Especifica a ID de um objeto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="09c26-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="09c26-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="09c26-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="09c26-127">Especifica uma coleção de referências do grupo de segurança do aplicativo à qual a configuração de IP da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="09c26-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="09c26-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="09c26-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="09c26-129">Especifica uma coleção de referências do grupo de segurança do aplicativo à qual a configuração de IP da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="09c26-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="09c26-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09c26-130">-AsJob</span></span>
<span data-ttu-id="09c26-131">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="09c26-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09c26-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c26-132">-DefaultProfile</span></span>
<span data-ttu-id="09c26-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09c26-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09c26-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="09c26-134">-DnsServer</span></span>
<span data-ttu-id="09c26-135">Especifica o servidor DNS para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-135">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="09c26-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="09c26-137">Permite a rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="09c26-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="09c26-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="09c26-138">-EnableIPForwarding</span></span>
<span data-ttu-id="09c26-139">Indica que esse cmdlet habilita o encaminhamento de IP para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="09c26-140">O encaminhamento de IP permite que uma máquina virtual receba tráfego endereçado a outros destinos.</span><span class="sxs-lookup"><span data-stu-id="09c26-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="09c26-141">-Force</span><span class="sxs-lookup"><span data-stu-id="09c26-141">-Force</span></span>
<span data-ttu-id="09c26-142">Força a criação da interface de rede mesmo que já exista uma interface de rede com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="09c26-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="09c26-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="09c26-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="09c26-144">Especifica o rótulo de nome DNS interno para a nova interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="09c26-145">-IpConfiguration</span></span>
<span data-ttu-id="09c26-146">Especifica a configuração de IP que este cmdlet usa para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="09c26-147">-IpConfigurationName</span></span>
<span data-ttu-id="09c26-148">Especifica o nome de uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="09c26-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="09c26-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="09c26-150">Especifica um objeto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="09c26-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="09c26-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="09c26-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="09c26-152">Especifica a ID de um objeto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="09c26-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="09c26-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="09c26-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="09c26-154">Especifica uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="09c26-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="09c26-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="09c26-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="09c26-156">Especifica a ID de uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="09c26-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="09c26-157">-Local</span><span class="sxs-lookup"><span data-stu-id="09c26-157">-Location</span></span>
<span data-ttu-id="09c26-158">Especifica a região para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-158">Specifies the region for a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="09c26-159">-Name</span></span>
<span data-ttu-id="09c26-160">Especifica o nome da interface de rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="09c26-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="09c26-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="09c26-162">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="09c26-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="09c26-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="09c26-164">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="09c26-165">-PrivateIpAddress</span></span>
<span data-ttu-id="09c26-166">Especifica um endereço IP IPv4 estático a ser atribuído a essa interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09c26-167">-PublicIpAddress</span></span>
<span data-ttu-id="09c26-168">Especifica um objeto **PublicIPAddress** para atribuir a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="09c26-169">-PublicIpAddressId</span></span>
<span data-ttu-id="09c26-170">Especifica a ID de um objeto **PublicIPAddress** a ser atribuído a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09c26-171">-ResourceGroupName</span></span>
<span data-ttu-id="09c26-172">Especifica o nome de um grupo de recursos ao qual a interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="09c26-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-173">-Subnet</span><span class="sxs-lookup"><span data-stu-id="09c26-173">-Subnet</span></span>
<span data-ttu-id="09c26-174">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="09c26-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="09c26-175">Esse cmdlet cria uma interface de rede para a sub-rede que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="09c26-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-176">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="09c26-176">-SubnetId</span></span>
<span data-ttu-id="09c26-177">Especifica a ID da sub-rede para a qual criar uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="09c26-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-178">-Marca</span><span class="sxs-lookup"><span data-stu-id="09c26-178">-Tag</span></span>
<span data-ttu-id="09c26-179">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="09c26-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="09c26-180">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="09c26-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-181">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09c26-181">-Confirm</span></span>
<span data-ttu-id="09c26-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09c26-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c26-183">-WhatIf</span></span>
<span data-ttu-id="09c26-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09c26-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09c26-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09c26-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c26-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c26-186">CommonParameters</span></span>
<span data-ttu-id="09c26-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c26-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c26-188">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c26-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c26-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09c26-189">INPUTS</span></span>

### <span data-ttu-id="09c26-190">System. String</span><span class="sxs-lookup"><span data-stu-id="09c26-190">System.String</span></span>

### <span data-ttu-id="09c26-191">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="09c26-191">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="09c26-192">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="09c26-192">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="09c26-193">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09c26-193">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="09c26-194">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="09c26-194">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="09c26-195">System. String []</span><span class="sxs-lookup"><span data-stu-id="09c26-195">System.String[]</span></span>

### <span data-ttu-id="09c26-196">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="09c26-196">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="09c26-197">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="09c26-197">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="09c26-198">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="09c26-198">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="09c26-199">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="09c26-199">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="09c26-200">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="09c26-200">System.Collections.Hashtable</span></span>

## <span data-ttu-id="09c26-201">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09c26-201">OUTPUTS</span></span>

### <span data-ttu-id="09c26-202">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09c26-202">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="09c26-203">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09c26-203">NOTES</span></span>

## <span data-ttu-id="09c26-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09c26-204">RELATED LINKS</span></span>

[<span data-ttu-id="09c26-205">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09c26-205">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="09c26-206">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09c26-206">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="09c26-207">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09c26-207">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
