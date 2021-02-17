---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 27476e310536f2bc849e66669fc80570731d21e1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408620"
---
# <span data-ttu-id="4b3e0-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4b3e0-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="4b3e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b3e0-102">SYNOPSIS</span></span>
<span data-ttu-id="4b3e0-103">Criar ou atualizar um recurso de log de fluxo para o grupo de segurança de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="4b3e0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b3e0-104">SYNTAX</span></span>

### <span data-ttu-id="4b3e0-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b3e0-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3e0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4b3e0-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3e0-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="4b3e0-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3e0-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="4b3e0-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3e0-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4b3e0-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3e0-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="4b3e0-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b3e0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b3e0-111">DESCRIPTION</span></span>
<span data-ttu-id="4b3e0-112">New-AzNetworkWatcherFlowLog comando cria ou atualiza um recurso de log de fluxo para o grupo de segurança de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="4b3e0-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b3e0-113">EXAMPLES</span></span>

### <span data-ttu-id="4b3e0-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b3e0-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="4b3e0-115">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="4b3e0-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="4b3e0-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4b3e0-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="4b3e0-117">Se você quiser desabilitar o recurso flowLog para o qual o TrafficAnalytics está configurado, também será necessário desabilitar o TrafficAnalytics.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="4b3e0-118">Isso pode ser feito como no exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="4b3e0-119">Nome : ID do teste : /subscriptions/bbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: Local bem-sucedido: eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId: /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled: False RetentionPolicy: { "Days": 0, "Enabled": false } Format: { "Type": "JSON", "Versão": 1 } FlowAnalyticsConfiguration: { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="4b3e0-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="4b3e0-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b3e0-120">PARAMETERS</span></span>

### <span data-ttu-id="4b3e0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b3e0-121">-DefaultProfile</span></span>
<span data-ttu-id="4b3e0-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b3e0-123">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="4b3e0-123">-Enabled</span></span>
<span data-ttu-id="4b3e0-124">Sinalizar para habilitar/desabilitar o registro em log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-124">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="4b3e0-125">-EnableRetention</span></span>
<span data-ttu-id="4b3e0-126">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-126">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="4b3e0-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="4b3e0-128">Sinalizar para habilitar/desabilitar o TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="4b3e0-128">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4b3e0-129">-Force</span></span>
<span data-ttu-id="4b3e0-130">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="4b3e0-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4b3e0-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="4b3e0-131">-FormatType</span></span>
<span data-ttu-id="4b3e0-132">O tipo de arquivo do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-132">The file type of flow log.</span></span>
<span data-ttu-id="4b3e0-133">O único valor com suporte agora é 'JSON'.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-133">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="4b3e0-134">-FormatVersion</span></span>
<span data-ttu-id="4b3e0-135">A versão (revisão) do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-135">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-136">-Local</span><span class="sxs-lookup"><span data-stu-id="4b3e0-136">-Location</span></span>
<span data-ttu-id="4b3e0-137">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4b3e0-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b3e0-138">-Name</span></span>
<span data-ttu-id="4b3e0-139">O nome do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-139">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b3e0-140">-NetworkWatcher</span></span>
<span data-ttu-id="4b3e0-141">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="4b3e0-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4b3e0-142">-NetworkWatcherName</span></span>
<span data-ttu-id="4b3e0-143">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="4b3e0-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b3e0-144">-ResourceGroupName</span></span>
<span data-ttu-id="4b3e0-145">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4b3e0-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="4b3e0-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="4b3e0-147">Número de dias para reter registros de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-147">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-148">-StorageId</span><span class="sxs-lookup"><span data-stu-id="4b3e0-148">-StorageId</span></span>
<span data-ttu-id="4b3e0-149">ID da conta de armazenamento usada para armazenar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-149">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b3e0-150">-Tag</span></span>
<span data-ttu-id="4b3e0-151">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-151">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4b3e0-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4b3e0-152">-TargetResourceId</span></span>
<span data-ttu-id="4b3e0-153">ID do grupo de segurança de rede ao qual o log de fluxo será aplicado.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-153">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="4b3e0-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="4b3e0-155">O intervalo em minutos que decidiria com que frequência o serviço TA deve fazer a análise de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="4b3e0-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="4b3e0-157">ID do recurso do espaço de trabalho anexado.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-157">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-158">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4b3e0-158">-Confirm</span></span>
<span data-ttu-id="4b3e0-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b3e0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b3e0-160">-WhatIf</span></span>
<span data-ttu-id="4b3e0-161">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b3e0-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b3e0-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b3e0-163">CommonParameters</span></span>
<span data-ttu-id="4b3e0-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b3e0-165">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b3e0-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b3e0-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b3e0-166">INPUTS</span></span>

### <span data-ttu-id="4b3e0-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b3e0-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="4b3e0-168">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b3e0-168">OUTPUTS</span></span>

### <span data-ttu-id="4b3e0-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="4b3e0-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="4b3e0-170">Notas</span><span class="sxs-lookup"><span data-stu-id="4b3e0-170">NOTES</span></span>

## <span data-ttu-id="4b3e0-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b3e0-171">RELATED LINKS</span></span>

[<span data-ttu-id="4b3e0-172">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b3e0-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4b3e0-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b3e0-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4b3e0-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4b3e0-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4b3e0-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4b3e0-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4b3e0-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4b3e0-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4b3e0-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4b3e0-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4b3e0-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4b3e0-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4b3e0-179">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b3e0-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b3e0-180">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4b3e0-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4b3e0-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b3e0-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b3e0-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b3e0-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b3e0-183">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b3e0-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b3e0-184">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b3e0-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4b3e0-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4b3e0-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4b3e0-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4b3e0-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4b3e0-187">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b3e0-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b3e0-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b3e0-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b3e0-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b3e0-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b3e0-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4b3e0-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4b3e0-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b3e0-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b3e0-192">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b3e0-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b3e0-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4b3e0-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4b3e0-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4b3e0-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4b3e0-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4b3e0-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4b3e0-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4b3e0-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4b3e0-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4b3e0-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4b3e0-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4b3e0-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4b3e0-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4b3e0-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="4b3e0-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4b3e0-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="4b3e0-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4b3e0-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)