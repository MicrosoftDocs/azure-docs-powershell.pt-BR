---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 8a2bde41d0e7e09acc1ad10a9901f0cf26334d02
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400494"
---
# <span data-ttu-id="a25b5-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a25b5-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="a25b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a25b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a25b5-103">Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="a25b5-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="a25b5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a25b5-104">SYNTAX</span></span>

### <span data-ttu-id="a25b5-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a25b5-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a25b5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a25b5-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a25b5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a25b5-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a25b5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a25b5-108">DESCRIPTION</span></span>
<span data-ttu-id="a25b5-109">O Get-AzNetworkWatcherFlowLogStatus cmdlet Obtém o status do log de fluxo em um recurso.</span><span class="sxs-lookup"><span data-stu-id="a25b5-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span>
<span data-ttu-id="a25b5-110">O status inclui se o log de fluxo está habilitado ou não para o recurso fornecido, a conta de armazenamento configurada para enviar logs e a política de retenção para os logs.</span><span class="sxs-lookup"><span data-stu-id="a25b5-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span>
<span data-ttu-id="a25b5-111">Atualmente, os Grupos de Segurança de Rede são suportados para o log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a25b5-111">Currently Network Security Groups are supported for flow logging.</span></span>

## <span data-ttu-id="a25b5-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a25b5-112">EXAMPLES</span></span>

### <span data-ttu-id="a25b5-113">Exemplo 1: Obter o Status de Log de Fluxo para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="a25b5-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
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

<span data-ttu-id="a25b5-114">Neste exemplo, obteremos o status de log de fluxo para um Grupo de Segurança de Rede.</span><span class="sxs-lookup"><span data-stu-id="a25b5-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="a25b5-115">O NSG especificado tem log de fluxo habilitado, formato padrão e nenhum conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="a25b5-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="a25b5-116">Exemplo 2: Obter o Status de Fluxo de Trabalho e Análise de Tráfego para um NSG especificado</span><span class="sxs-lookup"><span data-stu-id="a25b5-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
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

<span data-ttu-id="a25b5-117">Neste exemplo, temos o status de log de fluxo e análise de tráfego para um Grupo de Segurança de Rede.</span><span class="sxs-lookup"><span data-stu-id="a25b5-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="a25b5-118">O NSG especificado tem log de fluxo e Análise de Tráfego habilitados, formato padrão e nenhum conjunto de políticas de retenção.</span><span class="sxs-lookup"><span data-stu-id="a25b5-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="a25b5-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a25b5-119">PARAMETERS</span></span>

### <span data-ttu-id="a25b5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a25b5-120">-AsJob</span></span>
<span data-ttu-id="a25b5-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a25b5-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a25b5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25b5-122">-DefaultProfile</span></span>
<span data-ttu-id="a25b5-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a25b5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a25b5-124">-Local</span><span class="sxs-lookup"><span data-stu-id="a25b5-124">-Location</span></span>
<span data-ttu-id="a25b5-125">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="a25b5-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a25b5-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a25b5-126">-NetworkWatcher</span></span>
<span data-ttu-id="a25b5-127">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="a25b5-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="a25b5-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a25b5-128">-NetworkWatcherName</span></span>
<span data-ttu-id="a25b5-129">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="a25b5-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="a25b5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25b5-130">-ResourceGroupName</span></span>
<span data-ttu-id="a25b5-131">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="a25b5-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a25b5-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a25b5-132">-TargetResourceId</span></span>
<span data-ttu-id="a25b5-133">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="a25b5-133">The target resource ID.</span></span>

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

### <span data-ttu-id="a25b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25b5-134">CommonParameters</span></span>
<span data-ttu-id="a25b5-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25b5-136">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a25b5-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25b5-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="a25b5-137">INPUTS</span></span>

### <span data-ttu-id="a25b5-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a25b5-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a25b5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a25b5-139">System.String</span></span>

## <span data-ttu-id="a25b5-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="a25b5-140">OUTPUTS</span></span>

### <span data-ttu-id="a25b5-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="a25b5-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="a25b5-142">Notas</span><span class="sxs-lookup"><span data-stu-id="a25b5-142">NOTES</span></span>
<span data-ttu-id="a25b5-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="a25b5-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="a25b5-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a25b5-144">RELATED LINKS</span></span>

[<span data-ttu-id="a25b5-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a25b5-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a25b5-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a25b5-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a25b5-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a25b5-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a25b5-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a25b5-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a25b5-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a25b5-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a25b5-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a25b5-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a25b5-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a25b5-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a25b5-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a25b5-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a25b5-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a25b5-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a25b5-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a25b5-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a25b5-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a25b5-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a25b5-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a25b5-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a25b5-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a25b5-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a25b5-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a25b5-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a25b5-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a25b5-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a25b5-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a25b5-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a25b5-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a25b5-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a25b5-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a25b5-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a25b5-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a25b5-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a25b5-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a25b5-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a25b5-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a25b5-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a25b5-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a25b5-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a25b5-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a25b5-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a25b5-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a25b5-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a25b5-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a25b5-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a25b5-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a25b5-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a25b5-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a25b5-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
