---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 385301bf9cab32474aea59937de09003356a5798
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886202"
---
# <span data-ttu-id="068e8-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="068e8-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="068e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="068e8-102">SYNOPSIS</span></span>
<span data-ttu-id="068e8-103">Cria o ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="068e8-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="068e8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="068e8-104">SYNTAX</span></span>

### <span data-ttu-id="068e8-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="068e8-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068e8-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="068e8-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068e8-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="068e8-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068e8-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="068e8-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068e8-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="068e8-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="068e8-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="068e8-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="068e8-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="068e8-111">DESCRIPTION</span></span>
<span data-ttu-id="068e8-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet cria ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="068e8-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="068e8-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="068e8-113">EXAMPLES</span></span>

### <span data-ttu-id="068e8-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="068e8-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="068e8-115">Nome : workspaceEndpoint Tipo : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address : Scope : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } } }</span><span class="sxs-lookup"><span data-stu-id="068e8-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="068e8-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="068e8-116">PARAMETERS</span></span>

### <span data-ttu-id="068e8-117">-Address</span><span class="sxs-lookup"><span data-stu-id="068e8-117">-Address</span></span>
<span data-ttu-id="068e8-118">Endereço do ponto de extremidade do monitor de conexão (IP ou nome de domínio).</span><span class="sxs-lookup"><span data-stu-id="068e8-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="068e8-119">-AzureSubnet</span></span>
<span data-ttu-id="068e8-120">Opção de ponto de extremidade da Sub-rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="068e8-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="068e8-121">-AzureVM</span></span>
<span data-ttu-id="068e8-122">Opção de ponto de extremidade VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="068e8-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="068e8-123">-AzureVNet</span></span>
<span data-ttu-id="068e8-124">Opção de ponto de extremidade do Azure Vnet.</span><span class="sxs-lookup"><span data-stu-id="068e8-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="068e8-125">-CoverageLevel</span></span>
<span data-ttu-id="068e8-126">Teste a cobertura do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="068e8-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="068e8-127">Os valores suportados são Default, Low, BelowAverage, Average, AboveAvergae, Full.</span><span class="sxs-lookup"><span data-stu-id="068e8-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068e8-128">-DefaultProfile</span></span>
<span data-ttu-id="068e8-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="068e8-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="068e8-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="068e8-130">-ExcludeItem</span></span>
<span data-ttu-id="068e8-131">Lista de itens que precisam ser excluídos do escopo do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="068e8-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="068e8-132">-ExternalAddress</span></span>
<span data-ttu-id="068e8-133">Opção de ponto de extremidade endereço externo.</span><span class="sxs-lookup"><span data-stu-id="068e8-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="068e8-134">-IncludeItem</span></span>
<span data-ttu-id="068e8-135">Lista de itens que precisam ser incluídos no escopo de endpont.</span><span class="sxs-lookup"><span data-stu-id="068e8-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="068e8-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="068e8-137">Opção de ponto de extremidade do MMA Workspace Machine.</span><span class="sxs-lookup"><span data-stu-id="068e8-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="068e8-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="068e8-139">Opção de ponto de extremidade MMA Workspace Network.</span><span class="sxs-lookup"><span data-stu-id="068e8-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-140">-Name</span><span class="sxs-lookup"><span data-stu-id="068e8-140">-Name</span></span>
<span data-ttu-id="068e8-141">O nome do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="068e8-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="068e8-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="068e8-142">-ResourceId</span></span>
<span data-ttu-id="068e8-143">ID do recurso do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="068e8-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068e8-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="068e8-144">-Confirm</span></span>
<span data-ttu-id="068e8-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="068e8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="068e8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="068e8-146">-WhatIf</span></span>
<span data-ttu-id="068e8-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="068e8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="068e8-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="068e8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="068e8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068e8-149">CommonParameters</span></span>
<span data-ttu-id="068e8-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="068e8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068e8-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="068e8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068e8-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="068e8-152">INPUTS</span></span>

### <span data-ttu-id="068e8-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="068e8-153">None</span></span>

## <span data-ttu-id="068e8-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="068e8-154">OUTPUTS</span></span>

### <span data-ttu-id="068e8-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="068e8-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="068e8-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="068e8-156">NOTES</span></span>

## <span data-ttu-id="068e8-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="068e8-157">RELATED LINKS</span></span>
