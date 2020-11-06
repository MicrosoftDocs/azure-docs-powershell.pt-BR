---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
ms.openlocfilehash: 188d449e47155739b4bc532c12b0e9193781c7c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431329"
---
# <span data-ttu-id="36261-101">Update-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36261-101">Update-AzureRmVirtualHub</span></span>

## <span data-ttu-id="36261-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36261-102">SYNOPSIS</span></span>
<span data-ttu-id="36261-103">Atualiza um hub virtual para um estado de meta pretendido.</span><span class="sxs-lookup"><span data-stu-id="36261-103">Updates a Virtual Hub to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36261-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36261-104">SYNTAX</span></span>

### <span data-ttu-id="36261-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="36261-105">ByVirtualHubName (Default)</span></span>
```
Update-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36261-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="36261-106">ByVirtualHubResourceId</span></span>
```
Update-AzureRmVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36261-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="36261-107">ByVirtualHubObject</span></span>
```
Update-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36261-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36261-108">DESCRIPTION</span></span>
<span data-ttu-id="36261-109">Atualiza um hub virtual para um estado de meta pretendido.</span><span class="sxs-lookup"><span data-stu-id="36261-109">Updates a Virtual Hub to an intended goal state.</span></span>

## <span data-ttu-id="36261-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36261-110">EXAMPLES</span></span>

### <span data-ttu-id="36261-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36261-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="36261-112">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="36261-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="36261-113">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="36261-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="36261-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="36261-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="36261-115">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="36261-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="36261-116">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="36261-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="36261-117">Este exemplo é semelhante ao exemplo 1, mas também anexa uma tabela de rota ao Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="36261-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="36261-118">OS</span><span class="sxs-lookup"><span data-stu-id="36261-118">PARAMETERS</span></span>

### <span data-ttu-id="36261-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="36261-119">-AddressPrefix</span></span>
<span data-ttu-id="36261-120">A cadeia de caracteres de espaço de endereço para esse Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="36261-120">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36261-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36261-121">-AsJob</span></span>
<span data-ttu-id="36261-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="36261-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36261-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36261-123">-DefaultProfile</span></span>
<span data-ttu-id="36261-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36261-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36261-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="36261-125">-HubVnetConnection</span></span>
<span data-ttu-id="36261-126">As conexões de rede virtual Hub associadas a esse Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="36261-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="36261-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36261-127">-InputObject</span></span>
<span data-ttu-id="36261-128">O objeto de Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="36261-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36261-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="36261-129">-Name</span></span>
<span data-ttu-id="36261-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="36261-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36261-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36261-131">-ResourceGroupName</span></span>
<span data-ttu-id="36261-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36261-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36261-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36261-133">-ResourceId</span></span>
<span data-ttu-id="36261-134">A ID do recurso do Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="36261-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36261-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="36261-135">-RouteTable</span></span>
<span data-ttu-id="36261-136">A tabela de rotas associada a este Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="36261-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="36261-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="36261-137">-Tag</span></span>
<span data-ttu-id="36261-138">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="36261-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="36261-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36261-139">-Confirm</span></span>
<span data-ttu-id="36261-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36261-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36261-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36261-141">-WhatIf</span></span>
<span data-ttu-id="36261-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36261-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36261-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36261-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36261-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36261-144">CommonParameters</span></span>
<span data-ttu-id="36261-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36261-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36261-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36261-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36261-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36261-147">INPUTS</span></span>

### <span data-ttu-id="36261-148">System. String</span><span class="sxs-lookup"><span data-stu-id="36261-148">System.String</span></span>

### <span data-ttu-id="36261-149">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36261-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="36261-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36261-150">OUTPUTS</span></span>

### <span data-ttu-id="36261-151">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36261-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="36261-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36261-152">NOTES</span></span>

## <span data-ttu-id="36261-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36261-153">RELATED LINKS</span></span>
