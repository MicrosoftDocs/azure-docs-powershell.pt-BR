---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427537"
---
# <span data-ttu-id="6dd01-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6dd01-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="6dd01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6dd01-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd01-103">Cria um recurso de tabela de rota de Hub associado a um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="6dd01-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="6dd01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dd01-104">SYNTAX</span></span>

### <span data-ttu-id="6dd01-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6dd01-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd01-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="6dd01-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dd01-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="6dd01-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dd01-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6dd01-108">DESCRIPTION</span></span>
<span data-ttu-id="6dd01-109">Cria a tabela de rota especificada que está associada ao Hub virtual especificado com as rotas fornecidas e os rótulos.</span><span class="sxs-lookup"><span data-stu-id="6dd01-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="6dd01-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6dd01-110">EXAMPLES</span></span>

### <span data-ttu-id="6dd01-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6dd01-111">Example 1</span></span>

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

<span data-ttu-id="6dd01-112">Esse comando cria uma tabela de rota do Hub do Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="6dd01-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="6dd01-113">OS</span><span class="sxs-lookup"><span data-stu-id="6dd01-113">PARAMETERS</span></span>

### <span data-ttu-id="6dd01-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dd01-114">-AsJob</span></span>
<span data-ttu-id="6dd01-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6dd01-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6dd01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd01-116">-DefaultProfile</span></span>
<span data-ttu-id="6dd01-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd01-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dd01-118">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="6dd01-118">-Label</span></span>
<span data-ttu-id="6dd01-119">A lista de etiquetas.</span><span class="sxs-lookup"><span data-stu-id="6dd01-119">The list of labels.</span></span>

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

### <span data-ttu-id="6dd01-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dd01-120">-Name</span></span>
<span data-ttu-id="6dd01-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6dd01-121">The resource name.</span></span>

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

### <span data-ttu-id="6dd01-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6dd01-122">-ParentObject</span></span>
<span data-ttu-id="6dd01-123">O objeto Hub virtual pai deste recurso.</span><span class="sxs-lookup"><span data-stu-id="6dd01-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="6dd01-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6dd01-124">-ParentResourceName</span></span>
<span data-ttu-id="6dd01-125">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="6dd01-125">The parent resource name.</span></span>

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

### <span data-ttu-id="6dd01-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd01-126">-ResourceGroupName</span></span>
<span data-ttu-id="6dd01-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6dd01-127">The resource group name.</span></span>

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

### <span data-ttu-id="6dd01-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6dd01-128">-ParentResourceId</span></span>
<span data-ttu-id="6dd01-129">A ID do recurso do Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="6dd01-129">The resource id of the virtual hub resource.</span></span>

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

### <span data-ttu-id="6dd01-130">-Rota</span><span class="sxs-lookup"><span data-stu-id="6dd01-130">-Route</span></span>
<span data-ttu-id="6dd01-131">A lista de rotas para esta tabela de rotas.</span><span class="sxs-lookup"><span data-stu-id="6dd01-131">The list of routes for this route table.</span></span>

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

### <span data-ttu-id="6dd01-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6dd01-132">-Confirm</span></span>
<span data-ttu-id="6dd01-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd01-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dd01-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd01-134">-WhatIf</span></span>
<span data-ttu-id="6dd01-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6dd01-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd01-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6dd01-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dd01-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd01-137">CommonParameters</span></span>
<span data-ttu-id="6dd01-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd01-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd01-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dd01-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd01-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6dd01-140">INPUTS</span></span>

### <span data-ttu-id="6dd01-141">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6dd01-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="6dd01-142">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6dd01-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="6dd01-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6dd01-143">System.String</span></span>

## <span data-ttu-id="6dd01-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6dd01-144">OUTPUTS</span></span>

### <span data-ttu-id="6dd01-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6dd01-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="6dd01-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6dd01-146">NOTES</span></span>

## <span data-ttu-id="6dd01-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6dd01-147">RELATED LINKS</span></span>

[<span data-ttu-id="6dd01-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6dd01-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="6dd01-149">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="6dd01-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="6dd01-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6dd01-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="6dd01-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6dd01-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
