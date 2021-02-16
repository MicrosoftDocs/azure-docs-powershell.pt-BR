---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: a45a6ad4ee85dfabb28bef07400a0b6ebe115d7c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412581"
---
# <span data-ttu-id="250f3-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="250f3-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="250f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="250f3-102">SYNOPSIS</span></span>
<span data-ttu-id="250f3-103">Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="250f3-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="250f3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="250f3-104">SYNTAX</span></span>

### <span data-ttu-id="250f3-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="250f3-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="250f3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="250f3-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="250f3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="250f3-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="250f3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="250f3-108">DESCRIPTION</span></span>
<span data-ttu-id="250f3-109">O cmdlet Get-AzNetworkWatcherFlowLogStatus obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="250f3-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="250f3-110">O status inclui se o log de fluxo está habilitado ou não para o recurso fornecido, a conta de armazenamento configurada para enviar logs e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="250f3-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="250f3-111">Atualmente, os Grupos de Segurança de Rede são suportados para o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="250f3-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="250f3-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="250f3-112">EXAMPLES</span></span>

### <span data-ttu-id="250f3-113">Exemplo 1: Obter o Status de Log de Fluxo para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="250f3-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
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

<span data-ttu-id="250f3-114">Neste exemplo, obteremos o status de log de fluxo para um Grupo de Segurança de Rede.</span><span class="sxs-lookup"><span data-stu-id="250f3-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="250f3-115">O NSG especificado tem log de fluxo habilitado, formato padrão e nenhum conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="250f3-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="250f3-116">Exemplo 2: Obter o Status de Fluxo de Trabalho e Análise de Tráfego para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="250f3-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
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

<span data-ttu-id="250f3-117">Neste exemplo, obteremos o status de fluxo em log e análise de tráfego para um Grupo de Segurança de Rede.</span><span class="sxs-lookup"><span data-stu-id="250f3-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="250f3-118">O NSG especificado tem log de fluxo e Análise de Tráfego habilitados, formato padrão e nenhum conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="250f3-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="250f3-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="250f3-119">PARAMETERS</span></span>

### <span data-ttu-id="250f3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="250f3-120">-AsJob</span></span>
<span data-ttu-id="250f3-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="250f3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="250f3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="250f3-122">-DefaultProfile</span></span>
<span data-ttu-id="250f3-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="250f3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="250f3-124">-Local</span><span class="sxs-lookup"><span data-stu-id="250f3-124">-Location</span></span>
<span data-ttu-id="250f3-125">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="250f3-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="250f3-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="250f3-126">-NetworkWatcher</span></span>
<span data-ttu-id="250f3-127">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="250f3-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="250f3-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="250f3-128">-NetworkWatcherName</span></span>
<span data-ttu-id="250f3-129">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="250f3-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="250f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="250f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="250f3-131">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="250f3-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="250f3-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="250f3-132">-TargetResourceId</span></span>
<span data-ttu-id="250f3-133">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="250f3-133">The target resource ID.</span></span>

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

### <span data-ttu-id="250f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="250f3-134">CommonParameters</span></span>
<span data-ttu-id="250f3-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="250f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="250f3-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="250f3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="250f3-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="250f3-137">INPUTS</span></span>

### <span data-ttu-id="250f3-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="250f3-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="250f3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="250f3-139">System.String</span></span>

## <span data-ttu-id="250f3-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="250f3-140">OUTPUTS</span></span>

### <span data-ttu-id="250f3-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="250f3-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="250f3-142">Notas</span><span class="sxs-lookup"><span data-stu-id="250f3-142">NOTES</span></span>
<span data-ttu-id="250f3-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="250f3-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="250f3-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="250f3-144">RELATED LINKS</span></span>

[<span data-ttu-id="250f3-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="250f3-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="250f3-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="250f3-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="250f3-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="250f3-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="250f3-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="250f3-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="250f3-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="250f3-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="250f3-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="250f3-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="250f3-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="250f3-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="250f3-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="250f3-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="250f3-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="250f3-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="250f3-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="250f3-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="250f3-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="250f3-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="250f3-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="250f3-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="250f3-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="250f3-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="250f3-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="250f3-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="250f3-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="250f3-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="250f3-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="250f3-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="250f3-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="250f3-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="250f3-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="250f3-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="250f3-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="250f3-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="250f3-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="250f3-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="250f3-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="250f3-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="250f3-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="250f3-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="250f3-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="250f3-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="250f3-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="250f3-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="250f3-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="250f3-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="250f3-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="250f3-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="250f3-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="250f3-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
