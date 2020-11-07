---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1ef34f3770d4eba273a679de2914184c3bf411a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940654"
---
# <span data-ttu-id="34c97-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34c97-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="34c97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34c97-102">SYNOPSIS</span></span>
<span data-ttu-id="34c97-103">Atualiza uma configuração de sub-rede para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="34c97-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="34c97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34c97-104">SYNTAX</span></span>

### <span data-ttu-id="34c97-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="34c97-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34c97-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="34c97-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34c97-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34c97-107">DESCRIPTION</span></span>
<span data-ttu-id="34c97-108">O cmdlet **set-AzVirtualNetworkSubnetConfig** atualiza uma configuração de sub-rede para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="34c97-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="34c97-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34c97-109">EXAMPLES</span></span>

### <span data-ttu-id="34c97-110">1: modificar o prefixo do endereço de uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="34c97-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="34c97-111">Este exemplo cria uma rede virtual com uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="34c97-112">Em seguida, chama-se Set-AzVirtualNetworkSubnetConfig de modificar o AddressPrefix da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="34c97-113">Isso afeta apenas a representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="34c97-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="34c97-114">Set-AzVirtualNetwork, em seguida, é chamado para modificar a rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="34c97-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="34c97-115">2: adicionar um grupo de segurança de rede a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="34c97-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="34c97-116">Este exemplo cria um grupo de recursos com uma rede virtual contendo apenas uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="34c97-117">Em seguida, ele cria um grupo de segurança de rede com uma regra de permissão para tráfego RDP.</span><span class="sxs-lookup"><span data-stu-id="34c97-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="34c97-118">O cmdlet Set-AzVirtualNetworkSubnetConfig é usado para modificar a representação na memória da sub-rede de front-end para que ele aponte para o grupo de segurança de rede recém-criado.</span><span class="sxs-lookup"><span data-stu-id="34c97-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="34c97-119">O cmdlet Set-AzVirtualNetwork, em seguida, chamado para gravar o estado modificado novamente para o serviço.</span><span class="sxs-lookup"><span data-stu-id="34c97-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="34c97-120">3: anexar um gateway NAT a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="34c97-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="34c97-121">OS</span><span class="sxs-lookup"><span data-stu-id="34c97-121">PARAMETERS</span></span>

### <span data-ttu-id="34c97-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="34c97-122">-AddressPrefix</span></span>
<span data-ttu-id="34c97-123">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="34c97-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c97-124">-DefaultProfile</span></span>
<span data-ttu-id="34c97-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34c97-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34c97-126">-Delegation</span><span class="sxs-lookup"><span data-stu-id="34c97-126">-Delegation</span></span>
<span data-ttu-id="34c97-127">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="34c97-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34c97-128">-InputObject</span></span>
<span data-ttu-id="34c97-129">Especifica o gateway NAT associado à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="34c97-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="34c97-130">-Name</span></span>
<span data-ttu-id="34c97-131">Especifica o nome de uma configuração de sub-rede que este cmdlet configura.</span><span class="sxs-lookup"><span data-stu-id="34c97-131">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="34c97-132">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="34c97-132">-NetworkSecurityGroup</span></span>
<span data-ttu-id="34c97-133">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="34c97-133">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="34c97-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="34c97-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="34c97-135">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="34c97-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="34c97-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="34c97-137">Configure para habilitar ou desabilitar a aplicação de políticas de rede em um ponto de extremidade privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="34c97-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="34c97-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="34c97-139">Configure para habilitar ou desabilitar a aplicação de políticas de rede no serviço de link privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="34c97-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34c97-140">-ResourceId</span></span>
<span data-ttu-id="34c97-141">Especifica a ID do recurso de gateway NAT associado à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="34c97-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="34c97-142">-RouteTable</span></span>
<span data-ttu-id="34c97-143">Especifica o objeto da tabela de rota que está associado ao grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-143">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="34c97-144">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="34c97-144">-RouteTableId</span></span>
<span data-ttu-id="34c97-145">Especifica a ID do objeto da tabela de rota que está associado ao grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-145">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="34c97-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="34c97-146">-ServiceEndpoint</span></span>
<span data-ttu-id="34c97-147">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="34c97-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="34c97-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="34c97-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="34c97-149">Políticas de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="34c97-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="34c97-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34c97-150">-VirtualNetwork</span></span>
<span data-ttu-id="34c97-151">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="34c97-151">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="34c97-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c97-152">CommonParameters</span></span>
<span data-ttu-id="34c97-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c97-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c97-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34c97-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c97-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34c97-155">INPUTS</span></span>

### <span data-ttu-id="34c97-156">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34c97-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="34c97-157">System. String</span><span class="sxs-lookup"><span data-stu-id="34c97-157">System.String</span></span>

### <span data-ttu-id="34c97-158">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="34c97-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="34c97-159">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="34c97-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="34c97-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="34c97-160">System.String[]</span></span>

### <span data-ttu-id="34c97-161">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="34c97-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="34c97-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="34c97-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="34c97-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34c97-163">OUTPUTS</span></span>

### <span data-ttu-id="34c97-164">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34c97-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="34c97-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34c97-165">NOTES</span></span>

## <span data-ttu-id="34c97-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34c97-166">RELATED LINKS</span></span>

[<span data-ttu-id="34c97-167">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34c97-167">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="34c97-168">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34c97-168">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="34c97-169">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34c97-169">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="34c97-170">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="34c97-170">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
