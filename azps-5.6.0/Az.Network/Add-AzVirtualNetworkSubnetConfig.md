---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4c206bfe4681bfdc1cb622ec90170776e5528ebe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888852"
---
# <span data-ttu-id="6ae1b-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6ae1b-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="6ae1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ae1b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae1b-103">Adiciona uma configuração de sub-rede a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="6ae1b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6ae1b-104">SYNTAX</span></span>

### <span data-ttu-id="6ae1b-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6ae1b-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ae1b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ae1b-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ae1b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6ae1b-107">DESCRIPTION</span></span>
<span data-ttu-id="6ae1b-108">O cmdlet **Add-AzVirtualNetworkSubnetConfig** adiciona uma configuração de sub-rede a uma rede virtual existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="6ae1b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ae1b-109">EXAMPLES</span></span>

### <span data-ttu-id="6ae1b-110">Exemplo 1: Adicionar uma sub-rede a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="6ae1b-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="6ae1b-111">Este exemplo primeiro cria um grupo de recursos como um contêiner dos recursos a serem criados.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="6ae1b-112">Em seguida, ele cria uma configuração de sub-rede e a usa para criar uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="6ae1b-113">O Add-AzVirtualNetworkSubnetConfig é usado para adicionar uma sub-rede à representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="6ae1b-114">O Set-AzVirtualNetwork atualiza a rede virtual existente com a nova sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="6ae1b-115">Exemplo 2: Adicionar uma delegação a uma sub-rede que está sendo adicionada a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="6ae1b-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="6ae1b-116">Este exemplo primeiro obtém uma vnet existente.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="6ae1b-117">Em seguida, ele cria um objeto de delegação na memória.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="6ae1b-118">Por fim, ele cria uma nova sub-rede com essa delegação adicionada à vnet.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="6ae1b-119">Em seguida, a configuração modificada é enviada para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="6ae1b-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6ae1b-120">PARAMETERS</span></span>

### <span data-ttu-id="6ae1b-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6ae1b-121">-AddressPrefix</span></span>
<span data-ttu-id="6ae1b-122">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="6ae1b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae1b-123">-DefaultProfile</span></span>
<span data-ttu-id="6ae1b-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ae1b-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="6ae1b-125">-Delegation</span></span>
<span data-ttu-id="6ae1b-126">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="6ae1b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ae1b-127">-InputObject</span></span>
<span data-ttu-id="6ae1b-128">Especifica o gateway nat associado à configuração da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="6ae1b-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="6ae1b-129">-IpAllocation</span></span>
<span data-ttu-id="6ae1b-130">Especifica IpAllocations para uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="6ae1b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6ae1b-131">-Name</span></span>
<span data-ttu-id="6ae1b-132">Especifica o nome da configuração da sub-rede a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="6ae1b-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6ae1b-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="6ae1b-134">Especifica um **objeto NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="6ae1b-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="6ae1b-135">Este cmdlet adiciona uma configuração de sub-rede de rede virtual ao objeto especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ae1b-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6ae1b-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="6ae1b-137">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="6ae1b-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="6ae1b-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="6ae1b-139">Configure para habilitar ou desabilitar a aplicação de políticas de rede no ponto de extremidade privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="6ae1b-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="6ae1b-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="6ae1b-141">Configure para habilitar ou desabilitar a aplicação de políticas de rede no serviço de link privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="6ae1b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ae1b-142">-ResourceId</span></span>
<span data-ttu-id="6ae1b-143">Especifica a ID do recurso gateway NAT associado à configuração da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="6ae1b-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="6ae1b-144">-RouteTable</span></span>
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

### <span data-ttu-id="6ae1b-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="6ae1b-145">-RouteTableId</span></span>
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

### <span data-ttu-id="6ae1b-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ae1b-146">-ServiceEndpoint</span></span>
<span data-ttu-id="6ae1b-147">Valor do Ponto de Extremidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="6ae1b-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="6ae1b-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6ae1b-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="6ae1b-149">Políticas de Ponto de Extremidade de Serviço</span><span class="sxs-lookup"><span data-stu-id="6ae1b-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="6ae1b-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ae1b-150">-VirtualNetwork</span></span>
<span data-ttu-id="6ae1b-151">Especifica o **objeto VirtualNetwork** no qual adicionar uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="6ae1b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae1b-152">CommonParameters</span></span>
<span data-ttu-id="6ae1b-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae1b-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ae1b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae1b-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ae1b-155">INPUTS</span></span>

### <span data-ttu-id="6ae1b-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ae1b-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="6ae1b-157">System.String</span><span class="sxs-lookup"><span data-stu-id="6ae1b-157">System.String</span></span>

### <span data-ttu-id="6ae1b-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6ae1b-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="6ae1b-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6ae1b-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="6ae1b-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6ae1b-160">System.String[]</span></span>

### <span data-ttu-id="6ae1b-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="6ae1b-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="6ae1b-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span><span class="sxs-lookup"><span data-stu-id="6ae1b-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="6ae1b-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6ae1b-163">OUTPUTS</span></span>

### <span data-ttu-id="6ae1b-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ae1b-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6ae1b-165">NOTES</span><span class="sxs-lookup"><span data-stu-id="6ae1b-165">NOTES</span></span>

## <span data-ttu-id="6ae1b-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ae1b-166">RELATED LINKS</span></span>

[<span data-ttu-id="6ae1b-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6ae1b-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6ae1b-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6ae1b-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6ae1b-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6ae1b-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6ae1b-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6ae1b-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
