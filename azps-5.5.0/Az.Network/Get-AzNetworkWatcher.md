---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: ea4eb4b7c6a8b88d78db809ee85ab0f484a9eba6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395632"
---
# <span data-ttu-id="0e048-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e048-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="0e048-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e048-102">SYNOPSIS</span></span>
<span data-ttu-id="0e048-103">Obtém as propriedades de um Watcher de Rede</span><span class="sxs-lookup"><span data-stu-id="0e048-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="0e048-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e048-104">SYNTAX</span></span>

### <span data-ttu-id="0e048-105">Lista</span><span class="sxs-lookup"><span data-stu-id="0e048-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e048-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0e048-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e048-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e048-107">DESCRIPTION</span></span>
<span data-ttu-id="0e048-108">O Get-AzNetworkWatcher cmdlet obtém um ou mais recursos do Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="0e048-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="0e048-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e048-109">EXAMPLES</span></span>

### <span data-ttu-id="0e048-110">Exemplo 1: Obter um Watcher de Rede</span><span class="sxs-lookup"><span data-stu-id="0e048-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="0e048-111">Obtém o Watcher de Rede NetworkWatcher_westcentralus nomeada no grupo de recursos NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="0e048-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="0e048-112">Exemplo 2: Listar Watchers de Rede usando filtragem</span><span class="sxs-lookup"><span data-stu-id="0e048-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="0e048-113">Obtém os Watchers de Rede que começam com "NetworkWatcher"</span><span class="sxs-lookup"><span data-stu-id="0e048-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="0e048-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e048-114">PARAMETERS</span></span>

### <span data-ttu-id="0e048-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e048-115">-DefaultProfile</span></span>
<span data-ttu-id="0e048-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0e048-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e048-117">-Local</span><span class="sxs-lookup"><span data-stu-id="0e048-117">-Location</span></span>
<span data-ttu-id="0e048-118">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="0e048-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0e048-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e048-119">-Name</span></span>
<span data-ttu-id="0e048-120">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="0e048-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0e048-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e048-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e048-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e048-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0e048-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e048-123">CommonParameters</span></span>
<span data-ttu-id="0e048-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e048-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e048-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e048-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e048-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="0e048-126">INPUTS</span></span>

### <span data-ttu-id="0e048-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0e048-127">None</span></span>

## <span data-ttu-id="0e048-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="0e048-128">OUTPUTS</span></span>

### <span data-ttu-id="0e048-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e048-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="0e048-130">Notas</span><span class="sxs-lookup"><span data-stu-id="0e048-130">NOTES</span></span>
<span data-ttu-id="0e048-131">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="0e048-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="0e048-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e048-132">RELATED LINKS</span></span>

[<span data-ttu-id="0e048-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e048-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0e048-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e048-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0e048-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e048-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0e048-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0e048-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0e048-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0e048-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0e048-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0e048-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0e048-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0e048-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0e048-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e048-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e048-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0e048-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0e048-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e048-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e048-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e048-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e048-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e048-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e048-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e048-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0e048-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0e048-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0e048-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0e048-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0e048-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e048-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e048-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e048-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e048-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e048-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e048-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0e048-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0e048-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e048-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e048-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e048-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e048-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0e048-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0e048-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0e048-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0e048-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0e048-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0e048-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0e048-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0e048-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0e048-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0e048-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e048-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
