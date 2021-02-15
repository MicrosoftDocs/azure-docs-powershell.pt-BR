---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117393"
---
# <span data-ttu-id="a7711-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a7711-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="a7711-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7711-102">SYNOPSIS</span></span>
<span data-ttu-id="a7711-103">Cria uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-103">Creates a network interface.</span></span>

## <span data-ttu-id="a7711-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7711-104">SYNTAX</span></span>

### <span data-ttu-id="a7711-105">SetByIpConfigurationResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7711-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7711-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a7711-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7711-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7711-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7711-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a7711-108">SetByResource</span></span>
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

## <span data-ttu-id="a7711-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7711-109">DESCRIPTION</span></span>
<span data-ttu-id="a7711-110">O **cmdlet New-AzNetworkInterface** cria uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="a7711-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="a7711-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7711-111">EXAMPLES</span></span>

### <span data-ttu-id="a7711-112">Exemplo 1: Criar uma interface de rede do Azure</span><span class="sxs-lookup"><span data-stu-id="a7711-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="a7711-113">Esse comando cria uma interface de rede chamada NetworkInterface001 com um endereço IP privado atribuído dinamicamente a partir da Sub-rede1 na rede virtual chamada VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="a7711-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="a7711-114">O comando também atribui dois servidores DNS à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="a7711-115">O recurso filho IPConfiguration será criado automaticamente usando o nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="a7711-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="a7711-116">Exemplo 2: Criar uma interface de rede do Azure usando um objeto de configuração IP</span><span class="sxs-lookup"><span data-stu-id="a7711-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="a7711-117">Este exemplo cria uma nova interface de rede usando um objeto de configuração IP.</span><span class="sxs-lookup"><span data-stu-id="a7711-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="a7711-118">O objeto de configuração IP especifica um endereço IPv4 particular estático.</span><span class="sxs-lookup"><span data-stu-id="a7711-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="a7711-119">O primeiro comando recupera uma rede virtual especificada existente usada para atribuir a sub-rede no segundo comando.</span><span class="sxs-lookup"><span data-stu-id="a7711-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="a7711-120">O segundo comando cria uma configuração IP de interface de rede chamada IPConfig1 e armazena a configuração na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="a7711-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="a7711-121">O terceiro comando cria uma interface de rede chamada NetworkInterface1 que usa a configuração IP da interface de rede armazenada na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="a7711-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="a7711-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a7711-122">Example 3</span></span>

<span data-ttu-id="a7711-123">Cria uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-123">Creates a network interface.</span></span> <span data-ttu-id="a7711-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="a7711-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="a7711-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7711-125">PARAMETERS</span></span>

### <span data-ttu-id="a7711-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a7711-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="a7711-127">Especifica um **objeto ApplicationGatewayBackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="a7711-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a7711-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a7711-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="a7711-129">Especifica a ID de um objeto **ApplicationGatewayBackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="a7711-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a7711-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a7711-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="a7711-131">Especifica um conjunto de referências de grupo de segurança de aplicativos às quais a configuração ip da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="a7711-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="a7711-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a7711-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="a7711-133">Especifica um conjunto de referências de grupo de segurança de aplicativos às quais a configuração ip da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="a7711-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="a7711-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7711-134">-AsJob</span></span>
<span data-ttu-id="a7711-135">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a7711-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7711-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7711-136">-DefaultProfile</span></span>
<span data-ttu-id="a7711-137">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a7711-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7711-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="a7711-138">-DnsServer</span></span>
<span data-ttu-id="a7711-139">Especifica o servidor DNS para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="a7711-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="a7711-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="a7711-141">Habilita a rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="a7711-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="a7711-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a7711-142">-EnableIPForwarding</span></span>
<span data-ttu-id="a7711-143">Indica que esse cmdlet habilita o encaminhamento de IP para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="a7711-144">O encaminhamento de IP permite que uma máquina virtual receba tráfego endereçado a outros destinos.</span><span class="sxs-lookup"><span data-stu-id="a7711-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="a7711-145">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a7711-145">-Force</span></span>
<span data-ttu-id="a7711-146">Força a criação da interface de rede mesmo que já exista uma interface de rede com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a7711-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="a7711-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="a7711-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="a7711-148">Especifica o rótulo de nome DNS interno para a nova interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="a7711-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7711-149">-IpConfiguration</span></span>
<span data-ttu-id="a7711-150">Especifica a configuração IP que esse cmdlet usa para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="a7711-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a7711-151">-IpConfigurationName</span></span>
<span data-ttu-id="a7711-152">Especifica o nome de uma configuração IP.</span><span class="sxs-lookup"><span data-stu-id="a7711-152">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="a7711-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a7711-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="a7711-154">Especifica um **objeto BackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="a7711-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a7711-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a7711-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="a7711-156">Especifica a ID de um objeto **BackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="a7711-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a7711-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a7711-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="a7711-158">Especifica uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a7711-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="a7711-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="a7711-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="a7711-160">Especifica a ID de uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a7711-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="a7711-161">-Local</span><span class="sxs-lookup"><span data-stu-id="a7711-161">-Location</span></span>
<span data-ttu-id="a7711-162">Especifica a região de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="a7711-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7711-163">-Name</span></span>
<span data-ttu-id="a7711-164">Especifica o nome da interface de rede a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a7711-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="a7711-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a7711-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a7711-166">Especifica um objeto **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="a7711-166">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="a7711-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a7711-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a7711-168">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-168">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="a7711-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7711-169">-PrivateIpAddress</span></span>
<span data-ttu-id="a7711-170">Especifica um endereço IP IPv4 estático para atribuir a esta interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="a7711-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7711-171">-PublicIpAddress</span></span>
<span data-ttu-id="a7711-172">Especifica um objeto **PublicIPAddress** a ser atribuído a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="a7711-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a7711-173">-PublicIpAddressId</span></span>
<span data-ttu-id="a7711-174">Especifica a ID de um objeto **PublicIPAddress** a ser atribuído a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="a7711-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7711-175">-ResourceGroupName</span></span>
<span data-ttu-id="a7711-176">Especifica o nome de um grupo de recursos ao que a interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="a7711-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="a7711-177">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="a7711-177">-Subnet</span></span>
<span data-ttu-id="a7711-178">Especifica um **objeto de Sub-rede.**</span><span class="sxs-lookup"><span data-stu-id="a7711-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="a7711-179">Esse cmdlet cria uma interface de rede para a sub-rede especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a7711-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7711-180">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="a7711-180">-SubnetId</span></span>
<span data-ttu-id="a7711-181">Especifica a ID da sub-rede para a qual criar uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a7711-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="a7711-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7711-182">-Tag</span></span>
<span data-ttu-id="a7711-183">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a7711-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a7711-184">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a7711-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a7711-185">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a7711-185">-Confirm</span></span>
<span data-ttu-id="a7711-186">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7711-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7711-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7711-187">-WhatIf</span></span>
<span data-ttu-id="a7711-188">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a7711-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7711-189">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7711-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7711-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7711-190">CommonParameters</span></span>
<span data-ttu-id="a7711-191">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7711-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7711-192">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7711-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7711-193">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7711-193">INPUTS</span></span>

### <span data-ttu-id="a7711-194">System.String</span><span class="sxs-lookup"><span data-stu-id="a7711-194">System.String</span></span>

### <span data-ttu-id="a7711-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="a7711-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="a7711-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a7711-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="a7711-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7711-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="a7711-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a7711-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="a7711-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a7711-199">System.String[]</span></span>

### <span data-ttu-id="a7711-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="a7711-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="a7711-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="a7711-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="a7711-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="a7711-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="a7711-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="a7711-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="a7711-204">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a7711-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a7711-205">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7711-205">OUTPUTS</span></span>

### <span data-ttu-id="a7711-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a7711-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a7711-207">Notas</span><span class="sxs-lookup"><span data-stu-id="a7711-207">NOTES</span></span>

## <span data-ttu-id="a7711-208">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7711-208">RELATED LINKS</span></span>

[<span data-ttu-id="a7711-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a7711-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="a7711-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a7711-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="a7711-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a7711-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
