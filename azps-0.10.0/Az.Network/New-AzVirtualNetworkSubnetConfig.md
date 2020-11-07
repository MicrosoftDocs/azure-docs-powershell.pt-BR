---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 16f73c81c13740037131e47d03945d475db12ee9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775345"
---
# <span data-ttu-id="71b76-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="71b76-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="71b76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71b76-102">SYNOPSIS</span></span>
<span data-ttu-id="71b76-103">Cria uma configuração de sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="71b76-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="71b76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71b76-104">SYNTAX</span></span>

### <span data-ttu-id="71b76-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="71b76-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71b76-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="71b76-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71b76-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71b76-107">DESCRIPTION</span></span>
<span data-ttu-id="71b76-108">**O cmdlet New-AzVirtualNetworkSubnetConfig** cria uma configuração de sub-rede de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="71b76-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="71b76-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71b76-109">EXAMPLES</span></span>

### <span data-ttu-id="71b76-110">1: criar uma rede virtual com duas sub-redes e um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="71b76-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="71b76-111">Este exemplo cria duas novas configurações de sub-rede usando o cmdlet New-AzVirtualSubnetConfig e, em seguida, as usa para criar uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="71b76-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="71b76-112">O modelo New-AzVirtualSubnetConfig cria apenas uma representação na memória da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="71b76-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="71b76-113">Neste exemplo, o frontendSubnet tem CIDR 10.0.1.0/24 e faz referência a um grupo de segurança de rede que permite acesso ao RDP.</span><span class="sxs-lookup"><span data-stu-id="71b76-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="71b76-114">O backendSubnet tem 10.0.2.0/24 CIDR e faz referência ao mesmo grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="71b76-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="71b76-115">OS</span><span class="sxs-lookup"><span data-stu-id="71b76-115">PARAMETERS</span></span>

### <span data-ttu-id="71b76-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="71b76-116">-AddressPrefix</span></span>
<span data-ttu-id="71b76-117">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="71b76-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="71b76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b76-118">-DefaultProfile</span></span>
<span data-ttu-id="71b76-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71b76-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71b76-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="71b76-120">-Name</span></span>
<span data-ttu-id="71b76-121">Especifica o nome da configuração de sub-rede a ser criada.</span><span class="sxs-lookup"><span data-stu-id="71b76-121">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="71b76-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="71b76-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="71b76-123">Especifica um objeto NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="71b76-123">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="71b76-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="71b76-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="71b76-125">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="71b76-125">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="71b76-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="71b76-126">-RouteTable</span></span>
<span data-ttu-id="71b76-127">Especifica a tabela de rota associada à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="71b76-127">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="71b76-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="71b76-128">-RouteTableId</span></span>
<span data-ttu-id="71b76-129">Especifica a ID da tabela de rota associada à configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="71b76-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="71b76-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b76-130">-ServiceEndpoint</span></span>
<span data-ttu-id="71b76-131">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="71b76-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="71b76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b76-132">CommonParameters</span></span>
<span data-ttu-id="71b76-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b76-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b76-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b76-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71b76-135">INPUTS</span></span>

## <span data-ttu-id="71b76-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71b76-136">OUTPUTS</span></span>

### <span data-ttu-id="71b76-137">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="71b76-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="71b76-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71b76-138">NOTES</span></span>

## <span data-ttu-id="71b76-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71b76-139">RELATED LINKS</span></span>

[<span data-ttu-id="71b76-140">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="71b76-140">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="71b76-141">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="71b76-141">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="71b76-142">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="71b76-142">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="71b76-143">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="71b76-143">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


