---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e0356f738bcc0abd52f0ec72c4c6766af8be550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599950"
---
# <span data-ttu-id="268c1-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="268c1-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="268c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="268c1-102">SYNOPSIS</span></span>
<span data-ttu-id="268c1-103">Atualiza uma configuração de sub-rede para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="268c1-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="268c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="268c1-104">SYNTAX</span></span>

### <span data-ttu-id="268c1-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="268c1-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268c1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="268c1-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="268c1-107">DESCRIPTION</span></span>
<span data-ttu-id="268c1-108">O cmdlet **set-AzVirtualNetworkSubnetConfig** atualiza uma configuração de sub-rede para uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="268c1-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="268c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="268c1-109">EXAMPLES</span></span>

### <span data-ttu-id="268c1-110">1: modificar o prefixo do endereço de uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="268c1-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="268c1-111">Este exemplo cria uma rede virtual com uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="268c1-112">Em seguida, chama-se Set-AzVirtualNetworkSubnetConfig de modificar o AddressPrefix da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="268c1-113">Isso afeta apenas a representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="268c1-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="268c1-114">Set-AzVirtualNetwork, em seguida, é chamado para modificar a rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="268c1-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="268c1-115">2: adicionar um grupo de segurança de rede a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="268c1-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="268c1-116">Este exemplo cria um grupo de recursos com uma rede virtual contendo apenas uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="268c1-117">Em seguida, ele cria um grupo de segurança de rede com uma regra de permissão para tráfego RDP.</span><span class="sxs-lookup"><span data-stu-id="268c1-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="268c1-118">O cmdlet Set-AzVirtualNetworkSubnetConfig é usado para modificar a representação na memória da sub-rede de front-end para que ele aponte para o grupo de segurança de rede recém-criado.</span><span class="sxs-lookup"><span data-stu-id="268c1-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="268c1-119">O cmdlet Set-AzVirtualNetwork, em seguida, chamado para gravar o estado modificado novamente para o serviço.</span><span class="sxs-lookup"><span data-stu-id="268c1-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="268c1-120">OS</span><span class="sxs-lookup"><span data-stu-id="268c1-120">PARAMETERS</span></span>

### <span data-ttu-id="268c1-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="268c1-121">-AddressPrefix</span></span>
<span data-ttu-id="268c1-122">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="268c1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268c1-123">-DefaultProfile</span></span>
<span data-ttu-id="268c1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="268c1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268c1-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="268c1-125">-Delegation</span></span>
<span data-ttu-id="268c1-126">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="268c1-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="268c1-127">-Name</span></span>
<span data-ttu-id="268c1-128">Especifica o nome de uma configuração de sub-rede que este cmdlet configura.</span><span class="sxs-lookup"><span data-stu-id="268c1-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="268c1-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="268c1-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="268c1-130">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="268c1-130">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="268c1-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="268c1-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="268c1-132">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-132">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="268c1-133">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="268c1-133">-RouteTable</span></span>
<span data-ttu-id="268c1-134">Especifica o objeto da tabela de rota que está associado ao grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-134">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="268c1-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="268c1-135">-RouteTableId</span></span>
<span data-ttu-id="268c1-136">Especifica a ID do objeto da tabela de rota que está associado ao grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="268c1-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="268c1-137">-ServiceEndpoint</span></span>
<span data-ttu-id="268c1-138">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="268c1-138">Service Endpoint Value</span></span>

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

### <span data-ttu-id="268c1-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="268c1-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="268c1-140">Políticas de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="268c1-140">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="268c1-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="268c1-141">-VirtualNetwork</span></span>
<span data-ttu-id="268c1-142">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="268c1-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="268c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268c1-143">CommonParameters</span></span>
<span data-ttu-id="268c1-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268c1-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268c1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268c1-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="268c1-146">INPUTS</span></span>

### <span data-ttu-id="268c1-147">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="268c1-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="268c1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="268c1-148">System.String</span></span>

### <span data-ttu-id="268c1-149">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="268c1-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="268c1-150">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="268c1-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="268c1-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="268c1-151">System.String[]</span></span>

### <span data-ttu-id="268c1-152">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="268c1-152">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="268c1-153">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="268c1-153">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="268c1-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="268c1-154">OUTPUTS</span></span>

### <span data-ttu-id="268c1-155">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="268c1-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="268c1-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="268c1-156">NOTES</span></span>

## <span data-ttu-id="268c1-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="268c1-157">RELATED LINKS</span></span>

[<span data-ttu-id="268c1-158">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="268c1-158">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="268c1-159">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="268c1-159">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="268c1-160">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="268c1-160">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="268c1-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="268c1-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
