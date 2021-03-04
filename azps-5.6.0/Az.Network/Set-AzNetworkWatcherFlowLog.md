---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 69ac1db81294a88f087ab036fd9bc0206a768e7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888823"
---
# <span data-ttu-id="c5365-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c5365-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="c5365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5365-102">SYNOPSIS</span></span>
<span data-ttu-id="c5365-103">Atualiza o recurso de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-103">Updates flow log resource.</span></span>

## <span data-ttu-id="c5365-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c5365-104">SYNTAX</span></span>

### <span data-ttu-id="c5365-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c5365-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5365-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c5365-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5365-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="c5365-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5365-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="c5365-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5365-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c5365-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5365-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="c5365-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5365-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5365-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5365-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="c5365-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5365-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c5365-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5365-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c5365-114">DESCRIPTION</span></span>
<span data-ttu-id="c5365-115">Atualiza o recurso de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-115">Updates flow log resource.</span></span>

## <span data-ttu-id="c5365-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5365-116">EXAMPLES</span></span>

### <span data-ttu-id="c5365-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5365-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="c5365-118">Nome : id do pstest : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/bbbbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbb-1bbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled : True RetentionPolicy : { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span><span class="sxs-lookup"><span data-stu-id="c5365-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="c5365-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c5365-119">PARAMETERS</span></span>

### <span data-ttu-id="c5365-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5365-120">-DefaultProfile</span></span>
<span data-ttu-id="c5365-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5365-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5365-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="c5365-122">-Enabled</span></span>
<span data-ttu-id="c5365-123">Sinalizador para habilitar/desabilitar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="c5365-124">-EnableRetention</span></span>
<span data-ttu-id="c5365-125">Sinalizador para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="c5365-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="c5365-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="c5365-127">Sinalizador para habilitar/desabilitar TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="c5365-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-128">-Force</span><span class="sxs-lookup"><span data-stu-id="c5365-128">-Force</span></span>
<span data-ttu-id="c5365-129">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="c5365-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c5365-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="c5365-130">-FormatType</span></span>
<span data-ttu-id="c5365-131">O tipo de arquivo de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-131">The file type of flow log.</span></span>
<span data-ttu-id="c5365-132">O único valor suportado agora é 'JSON'.</span><span class="sxs-lookup"><span data-stu-id="c5365-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="c5365-133">-FormatVersion</span></span>
<span data-ttu-id="c5365-134">A versão (revisão) do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5365-135">-InputObject</span></span>
<span data-ttu-id="c5365-136">Objeto Flow lof.</span><span class="sxs-lookup"><span data-stu-id="c5365-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-137">-Location</span><span class="sxs-lookup"><span data-stu-id="c5365-137">-Location</span></span>
<span data-ttu-id="c5365-138">Local do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="c5365-138">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-139">-Name</span><span class="sxs-lookup"><span data-stu-id="c5365-139">-Name</span></span>
<span data-ttu-id="c5365-140">O nome do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5365-141">-NetworkWatcher</span></span>
<span data-ttu-id="c5365-142">O recurso do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="c5365-142">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c5365-143">-NetworkWatcherName</span></span>
<span data-ttu-id="c5365-144">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="c5365-144">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5365-145">-ResourceGroupName</span></span>
<span data-ttu-id="c5365-146">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="c5365-146">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5365-147">-ResourceId</span></span>
<span data-ttu-id="c5365-148">ID do recurso FlowLog.</span><span class="sxs-lookup"><span data-stu-id="c5365-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="c5365-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="c5365-150">Número de dias para reter registros de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="c5365-151">-StorageId</span></span>
<span data-ttu-id="c5365-152">ID da conta de armazenamento usada para armazenar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5365-153">-Tag</span></span>
<span data-ttu-id="c5365-154">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c5365-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c5365-155">-TargetResourceId</span></span>
<span data-ttu-id="c5365-156">ID do grupo de segurança de rede ao qual o log de fluxo será aplicado.</span><span class="sxs-lookup"><span data-stu-id="c5365-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="c5365-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="c5365-158">O intervalo em minutos que decidiria com que frequência o serviço TA deve fazer análise de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5365-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="c5365-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="c5365-160">ID de recurso do espaço de trabalho anexado.</span><span class="sxs-lookup"><span data-stu-id="c5365-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5365-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5365-161">-Confirm</span></span>
<span data-ttu-id="c5365-162">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5365-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5365-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5365-163">-WhatIf</span></span>
<span data-ttu-id="c5365-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5365-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5365-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5365-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5365-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5365-166">CommonParameters</span></span>
<span data-ttu-id="c5365-167">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5365-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5365-168">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5365-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5365-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5365-169">INPUTS</span></span>

### <span data-ttu-id="c5365-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5365-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c5365-171">System.String</span><span class="sxs-lookup"><span data-stu-id="c5365-171">System.String</span></span>

### <span data-ttu-id="c5365-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="c5365-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="c5365-173">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c5365-173">OUTPUTS</span></span>

### <span data-ttu-id="c5365-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="c5365-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="c5365-175">NOTES</span><span class="sxs-lookup"><span data-stu-id="c5365-175">NOTES</span></span>

## <span data-ttu-id="c5365-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5365-176">RELATED LINKS</span></span>

[<span data-ttu-id="c5365-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5365-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c5365-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5365-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c5365-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5365-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c5365-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c5365-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c5365-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c5365-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c5365-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c5365-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c5365-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c5365-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c5365-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c5365-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c5365-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c5365-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c5365-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c5365-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c5365-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c5365-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c5365-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c5365-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c5365-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5365-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c5365-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c5365-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c5365-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c5365-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c5365-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5365-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5365-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5365-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5365-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5365-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5365-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c5365-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c5365-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5365-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5365-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5365-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5365-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c5365-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c5365-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c5365-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c5365-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c5365-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c5365-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c5365-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c5365-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c5365-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c5365-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5365-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="c5365-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c5365-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="c5365-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c5365-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="c5365-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c5365-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
