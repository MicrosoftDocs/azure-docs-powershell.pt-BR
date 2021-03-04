---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: 77288758af2f0f3294d8f32c92b7f687dab79a97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886904"
---
# <span data-ttu-id="45ef2-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45ef2-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="45ef2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="45ef2-103">Cria um recurso de tabela de rota de hub associado a um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="45ef2-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="45ef2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45ef2-104">SYNTAX</span></span>

### <span data-ttu-id="45ef2-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="45ef2-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ef2-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="45ef2-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ef2-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="45ef2-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45ef2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45ef2-108">DESCRIPTION</span></span>
<span data-ttu-id="45ef2-109">Cria a tabela de rota especificada associada ao hub virtual especificado com as rotas fornecidas e os rótulos.</span><span class="sxs-lookup"><span data-stu-id="45ef2-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="45ef2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45ef2-110">EXAMPLES</span></span>

### <span data-ttu-id="45ef2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45ef2-111">Example 1</span></span>

```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="45ef2-112">Este comando cria uma tabela de rota de hub do hub virtual.</span><span class="sxs-lookup"><span data-stu-id="45ef2-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="45ef2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45ef2-113">PARAMETERS</span></span>

### <span data-ttu-id="45ef2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45ef2-114">-AsJob</span></span>
<span data-ttu-id="45ef2-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="45ef2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45ef2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ef2-116">-DefaultProfile</span></span>
<span data-ttu-id="45ef2-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45ef2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ef2-118">-Label</span><span class="sxs-lookup"><span data-stu-id="45ef2-118">-Label</span></span>
<span data-ttu-id="45ef2-119">A lista de rótulos.</span><span class="sxs-lookup"><span data-stu-id="45ef2-119">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ef2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="45ef2-120">-Name</span></span>
<span data-ttu-id="45ef2-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="45ef2-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ef2-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="45ef2-122">-ParentObject</span></span>
<span data-ttu-id="45ef2-123">O objeto hub virtual pai desse recurso.</span><span class="sxs-lookup"><span data-stu-id="45ef2-123">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45ef2-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="45ef2-124">-ParentResourceName</span></span>
<span data-ttu-id="45ef2-125">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="45ef2-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ef2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45ef2-126">-ResourceGroupName</span></span>
<span data-ttu-id="45ef2-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45ef2-127">The resource group name.</span></span>

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

### <span data-ttu-id="45ef2-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="45ef2-128">-ParentResourceId</span></span>
<span data-ttu-id="45ef2-129">A id de recurso do recurso de hub virtual.</span><span class="sxs-lookup"><span data-stu-id="45ef2-129">The resource id of the virtual hub resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45ef2-130">-Route</span><span class="sxs-lookup"><span data-stu-id="45ef2-130">-Route</span></span>
<span data-ttu-id="45ef2-131">A lista de rotas para esta tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="45ef2-131">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ef2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45ef2-132">-Confirm</span></span>
<span data-ttu-id="45ef2-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ef2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ef2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ef2-134">-WhatIf</span></span>
<span data-ttu-id="45ef2-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45ef2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ef2-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45ef2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ef2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ef2-137">CommonParameters</span></span>
<span data-ttu-id="45ef2-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ef2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ef2-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45ef2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ef2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45ef2-140">INPUTS</span></span>

### <span data-ttu-id="45ef2-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="45ef2-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="45ef2-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45ef2-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="45ef2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="45ef2-143">System.String</span></span>

## <span data-ttu-id="45ef2-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45ef2-144">OUTPUTS</span></span>

### <span data-ttu-id="45ef2-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45ef2-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="45ef2-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="45ef2-146">NOTES</span></span>

## <span data-ttu-id="45ef2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45ef2-147">RELATED LINKS</span></span>

[<span data-ttu-id="45ef2-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45ef2-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="45ef2-149">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="45ef2-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="45ef2-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45ef2-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="45ef2-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45ef2-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
