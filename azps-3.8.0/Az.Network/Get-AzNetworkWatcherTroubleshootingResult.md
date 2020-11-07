---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 710f35a96872ccf840810d8c2fe5189cccdbcaed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940371"
---
# <span data-ttu-id="2c7f0-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2c7f0-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="2c7f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7f0-103">Obtém o resultado da solução de problemas da operação de solução de problemas executada anteriormente ou em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="2c7f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c7f0-104">SYNTAX</span></span>

### <span data-ttu-id="2c7f0-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c7f0-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c7f0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2c7f0-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c7f0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2c7f0-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c7f0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c7f0-108">DESCRIPTION</span></span>
<span data-ttu-id="2c7f0-109">O cmdlet Get-AzNetworkWatcherTroubleshootingResult Obtém o resultado da solução de problemas da operação Start-AzNetworkWatcherResourceTroubleshooting executada anteriormente ou atualmente em execução.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="2c7f0-110">Se a operação de solução de problemas estiver em andamento, esta operação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="2c7f0-111">Atualmente, há suporte para gateways de rede virtual e conexões.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="2c7f0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c7f0-112">EXAMPLES</span></span>

### <span data-ttu-id="2c7f0-113">Exemplo 1: iniciar a solução de problemas em um gateway de rede virtual e recuperar resultado</span><span class="sxs-lookup"><span data-stu-id="2c7f0-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="2c7f0-114">O exemplo acima começa a solução de problemas em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="2c7f0-115">A operação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="2c7f0-116">Após a solução de problemas ter começado, uma chamada de Get-AzNetworkWatcherTroubleshootingResult é feita ao recurso para recuperar o resultado da chamada.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="2c7f0-117">OS</span><span class="sxs-lookup"><span data-stu-id="2c7f0-117">PARAMETERS</span></span>

### <span data-ttu-id="2c7f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c7f0-118">-DefaultProfile</span></span>
<span data-ttu-id="2c7f0-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c7f0-120">-Local</span><span class="sxs-lookup"><span data-stu-id="2c7f0-120">-Location</span></span>
<span data-ttu-id="2c7f0-121">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2c7f0-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c7f0-122">-NetworkWatcher</span></span>
<span data-ttu-id="2c7f0-123">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="2c7f0-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2c7f0-124">-NetworkWatcherName</span></span>
<span data-ttu-id="2c7f0-125">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="2c7f0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c7f0-126">-ResourceGroupName</span></span>
<span data-ttu-id="2c7f0-127">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2c7f0-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2c7f0-128">-TargetResourceId</span></span>
<span data-ttu-id="2c7f0-129">A ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-129">The target resource ID.</span></span>

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

### <span data-ttu-id="2c7f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7f0-130">CommonParameters</span></span>
<span data-ttu-id="2c7f0-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7f0-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c7f0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7f0-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c7f0-133">INPUTS</span></span>

### <span data-ttu-id="2c7f0-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c7f0-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2c7f0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2c7f0-135">System.String</span></span>

## <span data-ttu-id="2c7f0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c7f0-136">OUTPUTS</span></span>

### <span data-ttu-id="2c7f0-137">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2c7f0-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="2c7f0-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c7f0-138">NOTES</span></span>
<span data-ttu-id="2c7f0-139">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, solução de problemas, VPN, conexão</span><span class="sxs-lookup"><span data-stu-id="2c7f0-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="2c7f0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c7f0-140">RELATED LINKS</span></span>

[<span data-ttu-id="2c7f0-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c7f0-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2c7f0-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c7f0-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2c7f0-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c7f0-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2c7f0-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2c7f0-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2c7f0-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2c7f0-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2c7f0-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2c7f0-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2c7f0-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2c7f0-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2c7f0-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c7f0-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c7f0-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2c7f0-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2c7f0-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c7f0-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c7f0-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c7f0-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c7f0-152">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c7f0-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c7f0-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7f0-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2c7f0-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2c7f0-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2c7f0-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2c7f0-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2c7f0-156">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c7f0-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c7f0-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c7f0-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c7f0-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c7f0-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c7f0-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2c7f0-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2c7f0-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c7f0-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c7f0-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c7f0-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c7f0-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2c7f0-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2c7f0-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2c7f0-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2c7f0-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2c7f0-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2c7f0-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2c7f0-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2c7f0-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2c7f0-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2c7f0-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c7f0-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
