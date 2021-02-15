---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111610"
---
# <span data-ttu-id="62712-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="62712-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="62712-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62712-102">SYNOPSIS</span></span>
<span data-ttu-id="62712-103">Cria um recurso do Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="62712-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="62712-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62712-104">SYNTAX</span></span>

### <span data-ttu-id="62712-105">ByVirtualWanObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="62712-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62712-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="62712-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62712-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="62712-107">DESCRIPTION</span></span>
<span data-ttu-id="62712-108">Cria um recurso do Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="62712-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="62712-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62712-109">EXAMPLES</span></span>

### <span data-ttu-id="62712-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62712-110">Example 1</span></span>

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

<span data-ttu-id="62712-111">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="62712-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="62712-112">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="62712-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="62712-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="62712-113">Example 2</span></span>

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

<span data-ttu-id="62712-114">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="62712-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="62712-115">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="62712-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="62712-116">Este exemplo é semelhante ao Exemplo 1, mas usa uma ID de recurso para fazer referência à WAN Virtual necessária para criar o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="62712-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="62712-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="62712-117">Example 3</span></span>

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

<span data-ttu-id="62712-118">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="62712-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="62712-119">O hub virtual terá o espaço de endereço "10.0.1.0/24" e uma tabela de rota anexada.</span><span class="sxs-lookup"><span data-stu-id="62712-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="62712-120">Este exemplo é semelhante ao Exemplo 2, mas também anexa uma tabela de rota ao hub virtual.</span><span class="sxs-lookup"><span data-stu-id="62712-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="62712-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62712-121">PARAMETERS</span></span>

### <span data-ttu-id="62712-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="62712-122">-AddressPrefix</span></span>
<span data-ttu-id="62712-123">A cadeia de espaços de endereço para este hub virtual.</span><span class="sxs-lookup"><span data-stu-id="62712-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="62712-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62712-124">-AsJob</span></span>
<span data-ttu-id="62712-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="62712-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62712-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62712-126">-DefaultProfile</span></span>
<span data-ttu-id="62712-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62712-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62712-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="62712-128">-HubVnetConnection</span></span>
<span data-ttu-id="62712-129">As conexões de rede virtual do hub associadas a este Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="62712-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="62712-130">-Local</span><span class="sxs-lookup"><span data-stu-id="62712-130">-Location</span></span>
<span data-ttu-id="62712-131">Localização.</span><span class="sxs-lookup"><span data-stu-id="62712-131">location.</span></span>

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

### <span data-ttu-id="62712-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="62712-132">-Name</span></span>
<span data-ttu-id="62712-133">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="62712-133">The resource name.</span></span>

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

### <span data-ttu-id="62712-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62712-134">-ResourceGroupName</span></span>
<span data-ttu-id="62712-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62712-135">The resource group name.</span></span>

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

### <span data-ttu-id="62712-136">-Tabela de Rota</span><span class="sxs-lookup"><span data-stu-id="62712-136">-RouteTable</span></span>
<span data-ttu-id="62712-137">A tabela de rota associada a este Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="62712-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="62712-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="62712-138">-Sku</span></span>
<span data-ttu-id="62712-139">A sku do Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="62712-139">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="62712-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="62712-140">-Tag</span></span>
<span data-ttu-id="62712-141">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="62712-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="62712-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="62712-142">-VirtualWan</span></span>
<span data-ttu-id="62712-143">O objeto wan virtual ao que este hub está vinculado.</span><span class="sxs-lookup"><span data-stu-id="62712-143">The virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="62712-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="62712-144">-VirtualWanId</span></span>
<span data-ttu-id="62712-145">A id do objeto wan virtual ao que este hub está vinculado.</span><span class="sxs-lookup"><span data-stu-id="62712-145">The id of virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="62712-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="62712-146">-Confirm</span></span>
<span data-ttu-id="62712-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62712-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62712-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62712-148">-WhatIf</span></span>
<span data-ttu-id="62712-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="62712-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62712-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62712-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62712-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62712-151">CommonParameters</span></span>
<span data-ttu-id="62712-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62712-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62712-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62712-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62712-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="62712-154">INPUTS</span></span>

### <span data-ttu-id="62712-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="62712-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="62712-156">System.String</span><span class="sxs-lookup"><span data-stu-id="62712-156">System.String</span></span>

## <span data-ttu-id="62712-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="62712-157">OUTPUTS</span></span>

### <span data-ttu-id="62712-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="62712-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="62712-159">Notas</span><span class="sxs-lookup"><span data-stu-id="62712-159">NOTES</span></span>

## <span data-ttu-id="62712-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62712-160">RELATED LINKS</span></span>

[<span data-ttu-id="62712-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="62712-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="62712-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="62712-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="62712-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="62712-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
