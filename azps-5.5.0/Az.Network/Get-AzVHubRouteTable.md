---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVHubRouteTable.md
ms.openlocfilehash: 3461d629eac47a1bbf2842d2cb0a913c2734f94e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117445"
---
# <span data-ttu-id="4bdd9-101">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bdd9-101">Get-AzVHubRouteTable</span></span>

## <span data-ttu-id="4bdd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bdd9-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdd9-103">Recupera um recurso de tabela de rotação de hub associado a um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-103">Retrieves  a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="4bdd9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bdd9-104">SYNTAX</span></span>

### <span data-ttu-id="4bdd9-105">ByVHubRouteTableName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4bdd9-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Get-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdd9-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="4bdd9-106">ByVirtualHubObject</span></span>
```powershell
Get-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdd9-107">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="4bdd9-107">ByVHubRouteTableResourceId</span></span>
```powershell
Get-AzVHubRouteTable -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bdd9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bdd9-108">DESCRIPTION</span></span>
<span data-ttu-id="4bdd9-109">Obtém a tabela de rota do hub especificada associada ao hub virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-109">Gets the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="4bdd9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4bdd9-110">EXAMPLES</span></span>

### <span data-ttu-id="4bdd9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bdd9-111">Example 1</span></span>

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

<span data-ttu-id="4bdd9-112">Esse comando obtém a tabela de rota do hub do hub virtual.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-112">This command gets the hub route table of the virtual hub.</span></span>

### <span data-ttu-id="4bdd9-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4bdd9-113">Example 2</span></span>

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

<span data-ttu-id="4bdd9-114">Esse comando lista todas as tabelas de rota do hub no VirtualHub especificado.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-114">This command lists all the hub route tables in the specified VirtualHub.</span></span>

## <span data-ttu-id="4bdd9-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bdd9-115">PARAMETERS</span></span>

### <span data-ttu-id="4bdd9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bdd9-116">-AsJob</span></span>
<span data-ttu-id="4bdd9-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4bdd9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bdd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdd9-118">-DefaultProfile</span></span>
<span data-ttu-id="4bdd9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bdd9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bdd9-120">-Name</span></span>
<span data-ttu-id="4bdd9-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-121">The resource name.</span></span>

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

### <span data-ttu-id="4bdd9-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4bdd9-122">-ParentObject</span></span>
<span data-ttu-id="4bdd9-123">O objeto do hub virtual pai desse recurso.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="4bdd9-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4bdd9-124">-ParentResourceName</span></span>
<span data-ttu-id="4bdd9-125">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-125">The parent resource name.</span></span>

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

### <span data-ttu-id="4bdd9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdd9-126">-ResourceGroupName</span></span>
<span data-ttu-id="4bdd9-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-127">The resource group name.</span></span>

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

### <span data-ttu-id="4bdd9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bdd9-128">-ResourceId</span></span>
<span data-ttu-id="4bdd9-129">A ID de recurso do recurso que você pode obter.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-129">The resource id of the vhubroutetable resource to Get.</span></span>

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

### <span data-ttu-id="4bdd9-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4bdd9-130">-Confirm</span></span>
<span data-ttu-id="4bdd9-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bdd9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdd9-132">-WhatIf</span></span>
<span data-ttu-id="4bdd9-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bdd9-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bdd9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdd9-135">CommonParameters</span></span>
<span data-ttu-id="4bdd9-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bdd9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdd9-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bdd9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdd9-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="4bdd9-138">INPUTS</span></span>

### <span data-ttu-id="4bdd9-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4bdd9-139">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4bdd9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4bdd9-140">System.String</span></span>

## <span data-ttu-id="4bdd9-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="4bdd9-141">OUTPUTS</span></span>

### <span data-ttu-id="4bdd9-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bdd9-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="4bdd9-143">Notas</span><span class="sxs-lookup"><span data-stu-id="4bdd9-143">NOTES</span></span>

## <span data-ttu-id="4bdd9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bdd9-144">RELATED LINKS</span></span>

[<span data-ttu-id="4bdd9-145">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="4bdd9-145">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="4bdd9-146">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bdd9-146">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="4bdd9-147">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bdd9-147">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)

[<span data-ttu-id="4bdd9-148">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bdd9-148">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)