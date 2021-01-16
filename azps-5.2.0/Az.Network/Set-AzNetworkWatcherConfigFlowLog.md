---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 6d4dca8cdaa9e80fd1417fd65a9200eb5e3ecf7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260076"
---
# <span data-ttu-id="883e2-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="883e2-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="883e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="883e2-102">SYNOPSIS</span></span>
<span data-ttu-id="883e2-103">Configura o registro em log de fluxo para um recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="883e2-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="883e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="883e2-104">SYNTAX</span></span>

### <span data-ttu-id="883e2-105">SetFlowlogByResourceWithoutTA (padrão)</span><span class="sxs-lookup"><span data-stu-id="883e2-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883e2-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="883e2-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883e2-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="883e2-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="883e2-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="883e2-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883e2-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="883e2-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="883e2-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="883e2-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883e2-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="883e2-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="883e2-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="883e2-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883e2-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="883e2-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="883e2-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="883e2-114">DESCRIPTION</span></span>
<span data-ttu-id="883e2-115">O Set-AzNetworkWatcherConfigFlowLog configura o registro em log de fluxo para um recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="883e2-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="883e2-116">As propriedades a serem configuradas incluem: se o recurso de log de fluxo está ou não habilitado para o recurso fornecido, a conta de armazenamento configurada para enviar logs, o formato de log de fluxo e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="883e2-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="883e2-117">Atualmente, os grupos de segurança de rede têm suporte para o registro de fluxo.</span><span class="sxs-lookup"><span data-stu-id="883e2-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="883e2-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="883e2-118">EXAMPLES</span></span>

### <span data-ttu-id="883e2-119">Exemplo 1: configurar o log de fluxo para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="883e2-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="883e2-120">Neste exemplo, configuramos o status do log de fluxo para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="883e2-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="883e2-121">Na resposta, vemos que o NSG especificado tem o log de fluxo habilitado, um formato padrão e nenhuma política de retenção definida.</span><span class="sxs-lookup"><span data-stu-id="883e2-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="883e2-122">Exemplo 2: configurar o log de fluxo de um NSG especificado e definir a versão do log de fluxo para 2.</span><span class="sxs-lookup"><span data-stu-id="883e2-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="883e2-123">Neste exemplo, configuramos o log de fluxo em um grupo de segurança de rede (NSG) com logs da versão 2 especificados.</span><span class="sxs-lookup"><span data-stu-id="883e2-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="883e2-124">Na resposta, vemos que o NSG especificado tem o registro em log habilitado, o formato é definido e não há nenhuma política de retenção configurada.</span><span class="sxs-lookup"><span data-stu-id="883e2-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="883e2-125">Se a região não for compatível com a versão especificada, o Inspetor de rede irá gravar a versão com suporte padrão na região.</span><span class="sxs-lookup"><span data-stu-id="883e2-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="883e2-126">Exemplo 3: configurar o log de fluxo e a análise de tráfego para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="883e2-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="883e2-127">Neste exemplo, configuramos o status do log de fluxo e a análise de tráfego para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="883e2-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="883e2-128">Na resposta, vemos que o NSG especificado tem o log de fluxo e a análise de tráfego habilitada, formato padrão e sem conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="883e2-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="883e2-129">Exemplo 4: desabilitar a análise de tráfego para um NSG especificado com o log de fluxo e a análise de tráfego configurados</span><span class="sxs-lookup"><span data-stu-id="883e2-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="883e2-130">Neste exemplo, desabilitemos a análise de tráfego para um grupo de segurança de rede que tenha o log de fluxo e a análise de tráfego configurados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="883e2-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="883e2-131">Na resposta, vemos que o NSG especificado tem o log de fluxo habilitado, mas a análise de tráfego está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="883e2-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="883e2-132">OS</span><span class="sxs-lookup"><span data-stu-id="883e2-132">PARAMETERS</span></span>

### <span data-ttu-id="883e2-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="883e2-133">-AsJob</span></span>
<span data-ttu-id="883e2-134">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="883e2-134">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883e2-135">-DefaultProfile</span></span>
<span data-ttu-id="883e2-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="883e2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="883e2-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="883e2-137">-EnableFlowLog</span></span>
<span data-ttu-id="883e2-138">Sinalizador para habilitar/desabilitar o registro em log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="883e2-138">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="883e2-139">-EnableRetention</span></span>
<span data-ttu-id="883e2-140">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="883e2-140">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="883e2-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="883e2-142">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="883e2-142">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="883e2-143">-FormatType</span></span>
<span data-ttu-id="883e2-144">Tipo de formato de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="883e2-144">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="883e2-145">-FormatVersion</span></span>
<span data-ttu-id="883e2-146">Versão do formato de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="883e2-146">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-147">-Local</span><span class="sxs-lookup"><span data-stu-id="883e2-147">-Location</span></span>
<span data-ttu-id="883e2-148">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="883e2-148">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="883e2-149">-NetworkWatcher</span></span>
<span data-ttu-id="883e2-150">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="883e2-150">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="883e2-151">-NetworkWatcherName</span></span>
<span data-ttu-id="883e2-152">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="883e2-152">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883e2-153">-ResourceGroupName</span></span>
<span data-ttu-id="883e2-154">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="883e2-154">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="883e2-155">-RetentionInDays</span></span>
<span data-ttu-id="883e2-156">Número de dias para reter registros de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="883e2-156">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="883e2-157">-StorageAccountId</span></span>
<span data-ttu-id="883e2-158">ID da conta de armazenamento que é usada para armazenar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="883e2-158">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="883e2-159">-TargetResourceId</span></span>
<span data-ttu-id="883e2-160">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="883e2-160">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="883e2-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="883e2-162">Obtém ou define o intervalo (em minutos) que decidiria com que frequência o serviço TA deve fazer análises de fluxo.</span><span class="sxs-lookup"><span data-stu-id="883e2-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span> <span data-ttu-id="883e2-163">Os valores com suporte são 10 e 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="883e2-163">Supported values are 10 and 60 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-164">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="883e2-164">-Workspace</span></span>
<span data-ttu-id="883e2-165">O objeto WS que é usado para armazenar os dados de análise de tráfego.</span><span class="sxs-lookup"><span data-stu-id="883e2-165">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-166">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="883e2-166">-WorkspaceGUID</span></span>
<span data-ttu-id="883e2-167">O GUID do WS que é usado para armazenar os dados de análise do tráfego.</span><span class="sxs-lookup"><span data-stu-id="883e2-167">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-168">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="883e2-168">-WorkspaceLocation</span></span>
<span data-ttu-id="883e2-169">A região do Azure do WS que é usada para armazenar os dados de análise do tráfego.</span><span class="sxs-lookup"><span data-stu-id="883e2-169">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-170">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="883e2-170">-WorkspaceResourceId</span></span>
<span data-ttu-id="883e2-171">Assinatura do WS que é usada para armazenar os dados de análise de tráfego.</span><span class="sxs-lookup"><span data-stu-id="883e2-171">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="883e2-172">-Confirme</span><span class="sxs-lookup"><span data-stu-id="883e2-172">-Confirm</span></span>
<span data-ttu-id="883e2-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="883e2-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="883e2-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883e2-174">-WhatIf</span></span>
<span data-ttu-id="883e2-175">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="883e2-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="883e2-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="883e2-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="883e2-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883e2-177">CommonParameters</span></span>
<span data-ttu-id="883e2-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="883e2-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883e2-179">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="883e2-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883e2-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="883e2-180">INPUTS</span></span>

### <span data-ttu-id="883e2-181">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="883e2-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="883e2-182">System. String</span><span class="sxs-lookup"><span data-stu-id="883e2-182">System.String</span></span>

### <span data-ttu-id="883e2-183">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="883e2-183">System.Boolean</span></span>

### <span data-ttu-id="883e2-184">System. Int32</span><span class="sxs-lookup"><span data-stu-id="883e2-184">System.Int32</span></span>

### <span data-ttu-id="883e2-185">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="883e2-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="883e2-186">Microsoft. Azure. Management. Internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="883e2-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="883e2-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="883e2-187">OUTPUTS</span></span>

### <span data-ttu-id="883e2-188">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="883e2-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="883e2-189">INFORMA</span><span class="sxs-lookup"><span data-stu-id="883e2-189">NOTES</span></span>
<span data-ttu-id="883e2-190">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, fluxo, logs, flowlog, registro em log</span><span class="sxs-lookup"><span data-stu-id="883e2-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="883e2-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="883e2-191">RELATED LINKS</span></span>

[<span data-ttu-id="883e2-192">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="883e2-192">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="883e2-193">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="883e2-193">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="883e2-194">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="883e2-194">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="883e2-195">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="883e2-195">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="883e2-196">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="883e2-196">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="883e2-197">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="883e2-197">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="883e2-198">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="883e2-198">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="883e2-199">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="883e2-199">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="883e2-200">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="883e2-200">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="883e2-201">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="883e2-201">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="883e2-202">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="883e2-202">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="883e2-203">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="883e2-203">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="883e2-204">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="883e2-204">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="883e2-205">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="883e2-205">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="883e2-206">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="883e2-206">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="883e2-207">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="883e2-207">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="883e2-208">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="883e2-208">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="883e2-209">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="883e2-209">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="883e2-210">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="883e2-210">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="883e2-211">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="883e2-211">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="883e2-212">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="883e2-212">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="883e2-213">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="883e2-213">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="883e2-214">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="883e2-214">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="883e2-215">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="883e2-215">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="883e2-216">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="883e2-216">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="883e2-217">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="883e2-217">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="883e2-218">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="883e2-218">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
