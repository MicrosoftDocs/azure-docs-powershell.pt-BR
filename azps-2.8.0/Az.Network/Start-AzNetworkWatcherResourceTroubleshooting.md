---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5c11eecb00aa97fc90aecc770a77285f77be988b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408467"
---
# <span data-ttu-id="ff456-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ff456-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="ff456-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff456-102">SYNOPSIS</span></span>
<span data-ttu-id="ff456-103">Começa a solucionar problemas em um recurso de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="ff456-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="ff456-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff456-104">SYNTAX</span></span>

### <span data-ttu-id="ff456-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ff456-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff456-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ff456-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff456-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ff456-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff456-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff456-108">DESCRIPTION</span></span>
<span data-ttu-id="ff456-109">O Start-AzNetworkWatcherResourceTroubleshooting cmdlet começa a solucionar problemas para um recurso de rede no Azure e retorna informações sobre possíveis problemas e atenuações.</span><span class="sxs-lookup"><span data-stu-id="ff456-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="ff456-110">Atualmente, há suporte para Gateways e Conexões de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="ff456-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="ff456-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff456-111">EXAMPLES</span></span>

### <span data-ttu-id="ff456-112">Exemplo 1: Iniciar a solução de problemas em um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="ff456-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="ff456-113">O exemplo acima começa a solucionar problemas em um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ff456-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="ff456-114">A operação pode levar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="ff456-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="ff456-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff456-115">PARAMETERS</span></span>

### <span data-ttu-id="ff456-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff456-116">-DefaultProfile</span></span>
<span data-ttu-id="ff456-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ff456-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff456-118">-Local</span><span class="sxs-lookup"><span data-stu-id="ff456-118">-Location</span></span>
<span data-ttu-id="ff456-119">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="ff456-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ff456-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff456-120">-NetworkWatcher</span></span>
<span data-ttu-id="ff456-121">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="ff456-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="ff456-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ff456-122">-NetworkWatcherName</span></span>
<span data-ttu-id="ff456-123">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="ff456-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="ff456-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff456-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff456-125">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="ff456-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ff456-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="ff456-126">-StorageId</span></span>
<span data-ttu-id="ff456-127">A ID de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ff456-127">The storage ID.</span></span>

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

### <span data-ttu-id="ff456-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="ff456-128">-StoragePath</span></span>
<span data-ttu-id="ff456-129">O caminho de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ff456-129">The storage path.</span></span>

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

### <span data-ttu-id="ff456-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ff456-130">-TargetResourceId</span></span>
<span data-ttu-id="ff456-131">Especifica a ID de recurso do recurso a ser solucionado.</span><span class="sxs-lookup"><span data-stu-id="ff456-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="ff456-132">Formato de exemplo: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="ff456-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="ff456-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff456-133">CommonParameters</span></span>
<span data-ttu-id="ff456-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff456-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff456-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff456-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff456-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="ff456-136">INPUTS</span></span>

### <span data-ttu-id="ff456-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff456-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ff456-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ff456-138">System.String</span></span>

## <span data-ttu-id="ff456-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="ff456-139">OUTPUTS</span></span>

### <span data-ttu-id="ff456-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ff456-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="ff456-141">Notas</span><span class="sxs-lookup"><span data-stu-id="ff456-141">NOTES</span></span>
<span data-ttu-id="ff456-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="ff456-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="ff456-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff456-143">RELATED LINKS</span></span>

[<span data-ttu-id="ff456-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff456-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ff456-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff456-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ff456-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff456-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ff456-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ff456-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ff456-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ff456-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ff456-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ff456-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ff456-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ff456-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ff456-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ff456-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ff456-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ff456-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ff456-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ff456-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ff456-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ff456-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ff456-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ff456-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ff456-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff456-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ff456-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ff456-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ff456-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ff456-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ff456-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff456-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ff456-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff456-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ff456-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff456-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ff456-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ff456-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ff456-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff456-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ff456-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff456-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ff456-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ff456-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ff456-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ff456-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ff456-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ff456-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ff456-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ff456-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ff456-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ff456-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ff456-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff456-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
