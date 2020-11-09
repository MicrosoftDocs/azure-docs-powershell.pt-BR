---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: d330b7e25cc1184a3efaea2c3deb569bf44171b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284052"
---
# <span data-ttu-id="d86eb-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d86eb-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="d86eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d86eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d86eb-103">Excluir um recurso de tabela de rota de Hub associado a um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d86eb-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="d86eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d86eb-104">SYNTAX</span></span>

### <span data-ttu-id="d86eb-105">ByVHubRouteTableName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d86eb-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d86eb-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d86eb-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d86eb-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="d86eb-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d86eb-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="d86eb-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d86eb-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d86eb-109">DESCRIPTION</span></span>
<span data-ttu-id="d86eb-110">Atualiza a tabela de rotas especificada que está associada ao Hub virtual especificado com as rotas ou os rótulos fornecidos.</span><span class="sxs-lookup"><span data-stu-id="d86eb-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="d86eb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d86eb-111">EXAMPLES</span></span>

### <span data-ttu-id="d86eb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d86eb-112">Example 1</span></span>
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

<span data-ttu-id="d86eb-113">Esse comando exclui a tabela de rota do Hub do Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="d86eb-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="d86eb-114">OS</span><span class="sxs-lookup"><span data-stu-id="d86eb-114">PARAMETERS</span></span>

### <span data-ttu-id="d86eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d86eb-115">-AsJob</span></span>
<span data-ttu-id="d86eb-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d86eb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d86eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86eb-117">-DefaultProfile</span></span>
<span data-ttu-id="d86eb-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d86eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d86eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d86eb-119">-InputObject</span></span>
<span data-ttu-id="d86eb-120">O recurso vhubroutetable a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d86eb-120">The vhubroutetable resource to Update.</span></span>

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

### <span data-ttu-id="d86eb-121">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="d86eb-121">-Label</span></span>
<span data-ttu-id="d86eb-122">A lista de etiquetas.</span><span class="sxs-lookup"><span data-stu-id="d86eb-122">The list of labels.</span></span>

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

### <span data-ttu-id="d86eb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d86eb-123">-Name</span></span>
<span data-ttu-id="d86eb-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d86eb-124">The resource name.</span></span>

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

### <span data-ttu-id="d86eb-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d86eb-125">-ParentObject</span></span>
<span data-ttu-id="d86eb-126">O objeto Hub virtual pai deste recurso.</span><span class="sxs-lookup"><span data-stu-id="d86eb-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="d86eb-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d86eb-127">-ParentResourceName</span></span>
<span data-ttu-id="d86eb-128">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="d86eb-128">The parent resource name.</span></span>

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

### <span data-ttu-id="d86eb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d86eb-129">-ResourceGroupName</span></span>
<span data-ttu-id="d86eb-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86eb-130">The resource group name.</span></span>

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

### <span data-ttu-id="d86eb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d86eb-131">-ResourceId</span></span>
<span data-ttu-id="d86eb-132">A ID do recurso do recurso vhubroutetable a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d86eb-132">The resource id of the vhubroutetable resource to Update.</span></span>

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

### <span data-ttu-id="d86eb-133">-Rota</span><span class="sxs-lookup"><span data-stu-id="d86eb-133">-Route</span></span>
<span data-ttu-id="d86eb-134">A lista de rotas para esta tabela de rotas.</span><span class="sxs-lookup"><span data-stu-id="d86eb-134">The list of routes for this route table.</span></span>

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

### <span data-ttu-id="d86eb-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d86eb-135">-Confirm</span></span>
<span data-ttu-id="d86eb-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d86eb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d86eb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d86eb-137">-WhatIf</span></span>
<span data-ttu-id="d86eb-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d86eb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d86eb-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d86eb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d86eb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86eb-140">CommonParameters</span></span>
<span data-ttu-id="d86eb-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d86eb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86eb-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d86eb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86eb-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d86eb-143">INPUTS</span></span>

### <span data-ttu-id="d86eb-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d86eb-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d86eb-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d86eb-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="d86eb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d86eb-146">System.String</span></span>

## <span data-ttu-id="d86eb-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d86eb-147">OUTPUTS</span></span>

### <span data-ttu-id="d86eb-148">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d86eb-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="d86eb-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d86eb-149">NOTES</span></span>

## <span data-ttu-id="d86eb-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d86eb-150">RELATED LINKS</span></span>

[<span data-ttu-id="d86eb-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d86eb-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="d86eb-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="d86eb-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="d86eb-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d86eb-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="d86eb-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d86eb-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)