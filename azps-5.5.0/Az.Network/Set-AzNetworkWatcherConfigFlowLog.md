---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 6d4dca8cdaa9e80fd1417fd65a9200eb5e3ecf7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111548"
---
# <span data-ttu-id="fffca-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fffca-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="fffca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fffca-102">SYNOPSIS</span></span>
<span data-ttu-id="fffca-103">Configura o registro em log de fluxo para um recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="fffca-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="fffca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fffca-104">SYNTAX</span></span>

### <span data-ttu-id="fffca-105">SetFlowlogByResourceWithoutTA (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fffca-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffca-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="fffca-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffca-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="fffca-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fffca-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="fffca-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffca-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="fffca-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fffca-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="fffca-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffca-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="fffca-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fffca-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="fffca-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fffca-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="fffca-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fffca-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fffca-114">DESCRIPTION</span></span>
<span data-ttu-id="fffca-115">A Set-AzNetworkWatcherConfigFlowLog configura o registro em log de fluxo para um recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="fffca-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="fffca-116">As propriedades a ser configuradas incluem: se o log de fluxo está habilitado ou não para o recurso fornecido, a conta de armazenamento configurada para enviar logs, o formato de log de fluxo e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="fffca-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="fffca-117">Atualmente, os Grupos de Segurança de Rede são suportados para o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fffca-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="fffca-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fffca-118">EXAMPLES</span></span>

### <span data-ttu-id="fffca-119">Exemplo 1: Configurar o registro em log de fluxo para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="fffca-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="fffca-120">Neste exemplo, configuramos o status do log de fluxo para um Grupo de Segurança de Rede.</span><span class="sxs-lookup"><span data-stu-id="fffca-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="fffca-121">Na resposta, vemos que o NSG especificado tem log de fluxo habilitado, formato padrão e nenhum conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="fffca-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="fffca-122">Exemplo 2: Configurar o Log de Fluxo para um NSG especificado e definir a versão do registro em log de fluxo como 2.</span><span class="sxs-lookup"><span data-stu-id="fffca-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="fffca-123">Neste exemplo, configuramos o log de fluxo em um NSG (Grupo de Segurança de Rede) com logs da versão 2 especificados.</span><span class="sxs-lookup"><span data-stu-id="fffca-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="fffca-124">Na resposta, vemos que o NSG especificado tem o registro em log de fluxo habilitado, o formato é definido e não há nenhuma política de retenção configurada.</span><span class="sxs-lookup"><span data-stu-id="fffca-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="fffca-125">Se a região não for suportada pela versão especificada, o Network Watcher gravará a versão com suporte padrão na região.</span><span class="sxs-lookup"><span data-stu-id="fffca-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="fffca-126">Exemplo 3: Configurar o Log de Fluxo e a Análise de Tráfego para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="fffca-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="fffca-127">Neste exemplo, configuramos o status de log de fluxo e a Análise de Tráfego para um Grupo de Segurança de Rede.</span><span class="sxs-lookup"><span data-stu-id="fffca-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="fffca-128">Na resposta, vemos que o NSG especificado tem log de fluxo e Análise de Tráfego habilitado, formato padrão e nenhum conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="fffca-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="fffca-129">Exemplo 4: Desabilitar a Análise de Tráfego para um NSG especificado com o Log de Fluxo e a Análise de Tráfego configurados</span><span class="sxs-lookup"><span data-stu-id="fffca-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
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

<span data-ttu-id="fffca-130">Neste exemplo, desabilitaremos a Análise de Tráfego para um Grupo de Segurança de Rede que tem log de fluxo e Análise de Tráfego configurados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fffca-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="fffca-131">Na resposta, vemos que o NSG especificado tem o registro em log de fluxo habilitado, mas a Análise de Tráfego está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="fffca-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="fffca-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fffca-132">PARAMETERS</span></span>

### <span data-ttu-id="fffca-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fffca-133">-AsJob</span></span>
<span data-ttu-id="fffca-134">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fffca-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fffca-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffca-135">-DefaultProfile</span></span>
<span data-ttu-id="fffca-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fffca-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fffca-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="fffca-137">-EnableFlowLog</span></span>
<span data-ttu-id="fffca-138">Sinalizar para habilitar/desabilitar o registro em log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fffca-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="fffca-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="fffca-139">-EnableRetention</span></span>
<span data-ttu-id="fffca-140">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="fffca-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="fffca-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="fffca-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="fffca-142">Sinalizar para habilitar/desabilitar a retenção.</span><span class="sxs-lookup"><span data-stu-id="fffca-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="fffca-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="fffca-143">-FormatType</span></span>
<span data-ttu-id="fffca-144">Tipo de formato de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fffca-144">Type of flow log format.</span></span>

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

### <span data-ttu-id="fffca-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="fffca-145">-FormatVersion</span></span>
<span data-ttu-id="fffca-146">Versão do formato de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fffca-146">Version of flow log format.</span></span>

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

### <span data-ttu-id="fffca-147">-Local</span><span class="sxs-lookup"><span data-stu-id="fffca-147">-Location</span></span>
<span data-ttu-id="fffca-148">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="fffca-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fffca-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fffca-149">-NetworkWatcher</span></span>
<span data-ttu-id="fffca-150">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="fffca-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="fffca-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fffca-151">-NetworkWatcherName</span></span>
<span data-ttu-id="fffca-152">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="fffca-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="fffca-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fffca-153">-ResourceGroupName</span></span>
<span data-ttu-id="fffca-154">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="fffca-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fffca-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fffca-155">-RetentionInDays</span></span>
<span data-ttu-id="fffca-156">Número de dias para reter registros de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fffca-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="fffca-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fffca-157">-StorageAccountId</span></span>
<span data-ttu-id="fffca-158">ID da conta de armazenamento usada para armazenar o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fffca-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="fffca-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="fffca-159">-TargetResourceId</span></span>
<span data-ttu-id="fffca-160">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="fffca-160">The target resource ID.</span></span>

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

### <span data-ttu-id="fffca-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="fffca-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="fffca-162">Obtém ou define o intervalo (em minutos) que decide com que frequência o serviço TA deve fazer a análise de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fffca-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span> <span data-ttu-id="fffca-163">Os valores com suporte são de 10 e 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="fffca-163">Supported values are 10 and 60 minutes.</span></span>

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

### <span data-ttu-id="fffca-164">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="fffca-164">-Workspace</span></span>
<span data-ttu-id="fffca-165">O objeto WS usado para armazenar os dados de análise de tráfego.</span><span class="sxs-lookup"><span data-stu-id="fffca-165">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="fffca-166">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="fffca-166">-WorkspaceGUID</span></span>
<span data-ttu-id="fffca-167">GUID do WS que é usado para armazenar os dados de análise de tráfego.</span><span class="sxs-lookup"><span data-stu-id="fffca-167">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="fffca-168">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="fffca-168">-WorkspaceLocation</span></span>
<span data-ttu-id="fffca-169">Região do Azure do WS, que é usada para armazenar os dados de análise de tráfego.</span><span class="sxs-lookup"><span data-stu-id="fffca-169">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="fffca-170">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="fffca-170">-WorkspaceResourceId</span></span>
<span data-ttu-id="fffca-171">Assinatura do WS que é usado para armazenar os dados de análise de tráfego.</span><span class="sxs-lookup"><span data-stu-id="fffca-171">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="fffca-172">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fffca-172">-Confirm</span></span>
<span data-ttu-id="fffca-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fffca-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fffca-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fffca-174">-WhatIf</span></span>
<span data-ttu-id="fffca-175">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fffca-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fffca-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fffca-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fffca-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffca-177">CommonParameters</span></span>
<span data-ttu-id="fffca-178">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fffca-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffca-179">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fffca-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffca-180">Entradas</span><span class="sxs-lookup"><span data-stu-id="fffca-180">INPUTS</span></span>

### <span data-ttu-id="fffca-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fffca-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="fffca-182">System.String</span><span class="sxs-lookup"><span data-stu-id="fffca-182">System.String</span></span>

### <span data-ttu-id="fffca-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fffca-183">System.Boolean</span></span>

### <span data-ttu-id="fffca-184">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fffca-184">System.Int32</span></span>

### <span data-ttu-id="fffca-185">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fffca-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fffca-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="fffca-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="fffca-187">Saídas</span><span class="sxs-lookup"><span data-stu-id="fffca-187">OUTPUTS</span></span>

### <span data-ttu-id="fffca-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="fffca-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="fffca-189">Notas</span><span class="sxs-lookup"><span data-stu-id="fffca-189">NOTES</span></span>
<span data-ttu-id="fffca-190">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="fffca-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="fffca-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fffca-191">RELATED LINKS</span></span>

[<span data-ttu-id="fffca-192">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fffca-192">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fffca-193">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fffca-193">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="fffca-194">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fffca-194">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fffca-195">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fffca-195">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fffca-196">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fffca-196">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fffca-197">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fffca-197">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fffca-198">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fffca-198">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fffca-199">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fffca-199">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fffca-200">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fffca-200">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fffca-201">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fffca-201">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fffca-202">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fffca-202">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fffca-203">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fffca-203">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fffca-204">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fffca-204">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fffca-205">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fffca-205">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fffca-206">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fffca-206">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="fffca-207">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fffca-207">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fffca-208">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fffca-208">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fffca-209">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fffca-209">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fffca-210">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fffca-210">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fffca-211">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fffca-211">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fffca-212">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fffca-212">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fffca-213">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fffca-213">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fffca-214">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fffca-214">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fffca-215">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fffca-215">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fffca-216">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fffca-216">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fffca-217">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fffca-217">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="fffca-218">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fffca-218">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
