---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: b13a06fbc2bd7f071888dcd0504d3e1963cbedd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786250"
---
# <span data-ttu-id="af365-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="af365-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="af365-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af365-102">SYNOPSIS</span></span>
<span data-ttu-id="af365-103">Configura o estado da meta para uma configuração de sub-rede em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="af365-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af365-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af365-104">SYNTAX</span></span>

### <span data-ttu-id="af365-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="af365-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af365-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af365-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af365-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af365-107">DESCRIPTION</span></span>
<span data-ttu-id="af365-108">O cmdlet **set-AzureRmVirtualNetworkSubnetConfig** configura o estado da meta para uma configuração de sub-rede em uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="af365-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="af365-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af365-109">EXAMPLES</span></span>

### <span data-ttu-id="af365-110">1: modificar o prefixo do endereço de uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="af365-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="af365-111">Este exemplo cria uma rede virtual com uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="af365-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="af365-112">Em seguida, chama-se Set-AzureRmVirtualNetworkSubnetConfig de modificar o AddressPrefix da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="af365-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="af365-113">Isso afeta apenas a representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="af365-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="af365-114">Set-AzureRmVirtualNetwork, em seguida, é chamado para modificar a rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="af365-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="af365-115">2: adicionar um grupo de segurança de rede a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="af365-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="af365-116">Este exemplo cria um grupo de recursos com uma rede virtual contendo apenas uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="af365-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="af365-117">Em seguida, ele cria um grupo de segurança de rede com uma regra de permissão para tráfego RDP.</span><span class="sxs-lookup"><span data-stu-id="af365-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="af365-118">O cmdlet Set-AzureRmVirtualNetworkSubnetConfig é usado para modificar a representação na memória da sub-rede de front-end para que ele aponte para o grupo de segurança de rede recém-criado.</span><span class="sxs-lookup"><span data-stu-id="af365-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="af365-119">O cmdlet Set-AzureRmVirtualNetwork, em seguida, chamado para gravar o estado modificado novamente para o serviço.</span><span class="sxs-lookup"><span data-stu-id="af365-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="af365-120">OS</span><span class="sxs-lookup"><span data-stu-id="af365-120">PARAMETERS</span></span>

### <span data-ttu-id="af365-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="af365-121">-AddressPrefix</span></span>
<span data-ttu-id="af365-122">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="af365-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af365-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af365-123">-DefaultProfile</span></span>
<span data-ttu-id="af365-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af365-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af365-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="af365-125">-Name</span></span>
<span data-ttu-id="af365-126">Especifica o nome de uma configuração de sub-rede que este cmdlet configura.</span><span class="sxs-lookup"><span data-stu-id="af365-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af365-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="af365-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="af365-128">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="af365-128">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af365-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="af365-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="af365-130">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="af365-130">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="af365-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="af365-131">-RouteTable</span></span>
<span data-ttu-id="af365-132">Especifica o objeto da tabela de rota que está associado ao grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="af365-132">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af365-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="af365-133">-RouteTableId</span></span>
<span data-ttu-id="af365-134">Especifica a ID do objeto da tabela de rota que está associado ao grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="af365-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="af365-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="af365-135">-ServiceEndpoint</span></span>
<span data-ttu-id="af365-136">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="af365-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="af365-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="af365-137">-VirtualNetwork</span></span>
<span data-ttu-id="af365-138">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="af365-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af365-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af365-139">CommonParameters</span></span>
<span data-ttu-id="af365-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af365-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af365-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af365-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af365-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af365-142">INPUTS</span></span>

### <span data-ttu-id="af365-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="af365-143">PSVirtualNetwork</span></span>
<span data-ttu-id="af365-144">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="af365-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="af365-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af365-145">OUTPUTS</span></span>

### <span data-ttu-id="af365-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="af365-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="af365-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af365-147">NOTES</span></span>

## <span data-ttu-id="af365-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af365-148">RELATED LINKS</span></span>

[<span data-ttu-id="af365-149">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="af365-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="af365-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="af365-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="af365-151">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="af365-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="af365-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="af365-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


