---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942136"
---
# <span data-ttu-id="b48f1-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b48f1-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="b48f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b48f1-102">SYNOPSIS</span></span>
<span data-ttu-id="b48f1-103">Cria uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-103">Creates a network interface.</span></span>

## <span data-ttu-id="b48f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b48f1-104">SYNTAX</span></span>

### <span data-ttu-id="b48f1-105">SetByIpConfigurationResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="b48f1-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48f1-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b48f1-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48f1-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b48f1-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48f1-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b48f1-108">SetByResource</span></span>
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

## <span data-ttu-id="b48f1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b48f1-109">DESCRIPTION</span></span>
<span data-ttu-id="b48f1-110">O cmdlet **New-AzNetworkInterface** cria uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="b48f1-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="b48f1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b48f1-111">EXAMPLES</span></span>

### <span data-ttu-id="b48f1-112">Exemplo 1: criar uma interface de rede do Azure</span><span class="sxs-lookup"><span data-stu-id="b48f1-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="b48f1-113">Esse comando cria uma interface de rede chamada NetworkInterface001 com um endereço IP particular atribuído dinamicamente do Subnet1 na rede virtual chamada VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="b48f1-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="b48f1-114">O comando também atribui dois servidores DNS à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="b48f1-115">O recurso filho da IPConfiguration será criado automaticamente usando o nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="b48f1-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="b48f1-116">Exemplo 2: criar uma interface de rede do Azure usando um objeto de configuração de IP</span><span class="sxs-lookup"><span data-stu-id="b48f1-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="b48f1-117">Este exemplo cria uma nova interface de rede usando um objeto de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="b48f1-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="b48f1-118">O objeto de configuração de IP especifica um endereço IPv4 privado estático.</span><span class="sxs-lookup"><span data-stu-id="b48f1-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="b48f1-119">O primeiro comando recupera uma rede virtual especificada existente usada para atribuir a sub-rede no segundo comando.</span><span class="sxs-lookup"><span data-stu-id="b48f1-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="b48f1-120">O segundo comando cria uma configuração de IP de interface de rede chamada IPConfig1 e armazena a configuração na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="b48f1-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="b48f1-121">O terceiro comando cria uma interface de rede chamada NetworkInterface1 que usa a configuração de IP da interface de rede armazenada na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="b48f1-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="b48f1-122">OS</span><span class="sxs-lookup"><span data-stu-id="b48f1-122">PARAMETERS</span></span>

### <span data-ttu-id="b48f1-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b48f1-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="b48f1-124">Especifica um objeto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="b48f1-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="b48f1-125">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b48f1-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="b48f1-126">Especifica a ID de um objeto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="b48f1-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="b48f1-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b48f1-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="b48f1-128">Especifica uma coleção de referências do grupo de segurança do aplicativo à qual a configuração de IP da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="b48f1-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="b48f1-129">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b48f1-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="b48f1-130">Especifica uma coleção de referências do grupo de segurança do aplicativo à qual a configuração de IP da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="b48f1-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="b48f1-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b48f1-131">-AsJob</span></span>
<span data-ttu-id="b48f1-132">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b48f1-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b48f1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48f1-133">-DefaultProfile</span></span>
<span data-ttu-id="b48f1-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b48f1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b48f1-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="b48f1-135">-DnsServer</span></span>
<span data-ttu-id="b48f1-136">Especifica o servidor DNS para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-136">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="b48f1-137">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="b48f1-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="b48f1-138">Permite a rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="b48f1-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="b48f1-139">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="b48f1-139">-EnableIPForwarding</span></span>
<span data-ttu-id="b48f1-140">Indica que esse cmdlet habilita o encaminhamento de IP para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="b48f1-141">O encaminhamento de IP permite que uma máquina virtual receba tráfego endereçado a outros destinos.</span><span class="sxs-lookup"><span data-stu-id="b48f1-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="b48f1-142">-Force</span><span class="sxs-lookup"><span data-stu-id="b48f1-142">-Force</span></span>
<span data-ttu-id="b48f1-143">Força a criação da interface de rede mesmo que já exista uma interface de rede com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="b48f1-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="b48f1-144">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="b48f1-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="b48f1-145">Especifica o rótulo de nome DNS interno para a nova interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-145">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="b48f1-146">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b48f1-146">-IpConfiguration</span></span>
<span data-ttu-id="b48f1-147">Especifica a configuração de IP que este cmdlet usa para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="b48f1-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b48f1-148">-IpConfigurationName</span></span>
<span data-ttu-id="b48f1-149">Especifica o nome de uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="b48f1-149">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="b48f1-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b48f1-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="b48f1-151">Especifica um objeto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="b48f1-151">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="b48f1-152">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b48f1-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="b48f1-153">Especifica a ID de um objeto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="b48f1-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="b48f1-154">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="b48f1-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="b48f1-155">Especifica uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b48f1-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="b48f1-156">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="b48f1-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="b48f1-157">Especifica a ID de uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b48f1-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="b48f1-158">-Local</span><span class="sxs-lookup"><span data-stu-id="b48f1-158">-Location</span></span>
<span data-ttu-id="b48f1-159">Especifica a região para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-159">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="b48f1-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="b48f1-160">-Name</span></span>
<span data-ttu-id="b48f1-161">Especifica o nome da interface de rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="b48f1-161">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="b48f1-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b48f1-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b48f1-163">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="b48f1-163">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="b48f1-164">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b48f1-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b48f1-165">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-165">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="b48f1-166">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b48f1-166">-PrivateIpAddress</span></span>
<span data-ttu-id="b48f1-167">Especifica um endereço IP IPv4 estático a ser atribuído a essa interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="b48f1-168">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b48f1-168">-PublicIpAddress</span></span>
<span data-ttu-id="b48f1-169">Especifica um objeto **PublicIPAddress** para atribuir a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="b48f1-170">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b48f1-170">-PublicIpAddressId</span></span>
<span data-ttu-id="b48f1-171">Especifica a ID de um objeto **PublicIPAddress** a ser atribuído a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="b48f1-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48f1-172">-ResourceGroupName</span></span>
<span data-ttu-id="b48f1-173">Especifica o nome de um grupo de recursos ao qual a interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="b48f1-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="b48f1-174">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b48f1-174">-Subnet</span></span>
<span data-ttu-id="b48f1-175">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="b48f1-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="b48f1-176">Esse cmdlet cria uma interface de rede para a sub-rede que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b48f1-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="b48f1-177">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="b48f1-177">-SubnetId</span></span>
<span data-ttu-id="b48f1-178">Especifica a ID da sub-rede para a qual criar uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="b48f1-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="b48f1-179">-Marca</span><span class="sxs-lookup"><span data-stu-id="b48f1-179">-Tag</span></span>
<span data-ttu-id="b48f1-180">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b48f1-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b48f1-181">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b48f1-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b48f1-182">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b48f1-182">-Confirm</span></span>
<span data-ttu-id="b48f1-183">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b48f1-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b48f1-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48f1-184">-WhatIf</span></span>
<span data-ttu-id="b48f1-185">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b48f1-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b48f1-186">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b48f1-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b48f1-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48f1-187">CommonParameters</span></span>
<span data-ttu-id="b48f1-188">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b48f1-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48f1-189">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b48f1-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48f1-190">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b48f1-190">INPUTS</span></span>

### <span data-ttu-id="b48f1-191">System. String</span><span class="sxs-lookup"><span data-stu-id="b48f1-191">System.String</span></span>

### <span data-ttu-id="b48f1-192">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b48f1-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="b48f1-193">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b48f1-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b48f1-194">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b48f1-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="b48f1-195">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b48f1-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="b48f1-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="b48f1-196">System.String[]</span></span>

### <span data-ttu-id="b48f1-197">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="b48f1-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="b48f1-198">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="b48f1-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="b48f1-199">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="b48f1-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="b48f1-200">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="b48f1-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="b48f1-201">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b48f1-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b48f1-202">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b48f1-202">OUTPUTS</span></span>

### <span data-ttu-id="b48f1-203">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b48f1-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b48f1-204">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b48f1-204">NOTES</span></span>

## <span data-ttu-id="b48f1-205">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b48f1-205">RELATED LINKS</span></span>

[<span data-ttu-id="b48f1-206">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b48f1-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="b48f1-207">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b48f1-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="b48f1-208">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b48f1-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
