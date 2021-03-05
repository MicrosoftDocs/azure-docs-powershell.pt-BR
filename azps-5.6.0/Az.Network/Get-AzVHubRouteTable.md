---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 83758842fe91ef6cf8fca24f360750f813a31311
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901605"
---
# <span data-ttu-id="3ed54-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ed54-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="3ed54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ed54-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed54-103">Recupera um recurso de tabela de rota de hub associado a um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="3ed54-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="3ed54-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ed54-104">SYNTAX</span></span>

### <span data-ttu-id="3ed54-105">ByVHubRouteTableName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ed54-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed54-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="3ed54-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed54-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="3ed54-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ed54-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ed54-108">DESCRIPTION</span></span>
<span data-ttu-id="3ed54-109">Obtém a tabela de rota de hub especificada associada ao hub virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="3ed54-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="3ed54-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ed54-110">EXAMPLES</span></span>

### <span data-ttu-id="3ed54-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ed54-111">Example 1</span></span>

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

<span data-ttu-id="3ed54-112">Este comando obtém a tabela de rota de hub do hub virtual.</span><span class="sxs-lookup"><span data-stu-id="3ed54-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="3ed54-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3ed54-113">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName


Name                   : defaultRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []


Name                   : noneRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : []
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="3ed54-114">Este comando lista todas as tabelas de rota de hub no VirtualHub especificado.</span><span class="sxs-lookup"><span data-stu-id="3ed54-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="3ed54-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ed54-115">PARAMETERS</span></span>

### <span data-ttu-id="3ed54-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ed54-116">-AsJob</span></span>
<span data-ttu-id="3ed54-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3ed54-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ed54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed54-118">-DefaultProfile</span></span>
<span data-ttu-id="3ed54-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ed54-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ed54-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3ed54-120">-Name</span></span>
<span data-ttu-id="3ed54-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3ed54-121">The resource name.</span></span>

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

### <span data-ttu-id="3ed54-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3ed54-122">-ParentObject</span></span>
<span data-ttu-id="3ed54-123">O objeto hub virtual pai desse recurso.</span><span class="sxs-lookup"><span data-stu-id="3ed54-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="3ed54-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3ed54-124">-ParentResourceName</span></span>
<span data-ttu-id="3ed54-125">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="3ed54-125">The parent resource name.</span></span>

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

### <span data-ttu-id="3ed54-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed54-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ed54-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ed54-127">The resource group name.</span></span>

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

### <span data-ttu-id="3ed54-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ed54-128">-ResourceId</span></span>
<span data-ttu-id="3ed54-129">A id de recurso do recurso vhubroutetable para Obter.</span><span class="sxs-lookup"><span data-stu-id="3ed54-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="3ed54-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ed54-130">-Confirm</span></span>
<span data-ttu-id="3ed54-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ed54-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed54-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed54-132">-WhatIf</span></span>
<span data-ttu-id="3ed54-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ed54-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed54-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ed54-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed54-135">CommonParameters</span></span>
<span data-ttu-id="3ed54-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ed54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed54-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ed54-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed54-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ed54-138">INPUTS</span></span>

### <span data-ttu-id="3ed54-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3ed54-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3ed54-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3ed54-140">System.String</span></span>

## <span data-ttu-id="3ed54-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ed54-141">OUTPUTS</span></span>

### <span data-ttu-id="3ed54-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ed54-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="3ed54-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ed54-143">NOTES</span></span>

## <span data-ttu-id="3ed54-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ed54-144">RELATED LINKS</span></span>

[<span data-ttu-id="3ed54-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="3ed54-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="3ed54-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ed54-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="3ed54-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ed54-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="3ed54-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ed54-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)