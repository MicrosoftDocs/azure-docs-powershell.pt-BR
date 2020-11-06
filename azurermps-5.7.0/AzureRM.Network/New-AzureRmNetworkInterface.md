---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 111723b2f0271583d43bd1c845eebe9800190a59
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441596"
---
# <span data-ttu-id="a0675-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0675-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="a0675-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0675-102">SYNOPSIS</span></span>
<span data-ttu-id="a0675-103">Cria uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0675-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0675-104">SYNTAX</span></span>

### <span data-ttu-id="a0675-105">SetByIpConfigurationResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0675-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0675-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a0675-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0675-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0675-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0675-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a0675-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
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

## <span data-ttu-id="a0675-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0675-109">DESCRIPTION</span></span>
<span data-ttu-id="a0675-110">O cmdlet **New-AzureRmNetworkInterface** cria uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0675-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="a0675-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0675-111">EXAMPLES</span></span>

### <span data-ttu-id="a0675-112">Exemplo 1: criar uma interface de rede do Azure</span><span class="sxs-lookup"><span data-stu-id="a0675-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="a0675-113">Esse comando cria uma interface de rede chamada NetworkInterface001 com um endereço IP particular atribuído dinamicamente do Subnet1 na rede virtual chamada VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="a0675-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="a0675-114">O comando também atribui dois servidores DNS à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="a0675-115">O recurso filho da IPConfiguration será criado automaticamente usando o nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="a0675-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="a0675-116">Exemplo 2: criar uma interface de rede do Azure usando um objeto de configuração de IP</span><span class="sxs-lookup"><span data-stu-id="a0675-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="a0675-117">Este exemplo cria uma nova interface de rede usando um objeto de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="a0675-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="a0675-118">O objeto de configuração de IP especifica um endereço IPv4 privado estático.</span><span class="sxs-lookup"><span data-stu-id="a0675-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="a0675-119">O primeiro comando cria uma configuração de IP de interface de rede chamada IPConfig1 e armazena a configuração na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="a0675-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="a0675-120">O segundo comando cria uma interface de rede chamada NetworkInterface1 que usa a configuração de IP da interface de rede armazenada na variável chamada $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="a0675-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="a0675-121">OS</span><span class="sxs-lookup"><span data-stu-id="a0675-121">PARAMETERS</span></span>

### <span data-ttu-id="a0675-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a0675-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="a0675-123">Especifica um objeto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="a0675-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a0675-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a0675-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="a0675-125">Especifica a ID de um objeto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="a0675-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a0675-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a0675-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="a0675-127">Especifica uma coleção de referências do grupo de segurança do aplicativo à qual a configuração de IP da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="a0675-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="a0675-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a0675-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="a0675-129">Especifica uma coleção de referências do grupo de segurança do aplicativo à qual a configuração de IP da interface de rede deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="a0675-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="a0675-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0675-130">-AsJob</span></span>
<span data-ttu-id="a0675-131">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a0675-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0675-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0675-132">-DefaultProfile</span></span>
<span data-ttu-id="a0675-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0675-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0675-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="a0675-134">-DnsServer</span></span>
<span data-ttu-id="a0675-135">Especifica o servidor DNS para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="a0675-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="a0675-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="a0675-137">Permite a rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="a0675-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="a0675-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a0675-138">-EnableIPForwarding</span></span>
<span data-ttu-id="a0675-139">Indica que esse cmdlet habilita o encaminhamento de IP para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="a0675-140">O encaminhamento de IP permite que uma máquina virtual receba tráfego endereçado a outros destinos.</span><span class="sxs-lookup"><span data-stu-id="a0675-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="a0675-141">-Force</span><span class="sxs-lookup"><span data-stu-id="a0675-141">-Force</span></span>
<span data-ttu-id="a0675-142">Força a criação da interface de rede mesmo que já exista uma interface de rede com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a0675-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="a0675-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="a0675-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="a0675-144">Especifica o rótulo de nome DNS interno para a nova interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-144">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="a0675-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0675-145">-IpConfiguration</span></span>
<span data-ttu-id="a0675-146">Especifica a configuração de IP que este cmdlet usa para a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="a0675-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a0675-147">-IpConfigurationName</span></span>
<span data-ttu-id="a0675-148">Especifica o nome de uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="a0675-148">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="a0675-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a0675-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="a0675-150">Especifica um objeto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="a0675-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a0675-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a0675-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="a0675-152">Especifica a ID de um objeto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="a0675-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="a0675-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a0675-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="a0675-154">Especifica uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a0675-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="a0675-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="a0675-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="a0675-156">Especifica a ID de uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="a0675-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="a0675-157">-Local</span><span class="sxs-lookup"><span data-stu-id="a0675-157">-Location</span></span>
<span data-ttu-id="a0675-158">Especifica a região para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-158">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="a0675-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0675-159">-Name</span></span>
<span data-ttu-id="a0675-160">Especifica o nome da interface de rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="a0675-160">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="a0675-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a0675-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a0675-162">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="a0675-162">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="a0675-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a0675-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a0675-164">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-164">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="a0675-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a0675-165">-PrivateIpAddress</span></span>
<span data-ttu-id="a0675-166">Especifica um endereço IP IPv4 estático a ser atribuído a essa interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="a0675-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a0675-167">-PublicIpAddress</span></span>
<span data-ttu-id="a0675-168">Especifica um objeto **PublicIPAddress** para atribuir a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="a0675-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a0675-169">-PublicIpAddressId</span></span>
<span data-ttu-id="a0675-170">Especifica a ID de um objeto **PublicIPAddress** a ser atribuído a uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="a0675-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0675-171">-ResourceGroupName</span></span>
<span data-ttu-id="a0675-172">Especifica o nome de um grupo de recursos ao qual a interface de rede pertence.</span><span class="sxs-lookup"><span data-stu-id="a0675-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="a0675-173">-Subnet</span><span class="sxs-lookup"><span data-stu-id="a0675-173">-Subnet</span></span>
<span data-ttu-id="a0675-174">Especifica um objeto de **sub-rede** .</span><span class="sxs-lookup"><span data-stu-id="a0675-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="a0675-175">Esse cmdlet cria uma interface de rede para a sub-rede que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a0675-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0675-176">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="a0675-176">-SubnetId</span></span>
<span data-ttu-id="a0675-177">Especifica a ID da sub-rede para a qual criar uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a0675-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="a0675-178">-Marca</span><span class="sxs-lookup"><span data-stu-id="a0675-178">-Tag</span></span>
<span data-ttu-id="a0675-179">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a0675-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a0675-180">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a0675-180">For example:</span></span>

<span data-ttu-id="a0675-181">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a0675-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a0675-182">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0675-182">-Confirm</span></span>
<span data-ttu-id="a0675-183">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0675-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0675-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0675-184">-WhatIf</span></span>
<span data-ttu-id="a0675-185">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0675-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0675-186">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0675-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0675-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0675-187">CommonParameters</span></span>
<span data-ttu-id="a0675-188">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0675-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0675-189">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0675-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0675-190">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0675-190">INPUTS</span></span>

### <span data-ttu-id="a0675-191">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a0675-191">None</span></span>
<span data-ttu-id="a0675-192">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a0675-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0675-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0675-193">OUTPUTS</span></span>

### <span data-ttu-id="a0675-194">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0675-194">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a0675-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0675-195">NOTES</span></span>

## <span data-ttu-id="a0675-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0675-196">RELATED LINKS</span></span>

[<span data-ttu-id="a0675-197">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0675-197">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="a0675-198">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0675-198">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="a0675-199">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0675-199">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
