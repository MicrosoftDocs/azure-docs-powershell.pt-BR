---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 8296a680db76e1e7b3aedb15896f41ad0fba8e2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777691"
---
# <span data-ttu-id="4a78a-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4a78a-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="4a78a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a78a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a78a-103">Obtém um recurso de log de fluxo ou uma lista de recursos de log de fluxo na assinatura especificada e na região.</span><span class="sxs-lookup"><span data-stu-id="4a78a-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="4a78a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a78a-104">SYNTAX</span></span>

### <span data-ttu-id="4a78a-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a78a-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a78a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4a78a-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a78a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4a78a-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a78a-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a78a-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a78a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a78a-109">DESCRIPTION</span></span>
<span data-ttu-id="4a78a-110">Obtém um recurso de log de fluxo ou uma lista de recursos de log de fluxo na assinatura especificada e na região.</span><span class="sxs-lookup"><span data-stu-id="4a78a-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="4a78a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a78a-111">EXAMPLES</span></span>

### <span data-ttu-id="4a78a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a78a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="4a78a-113">Nome: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: localização bem-sucedida: lesteus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG Storageid:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/myarmazenamento habilitado: verdadeiro RetentionPolicy: {"dias": 5, "habilitado": verdadeiro} formato: {"Type": "JSON", "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": true, "workspaceid": "bbbbbbbb-BBBB-BBBB-BBBB-bbbbbbbbbbbb", "workspaceRegion": "lesteus", "workspaceResourceId": "/subscriptions/bbbbbbbb-BBBB-BBBB-BBBB-bbbbbbbbbbbb/resourcegr Oups/FlowLogsV2Demo/provedores/Microsoft. OperationalInsights/espaços de trabalho/MyWorkspace", "trafficAnalyticsInterval": 60}</span><span class="sxs-lookup"><span data-stu-id="4a78a-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="4a78a-114">OS</span><span class="sxs-lookup"><span data-stu-id="4a78a-114">PARAMETERS</span></span>

### <span data-ttu-id="4a78a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a78a-115">-DefaultProfile</span></span>
<span data-ttu-id="4a78a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a78a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a78a-117">-Local</span><span class="sxs-lookup"><span data-stu-id="4a78a-117">-Location</span></span>
<span data-ttu-id="4a78a-118">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="4a78a-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a78a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a78a-119">-Name</span></span>
<span data-ttu-id="4a78a-120">O nome do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4a78a-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a78a-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a78a-121">-NetworkWatcher</span></span>
<span data-ttu-id="4a78a-122">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="4a78a-122">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a78a-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4a78a-123">-NetworkWatcherName</span></span>
<span data-ttu-id="4a78a-124">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="4a78a-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a78a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a78a-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a78a-126">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="4a78a-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a78a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a78a-127">-ResourceId</span></span>
<span data-ttu-id="4a78a-128">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="4a78a-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a78a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a78a-129">CommonParameters</span></span>
<span data-ttu-id="4a78a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a78a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a78a-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a78a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a78a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a78a-132">INPUTS</span></span>

### <span data-ttu-id="4a78a-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a78a-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4a78a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4a78a-134">System.String</span></span>

## <span data-ttu-id="4a78a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a78a-135">OUTPUTS</span></span>

### <span data-ttu-id="4a78a-136">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="4a78a-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="4a78a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a78a-137">NOTES</span></span>

## <span data-ttu-id="4a78a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a78a-138">RELATED LINKS</span></span>

[<span data-ttu-id="4a78a-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a78a-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4a78a-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a78a-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4a78a-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a78a-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4a78a-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4a78a-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4a78a-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4a78a-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4a78a-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4a78a-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4a78a-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4a78a-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4a78a-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a78a-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a78a-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4a78a-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4a78a-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a78a-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a78a-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a78a-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a78a-150">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a78a-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a78a-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a78a-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4a78a-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4a78a-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4a78a-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4a78a-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4a78a-154">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a78a-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a78a-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a78a-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a78a-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a78a-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a78a-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4a78a-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4a78a-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a78a-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a78a-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a78a-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a78a-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4a78a-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4a78a-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4a78a-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4a78a-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4a78a-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4a78a-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4a78a-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4a78a-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4a78a-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4a78a-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a78a-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="4a78a-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4a78a-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog)

[<span data-ttu-id="4a78a-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4a78a-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="4a78a-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4a78a-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog)
