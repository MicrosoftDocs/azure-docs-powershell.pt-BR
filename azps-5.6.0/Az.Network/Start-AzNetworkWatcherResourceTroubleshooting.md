---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 4886277bb994e0fe3a33645916660658a8367f1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885385"
---
# <span data-ttu-id="44156-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="44156-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="44156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44156-102">SYNOPSIS</span></span>
<span data-ttu-id="44156-103">Inicia a solução de problemas em um recurso de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="44156-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="44156-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44156-104">SYNTAX</span></span>

### <span data-ttu-id="44156-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44156-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44156-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="44156-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44156-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="44156-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44156-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44156-108">DESCRIPTION</span></span>
<span data-ttu-id="44156-109">O Start-AzNetworkWatcherResourceTroubleshooting cmdlet começa a solucionar problemas para um recurso de rede no Azure e retorna informações sobre possíveis problemas e mitigações.</span><span class="sxs-lookup"><span data-stu-id="44156-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="44156-110">Atualmente, há suporte para Gateways e Conexões de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="44156-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="44156-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44156-111">EXAMPLES</span></span>

### <span data-ttu-id="44156-112">Exemplo 1: Iniciar Solução de Problemas em um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="44156-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="44156-113">O exemplo acima começa a solucionar problemas em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="44156-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="44156-114">A operação pode levar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="44156-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="44156-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44156-115">PARAMETERS</span></span>

### <span data-ttu-id="44156-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44156-116">-DefaultProfile</span></span>
<span data-ttu-id="44156-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="44156-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44156-118">-Location</span><span class="sxs-lookup"><span data-stu-id="44156-118">-Location</span></span>
<span data-ttu-id="44156-119">Local do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="44156-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="44156-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44156-120">-NetworkWatcher</span></span>
<span data-ttu-id="44156-121">O recurso do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="44156-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="44156-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="44156-122">-NetworkWatcherName</span></span>
<span data-ttu-id="44156-123">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="44156-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="44156-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44156-124">-ResourceGroupName</span></span>
<span data-ttu-id="44156-125">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="44156-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="44156-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="44156-126">-StorageId</span></span>
<span data-ttu-id="44156-127">A ID de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44156-127">The storage ID.</span></span>

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

### <span data-ttu-id="44156-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="44156-128">-StoragePath</span></span>
<span data-ttu-id="44156-129">O caminho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44156-129">The storage path.</span></span>

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

### <span data-ttu-id="44156-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="44156-130">-TargetResourceId</span></span>
<span data-ttu-id="44156-131">Especifica a id de recurso do recurso a ser solucionado.</span><span class="sxs-lookup"><span data-stu-id="44156-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="44156-132">Formato de exemplo: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="44156-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="44156-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44156-133">CommonParameters</span></span>
<span data-ttu-id="44156-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44156-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44156-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44156-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44156-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44156-136">INPUTS</span></span>

### <span data-ttu-id="44156-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44156-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="44156-138">System.String</span><span class="sxs-lookup"><span data-stu-id="44156-138">System.String</span></span>

## <span data-ttu-id="44156-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44156-139">OUTPUTS</span></span>

### <span data-ttu-id="44156-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="44156-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="44156-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="44156-141">NOTES</span></span>
<span data-ttu-id="44156-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="44156-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="44156-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44156-143">RELATED LINKS</span></span>

[<span data-ttu-id="44156-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44156-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="44156-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44156-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="44156-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="44156-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="44156-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="44156-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="44156-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="44156-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="44156-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="44156-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="44156-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="44156-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="44156-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44156-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44156-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="44156-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="44156-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44156-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44156-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44156-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44156-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44156-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="44156-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="44156-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="44156-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="44156-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="44156-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="44156-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="44156-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44156-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44156-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44156-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44156-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44156-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44156-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="44156-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="44156-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44156-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44156-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44156-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="44156-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="44156-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="44156-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="44156-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="44156-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="44156-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="44156-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="44156-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="44156-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="44156-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="44156-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="44156-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
