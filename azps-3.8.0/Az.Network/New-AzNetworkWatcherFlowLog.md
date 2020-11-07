---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 33441112856ebdbcb12da237542ed3ce62a3944c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941779"
---
# <span data-ttu-id="ab86a-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ab86a-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="ab86a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab86a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab86a-103">Crie ou atualize um recurso de log de fluxo para o grupo de segurança de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="ab86a-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="ab86a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab86a-104">SYNTAX</span></span>

### <span data-ttu-id="ab86a-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab86a-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab86a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ab86a-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab86a-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="ab86a-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab86a-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="ab86a-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab86a-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ab86a-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab86a-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="ab86a-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab86a-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab86a-111">DESCRIPTION</span></span>
<span data-ttu-id="ab86a-112">New-AzNetworkWatcherFlowLog comando cria ou atualiza um recurso de log de fluxo para o grupo de segurança de rede especificado.</span><span class="sxs-lookup"><span data-stu-id="ab86a-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="ab86a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab86a-113">EXAMPLES</span></span>

### <span data-ttu-id="ab86a-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab86a-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="ab86a-115">Nome: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: localização bem-sucedida: lesteus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG Storageid:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/myarmazenamento habilitado: verdadeiro RetentionPolicy: {"dias": 5, "habilitado": verdadeiro} formato: {"Type": "JSON", "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": true, "workspaceid": "bbbbbbbb-BBBB-BBBB-BBBB-bbbbbbbbbbbb", "workspaceRegion": "lesteus", "workspaceResourceId": "/subscriptions/bbbbbbbb-BBBB-BBBB-BBBB-bbbbbbbbbbbb/resourcegr Oups/FlowLogsV2Demo/provedores/Microsoft. OperationalInsights/espaços de trabalho/MyWorkspace", "trafficAnalyticsInterval": 60}}</span><span class="sxs-lookup"><span data-stu-id="ab86a-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="ab86a-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ab86a-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="ab86a-117">Se você quiser desabilitar o recurso flowLog para o qual TrafficAnalytics está configurado, também é necessário desabilitar o TrafficAnalytics.</span><span class="sxs-lookup"><span data-stu-id="ab86a-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="ab86a-118">Isso pode ser feito como no exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="ab86a-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="ab86a-119">Nome: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: localização bem-sucedida: lesteus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Networkid de rede/networkSecurityGroups/MyNSG:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/mystorage Enabled: false RetentionPolicy: {"Days": 0, "Enabled": false} Format: {"Type": "JSON", "versão": 1} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": false, "trafficAnalyticsInterval": 60}}</span><span class="sxs-lookup"><span data-stu-id="ab86a-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="ab86a-120">OS</span><span class="sxs-lookup"><span data-stu-id="ab86a-120">PARAMETERS</span></span>

### <span data-ttu-id="ab86a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab86a-121">-DefaultProfile</span></span>
<span data-ttu-id="ab86a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab86a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab86a-123">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="ab86a-123">-Enabled</span></span>
<span data-ttu-id="ab86a-124">Sinalizador para habilitar/desabilitar o registro em log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ab86a-124">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="ab86a-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="ab86a-125">-EnableRetention</span></span>
<span data-ttu-id="ab86a-126">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="ab86a-126">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="ab86a-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="ab86a-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="ab86a-128">Sinalizar para habilitar/desabilitar TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="ab86a-128">Flag to enable/disable TrafficAnalytics</span></span>

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

### <span data-ttu-id="ab86a-129">-Force</span><span class="sxs-lookup"><span data-stu-id="ab86a-129">-Force</span></span>
<span data-ttu-id="ab86a-130">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="ab86a-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ab86a-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="ab86a-131">-FormatType</span></span>
<span data-ttu-id="ab86a-132">O tipo de arquivo do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ab86a-132">The file type of flow log.</span></span>
<span data-ttu-id="ab86a-133">Agora, o único valor com suporte é ' JSON '.</span><span class="sxs-lookup"><span data-stu-id="ab86a-133">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="ab86a-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="ab86a-134">-FormatVersion</span></span>
<span data-ttu-id="ab86a-135">A versão (revisão) do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ab86a-135">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="ab86a-136">-Local</span><span class="sxs-lookup"><span data-stu-id="ab86a-136">-Location</span></span>
<span data-ttu-id="ab86a-137">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ab86a-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ab86a-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab86a-138">-Name</span></span>
<span data-ttu-id="ab86a-139">O nome do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ab86a-139">The flow log name.</span></span>

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

### <span data-ttu-id="ab86a-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab86a-140">-NetworkWatcher</span></span>
<span data-ttu-id="ab86a-141">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ab86a-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="ab86a-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ab86a-142">-NetworkWatcherName</span></span>
<span data-ttu-id="ab86a-143">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ab86a-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="ab86a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab86a-144">-ResourceGroupName</span></span>
<span data-ttu-id="ab86a-145">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ab86a-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ab86a-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="ab86a-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="ab86a-147">Número de dias para reter registros de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ab86a-147">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="ab86a-148">-Storageid</span><span class="sxs-lookup"><span data-stu-id="ab86a-148">-StorageId</span></span>
<span data-ttu-id="ab86a-149">ID da conta de armazenamento que é usada para armazenar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ab86a-149">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="ab86a-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="ab86a-150">-Tag</span></span>
<span data-ttu-id="ab86a-151">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="ab86a-151">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ab86a-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ab86a-152">-TargetResourceId</span></span>
<span data-ttu-id="ab86a-153">ID do grupo de segurança de rede para o qual o log de fluxo será aplicado.</span><span class="sxs-lookup"><span data-stu-id="ab86a-153">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="ab86a-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="ab86a-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="ab86a-155">O intervalo em minutos que decidiria com que frequência o serviço TA deve fazer análises de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ab86a-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="ab86a-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ab86a-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="ab86a-157">ID do recurso do espaço de trabalho anexado.</span><span class="sxs-lookup"><span data-stu-id="ab86a-157">Resource Id of the attached workspace.</span></span>

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

### <span data-ttu-id="ab86a-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab86a-158">-Confirm</span></span>
<span data-ttu-id="ab86a-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab86a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab86a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab86a-160">-WhatIf</span></span>
<span data-ttu-id="ab86a-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab86a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab86a-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab86a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab86a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab86a-163">CommonParameters</span></span>
<span data-ttu-id="ab86a-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab86a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab86a-165">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab86a-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab86a-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab86a-166">INPUTS</span></span>

### <span data-ttu-id="ab86a-167">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab86a-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="ab86a-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab86a-168">OUTPUTS</span></span>

### <span data-ttu-id="ab86a-169">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="ab86a-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="ab86a-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab86a-170">NOTES</span></span>

## <span data-ttu-id="ab86a-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab86a-171">RELATED LINKS</span></span>

[<span data-ttu-id="ab86a-172">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab86a-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ab86a-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab86a-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ab86a-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ab86a-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ab86a-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ab86a-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ab86a-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ab86a-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ab86a-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ab86a-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ab86a-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ab86a-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ab86a-179">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab86a-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab86a-180">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ab86a-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ab86a-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab86a-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab86a-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab86a-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab86a-183">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab86a-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ab86a-184">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab86a-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ab86a-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ab86a-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ab86a-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ab86a-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ab86a-187">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab86a-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ab86a-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab86a-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ab86a-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab86a-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ab86a-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ab86a-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ab86a-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab86a-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ab86a-192">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab86a-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ab86a-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ab86a-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ab86a-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ab86a-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ab86a-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ab86a-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ab86a-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ab86a-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ab86a-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ab86a-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ab86a-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab86a-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="ab86a-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ab86a-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="ab86a-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ab86a-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="ab86a-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ab86a-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog)