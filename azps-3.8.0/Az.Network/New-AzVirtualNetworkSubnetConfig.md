---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 144d04172f3169075a32c5e8111a90ff407532b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943229"
---
# <span data-ttu-id="20c44-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20c44-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="20c44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20c44-102">SYNOPSIS</span></span>
<span data-ttu-id="20c44-103">Cria uma configuração de sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20c44-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="20c44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20c44-104">SYNTAX</span></span>

### <span data-ttu-id="20c44-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="20c44-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20c44-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="20c44-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c44-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20c44-107">DESCRIPTION</span></span>
<span data-ttu-id="20c44-108">**O cmdlet New-AzVirtualNetworkSubnetConfig** cria uma configuração de sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20c44-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="20c44-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20c44-109">EXAMPLES</span></span>

### <span data-ttu-id="20c44-110">1: criar uma rede virtual com duas sub-redes e um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="20c44-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
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

<span data-ttu-id="20c44-111">Este exemplo cria duas novas configurações de sub-rede usando o cmdlet New-AzVirtualSubnetConfig e, em seguida, as usa para criar uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20c44-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="20c44-112">O modelo New-AzVirtualSubnetConfig cria apenas uma representação na memória da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="20c44-113">Neste exemplo, o frontendSubnet tem CIDR 10.0.1.0/24 e faz referência a um grupo de segurança de rede que permite acesso ao RDP.</span><span class="sxs-lookup"><span data-stu-id="20c44-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="20c44-114">O backendSubnet tem 10.0.2.0/24 CIDR e faz referência ao mesmo grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="20c44-115">OS</span><span class="sxs-lookup"><span data-stu-id="20c44-115">PARAMETERS</span></span>

### <span data-ttu-id="20c44-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="20c44-116">-AddressPrefix</span></span>
<span data-ttu-id="20c44-117">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="20c44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c44-118">-DefaultProfile</span></span>
<span data-ttu-id="20c44-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20c44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20c44-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="20c44-120">-Delegation</span></span>
<span data-ttu-id="20c44-121">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="20c44-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20c44-122">-InputObject</span></span>
<span data-ttu-id="20c44-123">Especifica o gateway NAT associado à configuração de sub-rede</span><span class="sxs-lookup"><span data-stu-id="20c44-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="20c44-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="20c44-124">-Name</span></span>
<span data-ttu-id="20c44-125">Especifica o nome da configuração de sub-rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="20c44-125">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="20c44-126">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20c44-126">-NetworkSecurityGroup</span></span>
<span data-ttu-id="20c44-127">Especifica um objeto NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="20c44-127">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="20c44-128">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="20c44-128">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="20c44-129">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-129">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="20c44-130">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="20c44-130">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="20c44-131">Configure para habilitar ou desabilitar a aplicação de políticas de rede em um ponto de extremidade privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-131">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="20c44-132">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="20c44-132">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="20c44-133">Configure para habilitar ou desabilitar a aplicação de políticas de rede no serviço de link privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-133">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="20c44-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20c44-134">-ResourceId</span></span>
<span data-ttu-id="20c44-135">Especifica a ID do recurso de gateway NAT associado à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-135">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="20c44-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="20c44-136">-RouteTable</span></span>
<span data-ttu-id="20c44-137">Especifica a tabela de rota associada à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-137">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="20c44-138">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="20c44-138">-RouteTableId</span></span>
<span data-ttu-id="20c44-139">Especifica a ID da tabela de rota associada à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="20c44-139">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="20c44-140">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="20c44-140">-ServiceEndpoint</span></span>
<span data-ttu-id="20c44-141">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="20c44-141">Service Endpoint Value</span></span>

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

### <span data-ttu-id="20c44-142">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="20c44-142">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="20c44-143">Políticas de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="20c44-143">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="20c44-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c44-144">CommonParameters</span></span>
<span data-ttu-id="20c44-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c44-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c44-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20c44-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c44-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20c44-147">INPUTS</span></span>

### <span data-ttu-id="20c44-148">System. String</span><span class="sxs-lookup"><span data-stu-id="20c44-148">System.String</span></span>

### <span data-ttu-id="20c44-149">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20c44-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="20c44-150">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="20c44-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="20c44-151">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="20c44-151">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="20c44-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="20c44-152">System.String[]</span></span>

### <span data-ttu-id="20c44-153">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="20c44-153">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="20c44-154">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="20c44-154">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="20c44-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20c44-155">OUTPUTS</span></span>

### <span data-ttu-id="20c44-156">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="20c44-156">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="20c44-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20c44-157">NOTES</span></span>

## <span data-ttu-id="20c44-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20c44-158">RELATED LINKS</span></span>

[<span data-ttu-id="20c44-159">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20c44-159">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="20c44-160">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20c44-160">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="20c44-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20c44-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="20c44-162">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20c44-162">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
