---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 47c56f2f55a07dc2567ca3ee2030e075d90dc324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885389"
---
# <span data-ttu-id="e5bf3-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e5bf3-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="e5bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="e5bf3-103">Atualiza uma configuração de sub-rede para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="e5bf3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e5bf3-104">SYNTAX</span></span>

### <span data-ttu-id="e5bf3-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e5bf3-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5bf3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5bf3-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5bf3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5bf3-107">DESCRIPTION</span></span>
<span data-ttu-id="e5bf3-108">O cmdlet **Set-AzVirtualNetworkSubnetConfig** atualiza uma configuração de sub-rede para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="e5bf3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5bf3-109">EXAMPLES</span></span>

### <span data-ttu-id="e5bf3-110">1: Modificar o prefixo de endereço de uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="e5bf3-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="e5bf3-111">Este exemplo cria uma rede virtual com uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="e5bf3-112">Em seguida, Set-AzVirtualNetworkSubnetConfig para modificar o AddressPrefix da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="e5bf3-113">Isso afeta apenas a representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="e5bf3-114">Set-AzVirtualNetwork então é chamado para modificar a rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="e5bf3-115">2: Adicionar um grupo de segurança de rede a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="e5bf3-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="e5bf3-116">Este exemplo cria um grupo de recursos com uma rede virtual contendo apenas uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="e5bf3-117">Em seguida, ele cria um grupo de segurança de rede com uma regra de autorização para tráfego RDP.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="e5bf3-118">O Set-AzVirtualNetworkSubnetConfig cmdlet é usado para modificar a representação na memória da sub-rede frontend para que ele aponta para o grupo de segurança de rede recém-criado.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="e5bf3-119">O Set-AzVirtualNetwork cmdlet é chamado para gravar o estado modificado de volta ao serviço.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="e5bf3-120">3: Anexar um Gateway Nat a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="e5bf3-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="e5bf3-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e5bf3-121">PARAMETERS</span></span>

### <span data-ttu-id="e5bf3-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e5bf3-122">-AddressPrefix</span></span>
<span data-ttu-id="e5bf3-123">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5bf3-124">-DefaultProfile</span></span>
<span data-ttu-id="e5bf3-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5bf3-126">-Delegation</span><span class="sxs-lookup"><span data-stu-id="e5bf3-126">-Delegation</span></span>
<span data-ttu-id="e5bf3-127">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-127">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5bf3-128">-InputObject</span></span>
<span data-ttu-id="e5bf3-129">Especifica o gateway nat associado à configuração da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="e5bf3-130">-IpAllocation</span></span>
<span data-ttu-id="e5bf3-131">Especifica IpAllocations para uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-131">Specifies IpAllocations for a subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e5bf3-132">-Name</span></span>
<span data-ttu-id="e5bf3-133">Especifica o nome de uma configuração de sub-rede que este cmdlet configura.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="e5bf3-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5bf3-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e5bf3-135">Especifica um **objeto NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="e5bf3-135">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e5bf3-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e5bf3-137">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="e5bf3-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="e5bf3-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="e5bf3-139">Configure para habilitar ou desabilitar a aplicação de políticas de rede no ponto de extremidade privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="e5bf3-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="e5bf3-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="e5bf3-141">Configure para habilitar ou desabilitar a aplicação de políticas de rede no serviço de link privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="e5bf3-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5bf3-142">-ResourceId</span></span>
<span data-ttu-id="e5bf3-143">Especifica a ID do recurso gateway NAT associado à configuração da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e5bf3-144">-RouteTable</span></span>
<span data-ttu-id="e5bf3-145">Especifica o objeto de tabela de rota associado ao grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-145">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="e5bf3-146">-RouteTableId</span></span>
<span data-ttu-id="e5bf3-147">Especifica a ID do objeto de tabela de rota associado ao grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="e5bf3-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5bf3-148">-ServiceEndpoint</span></span>
<span data-ttu-id="e5bf3-149">Valor do Ponto de Extremidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="e5bf3-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="e5bf3-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e5bf3-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e5bf3-151">Políticas de Ponto de Extremidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="e5bf3-151">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e5bf3-152">-VirtualNetwork</span></span>
<span data-ttu-id="e5bf3-153">Especifica o **objeto VirtualNetwork** que contém a configuração da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5bf3-154">CommonParameters</span></span>
<span data-ttu-id="e5bf3-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5bf3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5bf3-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5bf3-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5bf3-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5bf3-157">INPUTS</span></span>

### <span data-ttu-id="e5bf3-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e5bf3-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="e5bf3-159">System.String</span><span class="sxs-lookup"><span data-stu-id="e5bf3-159">System.String</span></span>

### <span data-ttu-id="e5bf3-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5bf3-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="e5bf3-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e5bf3-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e5bf3-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e5bf3-162">System.String[]</span></span>

### <span data-ttu-id="e5bf3-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="e5bf3-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="e5bf3-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span><span class="sxs-lookup"><span data-stu-id="e5bf3-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="e5bf3-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e5bf3-165">OUTPUTS</span></span>

### <span data-ttu-id="e5bf3-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e5bf3-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e5bf3-167">NOTES</span><span class="sxs-lookup"><span data-stu-id="e5bf3-167">NOTES</span></span>

## <span data-ttu-id="e5bf3-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5bf3-168">RELATED LINKS</span></span>

[<span data-ttu-id="e5bf3-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e5bf3-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e5bf3-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e5bf3-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e5bf3-171">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e5bf3-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e5bf3-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e5bf3-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
