---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 836973c4b1d95445d905bb41f489c48136e12f6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600257"
---
# <span data-ttu-id="d033f-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d033f-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="d033f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d033f-102">SYNOPSIS</span></span>
<span data-ttu-id="d033f-103">Cria uma configuração de sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d033f-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="d033f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d033f-104">SYNTAX</span></span>

### <span data-ttu-id="d033f-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="d033f-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d033f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d033f-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d033f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d033f-107">DESCRIPTION</span></span>
<span data-ttu-id="d033f-108">**O cmdlet New-AzVirtualNetworkSubnetConfig** cria uma configuração de sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d033f-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="d033f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d033f-109">EXAMPLES</span></span>

### <span data-ttu-id="d033f-110">1: criar uma rede virtual com duas sub-redes e um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="d033f-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="d033f-111">Este exemplo cria duas novas configurações de sub-rede usando o cmdlet New-AzVirtualSubnetConfig e, em seguida, as usa para criar uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d033f-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="d033f-112">O modelo New-AzVirtualSubnetConfig cria apenas uma representação na memória da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d033f-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="d033f-113">Neste exemplo, o frontendSubnet tem CIDR 10.0.1.0/24 e faz referência a um grupo de segurança de rede que permite acesso ao RDP.</span><span class="sxs-lookup"><span data-stu-id="d033f-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="d033f-114">O backendSubnet tem 10.0.2.0/24 CIDR e faz referência ao mesmo grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="d033f-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="d033f-115">OS</span><span class="sxs-lookup"><span data-stu-id="d033f-115">PARAMETERS</span></span>

### <span data-ttu-id="d033f-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d033f-116">-AddressPrefix</span></span>
<span data-ttu-id="d033f-117">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d033f-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="d033f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d033f-118">-DefaultProfile</span></span>
<span data-ttu-id="d033f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d033f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d033f-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="d033f-120">-Delegation</span></span>
<span data-ttu-id="d033f-121">Lista de serviços que têm permissão para executar operações nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d033f-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="d033f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d033f-122">-Name</span></span>
<span data-ttu-id="d033f-123">Especifica o nome da configuração de sub-rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="d033f-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="d033f-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d033f-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d033f-125">Especifica um objeto NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="d033f-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="d033f-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d033f-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d033f-127">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="d033f-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="d033f-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d033f-128">-RouteTable</span></span>
<span data-ttu-id="d033f-129">Especifica a tabela de rota associada à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d033f-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="d033f-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="d033f-130">-RouteTableId</span></span>
<span data-ttu-id="d033f-131">Especifica a ID da tabela de rota associada à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d033f-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="d033f-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d033f-132">-ServiceEndpoint</span></span>
<span data-ttu-id="d033f-133">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="d033f-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="d033f-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d033f-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d033f-135">Políticas de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="d033f-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="d033f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d033f-136">CommonParameters</span></span>
<span data-ttu-id="d033f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d033f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d033f-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d033f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d033f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d033f-139">INPUTS</span></span>

### <span data-ttu-id="d033f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d033f-140">System.String</span></span>

### <span data-ttu-id="d033f-141">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d033f-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="d033f-142">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d033f-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="d033f-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="d033f-143">System.String[]</span></span>

### <span data-ttu-id="d033f-144">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="d033f-144">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="d033f-145">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="d033f-145">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="d033f-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d033f-146">OUTPUTS</span></span>

### <span data-ttu-id="d033f-147">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d033f-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="d033f-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d033f-148">NOTES</span></span>

## <span data-ttu-id="d033f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d033f-149">RELATED LINKS</span></span>

[<span data-ttu-id="d033f-150">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d033f-150">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d033f-151">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d033f-151">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d033f-152">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d033f-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d033f-153">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d033f-153">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
