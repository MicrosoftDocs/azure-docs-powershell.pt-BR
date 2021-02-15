---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: db3e3e529fd5c056acf793cd14280ef688c58a81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115164"
---
# <span data-ttu-id="63538-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="63538-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="63538-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63538-102">SYNOPSIS</span></span>
<span data-ttu-id="63538-103">Obtém o resultado da solução de problemas da operação de solução de problemas anterior ou em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="63538-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="63538-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63538-104">SYNTAX</span></span>

### <span data-ttu-id="63538-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63538-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63538-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="63538-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63538-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="63538-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63538-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="63538-108">DESCRIPTION</span></span>
<span data-ttu-id="63538-109">O cmdlet Get-AzNetworkWatcherTroubleshootingResult obtém o resultado da solução de problemas da execução anterior ou da operação de Start-AzNetworkWatcherResourceTroubleshooting atual.</span><span class="sxs-lookup"><span data-stu-id="63538-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="63538-110">Se a operação de solução de problemas estiver em andamento, essa operação pode levar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="63538-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="63538-111">Atualmente, há suporte para Gateways e Conexões de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="63538-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="63538-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63538-112">EXAMPLES</span></span>

### <span data-ttu-id="63538-113">Exemplo 1: Iniciar a solução de problemas em um Gateway de Rede Virtual e recuperar resultado</span><span class="sxs-lookup"><span data-stu-id="63538-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="63538-114">O exemplo acima começa a solucionar problemas em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="63538-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="63538-115">A operação pode levar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="63538-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="63538-116">Depois que a solução de problemas for iniciada, uma Get-AzNetworkWatcherTroubleshootingResult chamada será feita ao recurso para recuperar o resultado dessa chamada.</span><span class="sxs-lookup"><span data-stu-id="63538-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="63538-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63538-117">PARAMETERS</span></span>

### <span data-ttu-id="63538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63538-118">-DefaultProfile</span></span>
<span data-ttu-id="63538-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="63538-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63538-120">-Local</span><span class="sxs-lookup"><span data-stu-id="63538-120">-Location</span></span>
<span data-ttu-id="63538-121">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="63538-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="63538-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63538-122">-NetworkWatcher</span></span>
<span data-ttu-id="63538-123">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="63538-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="63538-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="63538-124">-NetworkWatcherName</span></span>
<span data-ttu-id="63538-125">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="63538-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="63538-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63538-126">-ResourceGroupName</span></span>
<span data-ttu-id="63538-127">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="63538-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="63538-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="63538-128">-TargetResourceId</span></span>
<span data-ttu-id="63538-129">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="63538-129">The target resource ID.</span></span>

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

### <span data-ttu-id="63538-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63538-130">CommonParameters</span></span>
<span data-ttu-id="63538-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63538-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63538-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63538-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63538-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="63538-133">INPUTS</span></span>

### <span data-ttu-id="63538-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63538-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="63538-135">System.String</span><span class="sxs-lookup"><span data-stu-id="63538-135">System.String</span></span>

## <span data-ttu-id="63538-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="63538-136">OUTPUTS</span></span>

### <span data-ttu-id="63538-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="63538-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="63538-138">Notas</span><span class="sxs-lookup"><span data-stu-id="63538-138">NOTES</span></span>
<span data-ttu-id="63538-139">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="63538-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="63538-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63538-140">RELATED LINKS</span></span>

[<span data-ttu-id="63538-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63538-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="63538-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63538-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="63538-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63538-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="63538-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="63538-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="63538-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="63538-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="63538-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="63538-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="63538-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="63538-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="63538-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63538-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63538-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="63538-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="63538-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63538-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63538-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63538-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63538-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63538-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63538-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="63538-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="63538-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="63538-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="63538-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="63538-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="63538-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63538-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63538-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63538-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63538-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63538-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63538-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="63538-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="63538-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63538-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63538-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63538-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63538-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="63538-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="63538-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="63538-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="63538-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="63538-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="63538-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="63538-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="63538-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="63538-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="63538-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63538-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
