---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: a23b2ce975a67a87a5edd58b21835e16f812055b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887872"
---
# <span data-ttu-id="02c25-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="02c25-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="02c25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c25-102">SYNOPSIS</span></span>
<span data-ttu-id="02c25-103">Modifica um Hub Virtual para adicionar uma Tabela de Rota virtual do HUb a ele.</span><span class="sxs-lookup"><span data-stu-id="02c25-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="02c25-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="02c25-104">SYNTAX</span></span>

### <span data-ttu-id="02c25-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="02c25-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02c25-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="02c25-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c25-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="02c25-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c25-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="02c25-108">DESCRIPTION</span></span>
<span data-ttu-id="02c25-109">{{ Preencha a Descrição }}</span><span class="sxs-lookup"><span data-stu-id="02c25-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="02c25-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02c25-110">EXAMPLES</span></span>

### <span data-ttu-id="02c25-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02c25-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="02c25-112">Primeiro, criamos um objeto Rota de Hub Virtual e o usamos para criar um recurso de Tabela de Rota de Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="02c25-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="02c25-113">Em seguida, definimos esse recurso de tabela de rota para o hub virtual usando o Set-AzVirtualHub comando.</span><span class="sxs-lookup"><span data-stu-id="02c25-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="02c25-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="02c25-114">PARAMETERS</span></span>

### <span data-ttu-id="02c25-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02c25-115">-AsJob</span></span>
<span data-ttu-id="02c25-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="02c25-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02c25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c25-117">-DefaultProfile</span></span>
<span data-ttu-id="02c25-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02c25-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c25-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c25-119">-InputObject</span></span>
<span data-ttu-id="02c25-120">O objeto de hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="02c25-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="02c25-121">-Name</span><span class="sxs-lookup"><span data-stu-id="02c25-121">-Name</span></span>
<span data-ttu-id="02c25-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="02c25-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c25-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c25-123">-ResourceGroupName</span></span>
<span data-ttu-id="02c25-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02c25-124">The resource group name.</span></span>

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

### <span data-ttu-id="02c25-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02c25-125">-ResourceId</span></span>
<span data-ttu-id="02c25-126">A id de recurso do hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="02c25-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="02c25-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="02c25-127">-RouteTable</span></span>
<span data-ttu-id="02c25-128">As tabelas de rota associadas a esse Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="02c25-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c25-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="02c25-129">-Tag</span></span>
<span data-ttu-id="02c25-130">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="02c25-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="02c25-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02c25-131">-Confirm</span></span>
<span data-ttu-id="02c25-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02c25-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c25-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c25-133">-WhatIf</span></span>
<span data-ttu-id="02c25-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02c25-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c25-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02c25-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c25-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c25-136">CommonParameters</span></span>
<span data-ttu-id="02c25-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c25-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c25-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02c25-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c25-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02c25-139">INPUTS</span></span>

### <span data-ttu-id="02c25-140">System.String</span><span class="sxs-lookup"><span data-stu-id="02c25-140">System.String</span></span>

### <span data-ttu-id="02c25-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="02c25-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="02c25-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="02c25-142">OUTPUTS</span></span>

### <span data-ttu-id="02c25-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="02c25-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="02c25-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="02c25-144">NOTES</span></span>

## <span data-ttu-id="02c25-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02c25-145">RELATED LINKS</span></span>
