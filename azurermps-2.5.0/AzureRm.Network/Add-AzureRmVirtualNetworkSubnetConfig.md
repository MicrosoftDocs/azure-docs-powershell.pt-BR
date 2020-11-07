---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: 9f1f4f916ea0756ebf034c12e1e9f92f3cd3c865
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786493"
---
# <span data-ttu-id="7190c-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7190c-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="7190c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7190c-102">SYNOPSIS</span></span>
<span data-ttu-id="7190c-103">Adiciona uma configuração de sub-rede a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7190c-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7190c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7190c-104">SYNTAX</span></span>

### <span data-ttu-id="7190c-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="7190c-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7190c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7190c-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7190c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7190c-107">DESCRIPTION</span></span>
<span data-ttu-id="7190c-108">O cmdlet **Add-AzureRmVirtualNetworkSubnetConfig** adiciona uma configuração de sub-rede a uma rede virtual do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="7190c-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="7190c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7190c-109">EXAMPLES</span></span>

### <span data-ttu-id="7190c-110">1: adicionar uma sub-rede a uma rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="7190c-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="7190c-111">Este exemplo primeiro cria um grupo de recursos como um contêiner dos recursos a serem criados.</span><span class="sxs-lookup"><span data-stu-id="7190c-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="7190c-112">Em seguida, ele cria uma configuração de sub-rede e a usa para criar uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7190c-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="7190c-113">O Add-AzureRmVirtualNetworkSubnetConfig é usado para adicionar uma sub-rede à representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7190c-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="7190c-114">O comando Set-AzureRmVirtualNetwork atualiza a rede virtual existente com a nova sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7190c-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="7190c-115">OS</span><span class="sxs-lookup"><span data-stu-id="7190c-115">PARAMETERS</span></span>

### <span data-ttu-id="7190c-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7190c-116">-AddressPrefix</span></span>
<span data-ttu-id="7190c-117">Especifica um intervalo de endereços IP para uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7190c-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="7190c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7190c-118">-DefaultProfile</span></span>
<span data-ttu-id="7190c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7190c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7190c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7190c-120">-Name</span></span>
<span data-ttu-id="7190c-121">Especifica o nome da configuração de sub-rede a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7190c-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="7190c-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7190c-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7190c-123">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="7190c-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="7190c-124">Esse cmdlet adiciona uma configuração de sub-rede de rede virtual ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7190c-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="7190c-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7190c-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="7190c-126">Especifica a ID de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="7190c-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="7190c-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7190c-127">-RouteTable</span></span>
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

### <span data-ttu-id="7190c-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="7190c-128">-RouteTableId</span></span>
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

### <span data-ttu-id="7190c-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7190c-129">-ServiceEndpoint</span></span>
<span data-ttu-id="7190c-130">Valor do ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="7190c-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="7190c-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7190c-131">-VirtualNetwork</span></span>
<span data-ttu-id="7190c-132">Especifica o objeto **VirtualNetwork** no qual adicionar uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7190c-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="7190c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7190c-133">CommonParameters</span></span>
<span data-ttu-id="7190c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7190c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7190c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7190c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7190c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7190c-136">INPUTS</span></span>

### <span data-ttu-id="7190c-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7190c-137">PSVirtualNetwork</span></span>
<span data-ttu-id="7190c-138">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="7190c-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="7190c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7190c-139">OUTPUTS</span></span>

### <span data-ttu-id="7190c-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7190c-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7190c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7190c-141">NOTES</span></span>

## <span data-ttu-id="7190c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7190c-142">RELATED LINKS</span></span>

[<span data-ttu-id="7190c-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7190c-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7190c-144">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7190c-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7190c-145">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7190c-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7190c-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7190c-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


