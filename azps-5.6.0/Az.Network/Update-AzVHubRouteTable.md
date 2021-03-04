---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: b3b4fe711cbccd195f4549ae936fe438185c9070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885335"
---
# <span data-ttu-id="31a27-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31a27-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="31a27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31a27-102">SYNOPSIS</span></span>
<span data-ttu-id="31a27-103">Exclua um recurso de tabela de rota de hub associado a um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="31a27-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="31a27-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="31a27-104">SYNTAX</span></span>

### <span data-ttu-id="31a27-105">ByVHubRouteTableName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="31a27-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a27-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="31a27-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a27-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="31a27-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a27-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="31a27-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a27-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="31a27-109">DESCRIPTION</span></span>
<span data-ttu-id="31a27-110">Atualiza a tabela de rota especificada associada ao hub virtual especificado com as rotas fornecidas ou os rótulos.</span><span class="sxs-lookup"><span data-stu-id="31a27-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="31a27-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31a27-111">EXAMPLES</span></span>

### <span data-ttu-id="31a27-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31a27-112">Example 1</span></span>
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
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="31a27-113">Esse comando exclui a tabela de rota do hub do hub virtual.</span><span class="sxs-lookup"><span data-stu-id="31a27-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="31a27-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="31a27-114">PARAMETERS</span></span>

### <span data-ttu-id="31a27-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31a27-115">-AsJob</span></span>
<span data-ttu-id="31a27-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="31a27-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31a27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a27-117">-DefaultProfile</span></span>
<span data-ttu-id="31a27-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31a27-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a27-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31a27-119">-InputObject</span></span>
<span data-ttu-id="31a27-120">O recurso vhubroutetable para Update.</span><span class="sxs-lookup"><span data-stu-id="31a27-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31a27-121">-Label</span><span class="sxs-lookup"><span data-stu-id="31a27-121">-Label</span></span>
<span data-ttu-id="31a27-122">A lista de rótulos.</span><span class="sxs-lookup"><span data-stu-id="31a27-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a27-123">-Name</span><span class="sxs-lookup"><span data-stu-id="31a27-123">-Name</span></span>
<span data-ttu-id="31a27-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="31a27-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a27-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="31a27-125">-ParentObject</span></span>
<span data-ttu-id="31a27-126">O objeto hub virtual pai desse recurso.</span><span class="sxs-lookup"><span data-stu-id="31a27-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="31a27-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="31a27-127">-ParentResourceName</span></span>
<span data-ttu-id="31a27-128">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="31a27-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a27-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a27-129">-ResourceGroupName</span></span>
<span data-ttu-id="31a27-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31a27-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a27-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31a27-131">-ResourceId</span></span>
<span data-ttu-id="31a27-132">A id de recurso do recurso vhubroutetable para Update.</span><span class="sxs-lookup"><span data-stu-id="31a27-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a27-133">-Route</span><span class="sxs-lookup"><span data-stu-id="31a27-133">-Route</span></span>
<span data-ttu-id="31a27-134">A lista de rotas para esta tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="31a27-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a27-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31a27-135">-Confirm</span></span>
<span data-ttu-id="31a27-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31a27-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a27-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a27-137">-WhatIf</span></span>
<span data-ttu-id="31a27-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31a27-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31a27-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31a27-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31a27-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a27-140">CommonParameters</span></span>
<span data-ttu-id="31a27-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a27-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a27-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31a27-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a27-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31a27-143">INPUTS</span></span>

### <span data-ttu-id="31a27-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="31a27-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="31a27-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31a27-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="31a27-146">System.String</span><span class="sxs-lookup"><span data-stu-id="31a27-146">System.String</span></span>

## <span data-ttu-id="31a27-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="31a27-147">OUTPUTS</span></span>

### <span data-ttu-id="31a27-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31a27-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="31a27-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="31a27-149">NOTES</span></span>

## <span data-ttu-id="31a27-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31a27-150">RELATED LINKS</span></span>

[<span data-ttu-id="31a27-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31a27-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="31a27-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="31a27-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="31a27-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31a27-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="31a27-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="31a27-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)