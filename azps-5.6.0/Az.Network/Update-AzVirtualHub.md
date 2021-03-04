---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: 871847c9b089a53021d90cdf5b290bf7f9241867
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885333"
---
# <span data-ttu-id="a3850-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3850-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="a3850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3850-102">SYNOPSIS</span></span>
<span data-ttu-id="a3850-103">Atualiza um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="a3850-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="a3850-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3850-104">SYNTAX</span></span>

### <span data-ttu-id="a3850-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3850-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3850-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a3850-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3850-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a3850-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3850-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3850-108">DESCRIPTION</span></span>
<span data-ttu-id="a3850-109">O cmdlet **Update-AzVirtualHub** atualiza um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="a3850-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="a3850-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3850-110">EXAMPLES</span></span>

### <span data-ttu-id="a3850-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3850-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="a3850-112">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="a3850-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a3850-113">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a3850-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="a3850-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a3850-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="a3850-115">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="a3850-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="a3850-116">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="a3850-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="a3850-117">Este exemplo é semelhante ao Exemplo 1, mas também anexa uma tabela de rota ao hub virtual.</span><span class="sxs-lookup"><span data-stu-id="a3850-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="a3850-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3850-118">PARAMETERS</span></span>

### <span data-ttu-id="a3850-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a3850-119">-AddressPrefix</span></span>
<span data-ttu-id="a3850-120">A cadeia de caracteres de espaço de endereço para esse hub virtual.</span><span class="sxs-lookup"><span data-stu-id="a3850-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="a3850-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3850-121">-AsJob</span></span>
<span data-ttu-id="a3850-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a3850-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3850-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3850-123">-DefaultProfile</span></span>
<span data-ttu-id="a3850-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3850-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3850-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a3850-125">-HubVnetConnection</span></span>
<span data-ttu-id="a3850-126">As conexões de rede virtual do hub associadas a esse Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="a3850-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="a3850-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3850-127">-InputObject</span></span>
<span data-ttu-id="a3850-128">O objeto de hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="a3850-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3850-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a3850-129">-Name</span></span>
<span data-ttu-id="a3850-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a3850-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3850-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3850-131">-ResourceGroupName</span></span>
<span data-ttu-id="a3850-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3850-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3850-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3850-133">-ResourceId</span></span>
<span data-ttu-id="a3850-134">A id de recurso do hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="a3850-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3850-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a3850-135">-RouteTable</span></span>
<span data-ttu-id="a3850-136">A tabela de rota associada a esse Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="a3850-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="a3850-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="a3850-137">-Sku</span></span>
<span data-ttu-id="a3850-138">O sku do Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="a3850-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="a3850-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3850-139">-Tag</span></span>
<span data-ttu-id="a3850-140">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a3850-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a3850-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3850-141">-Confirm</span></span>
<span data-ttu-id="a3850-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3850-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3850-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3850-143">-WhatIf</span></span>
<span data-ttu-id="a3850-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3850-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3850-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3850-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3850-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3850-146">CommonParameters</span></span>
<span data-ttu-id="a3850-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3850-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3850-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3850-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3850-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3850-149">INPUTS</span></span>

### <span data-ttu-id="a3850-150">System.String</span><span class="sxs-lookup"><span data-stu-id="a3850-150">System.String</span></span>

### <span data-ttu-id="a3850-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3850-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a3850-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3850-152">OUTPUTS</span></span>

### <span data-ttu-id="a3850-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3850-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a3850-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3850-154">NOTES</span></span>

## <span data-ttu-id="a3850-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3850-155">RELATED LINKS</span></span>

[<span data-ttu-id="a3850-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3850-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="a3850-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3850-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="a3850-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a3850-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
