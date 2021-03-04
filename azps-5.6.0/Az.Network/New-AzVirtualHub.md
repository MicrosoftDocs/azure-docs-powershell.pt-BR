---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: a7b8e790892b14e053a07f83e6a27c4ce82c00ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889437"
---
# <span data-ttu-id="4eebd-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4eebd-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="4eebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eebd-102">SYNOPSIS</span></span>
<span data-ttu-id="4eebd-103">Cria um recurso virtualHub do Azure.</span><span class="sxs-lookup"><span data-stu-id="4eebd-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="4eebd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4eebd-104">SYNTAX</span></span>

### <span data-ttu-id="4eebd-105">ByVirtualWanObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4eebd-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eebd-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="4eebd-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eebd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4eebd-107">DESCRIPTION</span></span>
<span data-ttu-id="4eebd-108">Cria um recurso virtualHub do Azure.</span><span class="sxs-lookup"><span data-stu-id="4eebd-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="4eebd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4eebd-109">EXAMPLES</span></span>

### <span data-ttu-id="4eebd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4eebd-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="4eebd-111">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="4eebd-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="4eebd-112">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="4eebd-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="4eebd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4eebd-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="4eebd-114">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="4eebd-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="4eebd-115">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="4eebd-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="4eebd-116">Este exemplo é semelhante ao Exemplo 1, mas usa uma ID de recurso para fazer referência à WAN Virtual necessária para criar o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="4eebd-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="4eebd-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4eebd-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="4eebd-118">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="4eebd-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="4eebd-119">O hub virtual terá o espaço de endereço "10.0.1.0/24" e uma tabela de rota anexada.</span><span class="sxs-lookup"><span data-stu-id="4eebd-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="4eebd-120">Este exemplo é semelhante ao Exemplo 2, mas também anexa uma tabela de rota ao hub virtual.</span><span class="sxs-lookup"><span data-stu-id="4eebd-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="4eebd-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4eebd-121">PARAMETERS</span></span>

### <span data-ttu-id="4eebd-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4eebd-122">-AddressPrefix</span></span>
<span data-ttu-id="4eebd-123">A cadeia de caracteres de espaço de endereço para esse hub virtual.</span><span class="sxs-lookup"><span data-stu-id="4eebd-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="4eebd-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4eebd-124">-AsJob</span></span>
<span data-ttu-id="4eebd-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4eebd-125">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eebd-126">-DefaultProfile</span></span>
<span data-ttu-id="4eebd-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4eebd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4eebd-128">-HubVnetConnection</span></span>
<span data-ttu-id="4eebd-129">As conexões de rede virtual do hub associadas a esse Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="4eebd-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-130">-Location</span><span class="sxs-lookup"><span data-stu-id="4eebd-130">-Location</span></span>
<span data-ttu-id="4eebd-131">location.</span><span class="sxs-lookup"><span data-stu-id="4eebd-131">location.</span></span>

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

### <span data-ttu-id="4eebd-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4eebd-132">-Name</span></span>
<span data-ttu-id="4eebd-133">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4eebd-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eebd-134">-ResourceGroupName</span></span>
<span data-ttu-id="4eebd-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4eebd-135">The resource group name.</span></span>

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

### <span data-ttu-id="4eebd-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4eebd-136">-RouteTable</span></span>
<span data-ttu-id="4eebd-137">A tabela de rota associada a esse Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="4eebd-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="4eebd-138">-Sku</span></span>
<span data-ttu-id="4eebd-139">O sku do Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="4eebd-139">The sku of the Virtual Hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="4eebd-140">-Tag</span></span>
<span data-ttu-id="4eebd-141">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="4eebd-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="4eebd-142">-VirtualWan</span></span>
<span data-ttu-id="4eebd-143">O objeto wan virtual ao que esse hub está vinculado.</span><span class="sxs-lookup"><span data-stu-id="4eebd-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="4eebd-144">-VirtualWanId</span></span>
<span data-ttu-id="4eebd-145">A id do objeto wan virtual ao que o hub está vinculado.</span><span class="sxs-lookup"><span data-stu-id="4eebd-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eebd-146">-Confirm</span></span>
<span data-ttu-id="4eebd-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eebd-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eebd-148">-WhatIf</span></span>
<span data-ttu-id="4eebd-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4eebd-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eebd-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4eebd-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eebd-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eebd-151">CommonParameters</span></span>
<span data-ttu-id="4eebd-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eebd-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eebd-153">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4eebd-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eebd-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eebd-154">INPUTS</span></span>

### <span data-ttu-id="4eebd-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="4eebd-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="4eebd-156">System.String</span><span class="sxs-lookup"><span data-stu-id="4eebd-156">System.String</span></span>

## <span data-ttu-id="4eebd-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4eebd-157">OUTPUTS</span></span>

### <span data-ttu-id="4eebd-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4eebd-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="4eebd-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="4eebd-159">NOTES</span></span>

## <span data-ttu-id="4eebd-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4eebd-160">RELATED LINKS</span></span>

[<span data-ttu-id="4eebd-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4eebd-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="4eebd-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4eebd-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="4eebd-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4eebd-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
