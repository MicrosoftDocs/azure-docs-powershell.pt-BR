---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: 8527b383dd5469d1a9bc34b7916a1e28b3f673f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600272"
---
# <span data-ttu-id="b8e78-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b8e78-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="b8e78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8e78-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e78-103">Cria um recurso do Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b8e78-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="b8e78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8e78-104">SYNTAX</span></span>

### <span data-ttu-id="b8e78-105">ByVirtualWanObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8e78-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e78-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="b8e78-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e78-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8e78-107">DESCRIPTION</span></span>
<span data-ttu-id="b8e78-108">Cria um recurso do Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b8e78-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="b8e78-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8e78-109">EXAMPLES</span></span>

### <span data-ttu-id="b8e78-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8e78-110">Example 1</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="b8e78-111">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e78-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="b8e78-112">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="b8e78-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="b8e78-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b8e78-113">Example 2</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="b8e78-114">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e78-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="b8e78-115">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="b8e78-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="b8e78-116">Este exemplo é semelhante ao exemplo 1, mas usa uma ID de recurso para fazer referência à rede WAN virtual necessária para criar o Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="b8e78-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="b8e78-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b8e78-117">Example 3</span></span>

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
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="b8e78-118">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e78-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="b8e78-119">O Hub virtual terá o espaço de endereço "10.0.1.0/24" e uma tabela de rota anexada.</span><span class="sxs-lookup"><span data-stu-id="b8e78-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="b8e78-120">Este exemplo é semelhante ao exemplo 2, mas também anexa uma tabela de rota ao Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="b8e78-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="b8e78-121">OS</span><span class="sxs-lookup"><span data-stu-id="b8e78-121">PARAMETERS</span></span>

### <span data-ttu-id="b8e78-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b8e78-122">-AddressPrefix</span></span>
<span data-ttu-id="b8e78-123">A cadeia de caracteres de espaço de endereço para esse Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="b8e78-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="b8e78-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8e78-124">-AsJob</span></span>
<span data-ttu-id="b8e78-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b8e78-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e78-126">-DefaultProfile</span></span>
<span data-ttu-id="b8e78-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e78-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8e78-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b8e78-128">-HubVnetConnection</span></span>
<span data-ttu-id="b8e78-129">As conexões de rede virtual Hub associadas a esse Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="b8e78-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-130">-Local</span><span class="sxs-lookup"><span data-stu-id="b8e78-130">-Location</span></span>
<span data-ttu-id="b8e78-131">ponto.</span><span class="sxs-lookup"><span data-stu-id="b8e78-131">location.</span></span>

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

### <span data-ttu-id="b8e78-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8e78-132">-Name</span></span>
<span data-ttu-id="b8e78-133">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b8e78-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e78-134">-ResourceGroupName</span></span>
<span data-ttu-id="b8e78-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8e78-135">The resource group name.</span></span>

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

### <span data-ttu-id="b8e78-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b8e78-136">-RouteTable</span></span>
<span data-ttu-id="b8e78-137">A tabela de rotas associada a este Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="b8e78-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="b8e78-138">-Tag</span></span>
<span data-ttu-id="b8e78-139">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8e78-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="b8e78-140">-VirtualWan</span></span>
<span data-ttu-id="b8e78-141">O objeto de WAN virtual ao qual esse Hub está vinculado.</span><span class="sxs-lookup"><span data-stu-id="b8e78-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="b8e78-142">-VirtualWanId</span></span>
<span data-ttu-id="b8e78-143">A ID do objeto de WAN virtual ao qual este Hub está vinculado.</span><span class="sxs-lookup"><span data-stu-id="b8e78-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8e78-144">-Confirm</span></span>
<span data-ttu-id="b8e78-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8e78-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e78-146">-WhatIf</span></span>
<span data-ttu-id="b8e78-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8e78-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e78-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8e78-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e78-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e78-149">CommonParameters</span></span>
<span data-ttu-id="b8e78-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8e78-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e78-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e78-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e78-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8e78-152">INPUTS</span></span>

### <span data-ttu-id="b8e78-153">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b8e78-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="b8e78-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b8e78-154">System.String</span></span>

## <span data-ttu-id="b8e78-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8e78-155">OUTPUTS</span></span>

### <span data-ttu-id="b8e78-156">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b8e78-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b8e78-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8e78-157">NOTES</span></span>

## <span data-ttu-id="b8e78-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8e78-158">RELATED LINKS</span></span>

[<span data-ttu-id="b8e78-159">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b8e78-159">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="b8e78-160">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b8e78-160">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="b8e78-161">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b8e78-161">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
