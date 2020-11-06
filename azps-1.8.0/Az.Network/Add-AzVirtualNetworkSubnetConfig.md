---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600682"
---
# <span data-ttu-id="2adb1-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2adb1-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="2adb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2adb1-102">SYNOPSIS</span></span>
<span data-ttu-id="2adb1-103">Adiciona uma configuração de sub-rede a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2adb1-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="2adb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2adb1-104">SYNTAX</span></span>

### <span data-ttu-id="2adb1-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="2adb1-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2adb1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2adb1-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2adb1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2adb1-107">DESCRIPTION</span></span>
<span data-ttu-id="2adb1-108">O cmdlet **Add-AzVirtualNetworkSubnetConfig** adiciona uma configuração de sub-rede a uma rede virtual do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="2adb1-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="2adb1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2adb1-109">EXAMPLES</span></span>

### <span data-ttu-id="2adb1-110">1: adicionar uma sub-rede a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="2adb1-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="2adb1-111">Este exemplo primeiro cria um grupo de recursos como um contêiner dos recursos a serem criados.</span><span class="sxs-lookup"><span data-stu-id="2adb1-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="2adb1-112">Em seguida, ele cria uma configuração de sub-rede e a usa para criar uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2adb1-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="2adb1-113">O Add-AzVirtualNetworkSubnetConfig é usado para adicionar uma sub-rede à representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2adb1-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="2adb1-114">O comando Set-AzVirtualNetwork atualiza a rede virtual existente com a nova sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2adb1-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="2adb1-115">2: adicionar uma delegação a uma sub-rede adicionada a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="2adb1-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="2adb1-116">Este exemplo primeiro obtém uma vnet existente.</span><span class="sxs-lookup"><span data-stu-id="2adb1-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="2adb1-117">Em seguida, ele cria um objeto Delegation na memória.</span><span class="sxs-lookup"><span data-stu-id="2adb1-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="2adb1-118">Por fim, ele cria uma nova sub-rede com essa delegação que é adicionada à vnet.</span><span class="sxs-lookup"><span data-stu-id="2adb1-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="2adb1-119">A configuração modificada é enviada para o servidor.</span><span class="sxs-lookup"><span data-stu-id="2adb1-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="2adb1-120">OS</span><span class="sxs-lookup"><span data-stu-id="2adb1-120">PARAMETERS</span></span>

### <span data-ttu-id="2adb1-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2adb1-121">-AddressPrefix</span></span>
<span data-ttu-id="2adb1-122">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2adb1-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="2adb1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2adb1-123">-DefaultProfile</span></span>
<span data-ttu-id="2adb1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2adb1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2adb1-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="2adb1-125">-Delegation</span></span>
<span data-ttu-id="2adb1-126">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2adb1-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="2adb1-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2adb1-127">-Name</span></span>
<span data-ttu-id="2adb1-128">Especifica o nome da configuração de sub-rede a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="2adb1-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="2adb1-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2adb1-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2adb1-130">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="2adb1-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="2adb1-131">Esse cmdlet adiciona uma configuração de sub-rede de rede virtual ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2adb1-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="2adb1-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2adb1-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2adb1-133">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="2adb1-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="2adb1-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2adb1-134">-RouteTable</span></span>
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

### <span data-ttu-id="2adb1-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="2adb1-135">-RouteTableId</span></span>
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

### <span data-ttu-id="2adb1-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2adb1-136">-ServiceEndpoint</span></span>
<span data-ttu-id="2adb1-137">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="2adb1-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="2adb1-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2adb1-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2adb1-139">Políticas de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="2adb1-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="2adb1-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2adb1-140">-VirtualNetwork</span></span>
<span data-ttu-id="2adb1-141">Especifica o objeto **VirtualNetwork** no qual adicionar uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2adb1-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="2adb1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adb1-142">CommonParameters</span></span>
<span data-ttu-id="2adb1-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2adb1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adb1-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adb1-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2adb1-145">INPUTS</span></span>

### <span data-ttu-id="2adb1-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2adb1-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="2adb1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2adb1-147">System.String</span></span>

### <span data-ttu-id="2adb1-148">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2adb1-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="2adb1-149">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2adb1-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="2adb1-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="2adb1-150">System.String[]</span></span>

### <span data-ttu-id="2adb1-151">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="2adb1-151">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="2adb1-152">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="2adb1-152">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="2adb1-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2adb1-153">OUTPUTS</span></span>

### <span data-ttu-id="2adb1-154">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2adb1-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="2adb1-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2adb1-155">NOTES</span></span>

## <span data-ttu-id="2adb1-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2adb1-156">RELATED LINKS</span></span>

[<span data-ttu-id="2adb1-157">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2adb1-157">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2adb1-158">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2adb1-158">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2adb1-159">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2adb1-159">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2adb1-160">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2adb1-160">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
