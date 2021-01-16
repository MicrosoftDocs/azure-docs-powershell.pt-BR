---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263011"
---
# <span data-ttu-id="4517f-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4517f-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4517f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4517f-102">SYNOPSIS</span></span>
<span data-ttu-id="4517f-103">Cria uma configuração de sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4517f-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="4517f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4517f-104">SYNTAX</span></span>

### <span data-ttu-id="4517f-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="4517f-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4517f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4517f-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4517f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4517f-107">DESCRIPTION</span></span>
<span data-ttu-id="4517f-108">**O cmdlet New-AzVirtualNetworkSubnetConfig** cria uma configuração de sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4517f-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="4517f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4517f-109">EXAMPLES</span></span>

### <span data-ttu-id="4517f-110">Exemplo 1: criar uma rede virtual com duas sub-redes e um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4517f-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="4517f-111">Este exemplo cria duas novas configurações de sub-rede usando o cmdlet New-AzVirtualSubnetConfig e, em seguida, as usa para criar uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4517f-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="4517f-112">O modelo New-AzVirtualSubnetConfig cria apenas uma representação na memória da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="4517f-113">Neste exemplo, o frontendSubnet tem CIDR 10.0.1.0/24 e faz referência a um grupo de segurança de rede que permite acesso ao RDP.</span><span class="sxs-lookup"><span data-stu-id="4517f-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="4517f-114">O backendSubnet tem 10.0.2.0/24 CIDR e faz referência ao mesmo grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="4517f-115">OS</span><span class="sxs-lookup"><span data-stu-id="4517f-115">PARAMETERS</span></span>

### <span data-ttu-id="4517f-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4517f-116">-AddressPrefix</span></span>
<span data-ttu-id="4517f-117">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="4517f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4517f-118">-DefaultProfile</span></span>
<span data-ttu-id="4517f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4517f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4517f-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="4517f-120">-Delegation</span></span>
<span data-ttu-id="4517f-121">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="4517f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4517f-122">-InputObject</span></span>
<span data-ttu-id="4517f-123">Especifica o gateway NAT associado à configuração de sub-rede</span><span class="sxs-lookup"><span data-stu-id="4517f-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="4517f-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="4517f-124">-IpAllocation</span></span>
<span data-ttu-id="4517f-125">Especifica IpAllocations para uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="4517f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4517f-126">-Name</span></span>
<span data-ttu-id="4517f-127">Especifica o nome da configuração de sub-rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="4517f-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="4517f-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4517f-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4517f-129">Especifica um objeto NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="4517f-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="4517f-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4517f-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="4517f-131">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="4517f-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="4517f-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="4517f-133">Configure para habilitar ou desabilitar a aplicação de políticas de rede em um ponto de extremidade privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="4517f-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="4517f-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="4517f-135">Configure para habilitar ou desabilitar a aplicação de políticas de rede no serviço de link privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="4517f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4517f-136">-ResourceId</span></span>
<span data-ttu-id="4517f-137">Especifica a ID do recurso de gateway NAT associado à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="4517f-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4517f-138">-RouteTable</span></span>
<span data-ttu-id="4517f-139">Especifica a tabela de rota associada à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="4517f-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="4517f-140">-RouteTableId</span></span>
<span data-ttu-id="4517f-141">Especifica a ID da tabela de rota associada à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4517f-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="4517f-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4517f-142">-ServiceEndpoint</span></span>
<span data-ttu-id="4517f-143">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="4517f-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="4517f-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4517f-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4517f-145">Políticas de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="4517f-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="4517f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4517f-146">CommonParameters</span></span>
<span data-ttu-id="4517f-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4517f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4517f-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4517f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4517f-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4517f-149">INPUTS</span></span>

### <span data-ttu-id="4517f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4517f-150">System.String</span></span>

### <span data-ttu-id="4517f-151">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4517f-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="4517f-152">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4517f-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="4517f-153">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="4517f-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="4517f-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="4517f-154">System.String[]</span></span>

### <span data-ttu-id="4517f-155">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="4517f-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="4517f-156">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="4517f-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="4517f-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4517f-157">OUTPUTS</span></span>

### <span data-ttu-id="4517f-158">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4517f-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="4517f-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4517f-159">NOTES</span></span>

## <span data-ttu-id="4517f-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4517f-160">RELATED LINKS</span></span>

[<span data-ttu-id="4517f-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4517f-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4517f-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4517f-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4517f-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4517f-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4517f-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4517f-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
