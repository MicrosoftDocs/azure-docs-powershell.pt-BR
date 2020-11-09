---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: dd88c40876bf3ceb5f90a7088f5943fcf5f18ce8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283911"
---
# <span data-ttu-id="3a542-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3a542-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="3a542-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a542-102">SYNOPSIS</span></span>
<span data-ttu-id="3a542-103">Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="3a542-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="3a542-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a542-104">SYNTAX</span></span>

### <span data-ttu-id="3a542-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="3a542-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a542-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3a542-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a542-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3a542-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a542-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a542-108">DESCRIPTION</span></span>
<span data-ttu-id="3a542-109">O cmdlet Get-AzNetworkWatcherFlowLogStatus Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="3a542-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="3a542-110">O status inclui se o registro em log de fluxo está habilitado ou não para o recurso fornecido, a conta de armazenamento configurada para enviar logs e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="3a542-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="3a542-111">Atualmente, os grupos de segurança de rede têm suporte para o registro de fluxo.</span><span class="sxs-lookup"><span data-stu-id="3a542-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="3a542-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a542-112">EXAMPLES</span></span>

### <span data-ttu-id="3a542-113">Exemplo 1: obter o status de log de fluxo de um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="3a542-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="3a542-114">Neste exemplo, obtemos o status de log de fluxo para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3a542-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="3a542-115">O NSG especificado tem o log de fluxo habilitado, um formato padrão e nenhum conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="3a542-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="3a542-116">Exemplo 2: obter o log de fluxo e o status da análise de tráfego para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="3a542-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="3a542-117">Neste exemplo, obtemos o status de registro de fluxo e de análise de tráfego para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3a542-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="3a542-118">O NSG especificado tem o log de fluxo e a análise de tráfego habilitada, formato padrão e sem conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="3a542-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="3a542-119">OS</span><span class="sxs-lookup"><span data-stu-id="3a542-119">PARAMETERS</span></span>

### <span data-ttu-id="3a542-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a542-120">-AsJob</span></span>
<span data-ttu-id="3a542-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3a542-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a542-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a542-122">-DefaultProfile</span></span>
<span data-ttu-id="3a542-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a542-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a542-124">-Local</span><span class="sxs-lookup"><span data-stu-id="3a542-124">-Location</span></span>
<span data-ttu-id="3a542-125">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3a542-125">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a542-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a542-126">-NetworkWatcher</span></span>
<span data-ttu-id="3a542-127">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3a542-127">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a542-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3a542-128">-NetworkWatcherName</span></span>
<span data-ttu-id="3a542-129">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3a542-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a542-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a542-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a542-131">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="3a542-131">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a542-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3a542-132">-TargetResourceId</span></span>
<span data-ttu-id="3a542-133">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="3a542-133">The target resource ID.</span></span>

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

### <span data-ttu-id="3a542-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a542-134">CommonParameters</span></span>
<span data-ttu-id="3a542-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a542-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a542-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a542-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a542-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a542-137">INPUTS</span></span>

### <span data-ttu-id="3a542-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a542-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3a542-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3a542-139">System.String</span></span>

## <span data-ttu-id="3a542-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a542-140">OUTPUTS</span></span>

### <span data-ttu-id="3a542-141">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="3a542-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="3a542-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a542-142">NOTES</span></span>
<span data-ttu-id="3a542-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, fluxo, logs, flowlog, registro em log</span><span class="sxs-lookup"><span data-stu-id="3a542-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="3a542-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a542-144">RELATED LINKS</span></span>

[<span data-ttu-id="3a542-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a542-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3a542-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a542-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3a542-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3a542-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3a542-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3a542-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3a542-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3a542-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3a542-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3a542-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3a542-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3a542-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3a542-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3a542-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3a542-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3a542-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3a542-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3a542-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3a542-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3a542-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3a542-156">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3a542-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3a542-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a542-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3a542-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3a542-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3a542-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3a542-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3a542-160">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3a542-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3a542-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3a542-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3a542-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3a542-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3a542-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3a542-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3a542-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3a542-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3a542-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3a542-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3a542-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3a542-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3a542-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3a542-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3a542-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3a542-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3a542-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3a542-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3a542-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3a542-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3a542-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3a542-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
