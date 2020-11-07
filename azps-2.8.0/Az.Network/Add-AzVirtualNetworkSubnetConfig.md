---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fea7f3f3d24595cdddd9635e73e3073efe5cb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772075"
---
# <span data-ttu-id="fb44f-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fb44f-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="fb44f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb44f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb44f-103">Adiciona uma configuração de sub-rede a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fb44f-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="fb44f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb44f-104">SYNTAX</span></span>

### <span data-ttu-id="fb44f-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb44f-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb44f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb44f-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb44f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb44f-107">DESCRIPTION</span></span>
<span data-ttu-id="fb44f-108">O cmdlet **Add-AzVirtualNetworkSubnetConfig** adiciona uma configuração de sub-rede a uma rede virtual do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="fb44f-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="fb44f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb44f-109">EXAMPLES</span></span>

### <span data-ttu-id="fb44f-110">1: adicionar uma sub-rede a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="fb44f-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="fb44f-111">Este exemplo primeiro cria um grupo de recursos como um contêiner dos recursos a serem criados.</span><span class="sxs-lookup"><span data-stu-id="fb44f-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="fb44f-112">Em seguida, ele cria uma configuração de sub-rede e a usa para criar uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fb44f-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="fb44f-113">O Add-AzVirtualNetworkSubnetConfig é usado para adicionar uma sub-rede à representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fb44f-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="fb44f-114">O comando Set-AzVirtualNetwork atualiza a rede virtual existente com a nova sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="fb44f-115">2: adicionar uma delegação a uma sub-rede adicionada a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="fb44f-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="fb44f-116">Este exemplo primeiro obtém uma vnet existente.</span><span class="sxs-lookup"><span data-stu-id="fb44f-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="fb44f-117">Em seguida, ele cria um objeto Delegation na memória.</span><span class="sxs-lookup"><span data-stu-id="fb44f-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="fb44f-118">Por fim, ele cria uma nova sub-rede com essa delegação que é adicionada à vnet.</span><span class="sxs-lookup"><span data-stu-id="fb44f-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="fb44f-119">A configuração modificada é enviada para o servidor.</span><span class="sxs-lookup"><span data-stu-id="fb44f-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="fb44f-120">OS</span><span class="sxs-lookup"><span data-stu-id="fb44f-120">PARAMETERS</span></span>

### <span data-ttu-id="fb44f-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fb44f-121">-AddressPrefix</span></span>
<span data-ttu-id="fb44f-122">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="fb44f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb44f-123">-DefaultProfile</span></span>
<span data-ttu-id="fb44f-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb44f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb44f-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="fb44f-125">-Delegation</span></span>
<span data-ttu-id="fb44f-126">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="fb44f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb44f-127">-InputObject</span></span>
<span data-ttu-id="fb44f-128">Especifica o gateway NAT associado à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="fb44f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb44f-129">-Name</span></span>
<span data-ttu-id="fb44f-130">Especifica o nome da configuração de sub-rede a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="fb44f-130">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="fb44f-131">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb44f-131">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fb44f-132">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="fb44f-132">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="fb44f-133">Esse cmdlet adiciona uma configuração de sub-rede de rede virtual ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="fb44f-133">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb44f-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fb44f-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="fb44f-135">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="fb44f-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="fb44f-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="fb44f-137">Configure para habilitar ou desabilitar a aplicação de políticas de rede em um ponto de extremidade privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="fb44f-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="fb44f-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="fb44f-139">Configure para habilitar ou desabilitar a aplicação de políticas de rede no serviço de link privado na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="fb44f-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb44f-140">-ResourceId</span></span>
<span data-ttu-id="fb44f-141">Especifica a ID do recurso de gateway NAT associado à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="fb44f-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="fb44f-142">-RouteTable</span></span>
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

### <span data-ttu-id="fb44f-143">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="fb44f-143">-RouteTableId</span></span>
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

### <span data-ttu-id="fb44f-144">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb44f-144">-ServiceEndpoint</span></span>
<span data-ttu-id="fb44f-145">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="fb44f-145">Service Endpoint Value</span></span>

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

### <span data-ttu-id="fb44f-146">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fb44f-146">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="fb44f-147">Políticas de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="fb44f-147">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="fb44f-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb44f-148">-VirtualNetwork</span></span>
<span data-ttu-id="fb44f-149">Especifica o objeto **VirtualNetwork** no qual adicionar uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb44f-149">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="fb44f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb44f-150">CommonParameters</span></span>
<span data-ttu-id="fb44f-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb44f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb44f-152">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb44f-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb44f-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb44f-153">INPUTS</span></span>

### <span data-ttu-id="fb44f-154">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb44f-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="fb44f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="fb44f-155">System.String</span></span>

### <span data-ttu-id="fb44f-156">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fb44f-156">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="fb44f-157">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="fb44f-157">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="fb44f-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="fb44f-158">System.String[]</span></span>

### <span data-ttu-id="fb44f-159">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="fb44f-159">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="fb44f-160">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="fb44f-160">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="fb44f-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb44f-161">OUTPUTS</span></span>

### <span data-ttu-id="fb44f-162">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb44f-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="fb44f-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb44f-163">NOTES</span></span>

## <span data-ttu-id="fb44f-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb44f-164">RELATED LINKS</span></span>

[<span data-ttu-id="fb44f-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fb44f-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fb44f-166">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fb44f-166">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fb44f-167">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fb44f-167">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fb44f-168">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fb44f-168">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
