---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: fe5236d6f98cc78ed19c4fd3e5cf4a066d841fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600528"
---
# <span data-ttu-id="f7f11-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7f11-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="f7f11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7f11-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f11-103">Obtém as propriedades de um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="f7f11-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="f7f11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7f11-104">SYNTAX</span></span>

### <span data-ttu-id="f7f11-105">Programação</span><span class="sxs-lookup"><span data-stu-id="f7f11-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7f11-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f7f11-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7f11-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7f11-107">DESCRIPTION</span></span>
<span data-ttu-id="f7f11-108">O cmdlet Get-AzNetworkWatcher Obtém um ou mais recursos do Inspetor de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f11-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="f7f11-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7f11-109">EXAMPLES</span></span>

### <span data-ttu-id="f7f11-110">Exemplo 1: obter um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="f7f11-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="f7f11-111">Obtém o Inspetor de rede chamado NetworkWatcher_westcentralus na NetworkWatcherRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7f11-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="f7f11-112">Exemplo 2: listar os inspetores de rede usando filtragem</span><span class="sxs-lookup"><span data-stu-id="f7f11-112">Example 2: List Network Watchers using filtering</span></span>
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

<span data-ttu-id="f7f11-113">Obtém os inspetores de rede que começam com "NetworkWatcher"</span><span class="sxs-lookup"><span data-stu-id="f7f11-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="f7f11-114">OS</span><span class="sxs-lookup"><span data-stu-id="f7f11-114">PARAMETERS</span></span>

### <span data-ttu-id="f7f11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f11-115">-DefaultProfile</span></span>
<span data-ttu-id="f7f11-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7f11-117">-Local</span><span class="sxs-lookup"><span data-stu-id="f7f11-117">-Location</span></span>
<span data-ttu-id="f7f11-118">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f7f11-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f7f11-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7f11-119">-Name</span></span>
<span data-ttu-id="f7f11-120">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f7f11-120">The network watcher name.</span></span>

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

### <span data-ttu-id="f7f11-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f11-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7f11-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7f11-122">The resource group name.</span></span>

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

### <span data-ttu-id="f7f11-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f11-123">CommonParameters</span></span>
<span data-ttu-id="f7f11-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f11-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f11-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7f11-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f11-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7f11-126">INPUTS</span></span>

### <span data-ttu-id="f7f11-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f7f11-127">None</span></span>

## <span data-ttu-id="f7f11-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7f11-128">OUTPUTS</span></span>

### <span data-ttu-id="f7f11-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7f11-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="f7f11-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7f11-130">NOTES</span></span>
<span data-ttu-id="f7f11-131">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="f7f11-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="f7f11-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7f11-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7f11-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7f11-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f7f11-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7f11-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f7f11-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7f11-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f7f11-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f7f11-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f7f11-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f7f11-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f7f11-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f7f11-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f7f11-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f7f11-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f7f11-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7f11-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7f11-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f7f11-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f7f11-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7f11-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7f11-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7f11-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7f11-144">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7f11-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7f11-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7f11-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f7f11-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f7f11-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f7f11-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f7f11-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f7f11-148">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7f11-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7f11-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7f11-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7f11-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7f11-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7f11-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f7f11-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f7f11-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7f11-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7f11-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7f11-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f7f11-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f7f11-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f7f11-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f7f11-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f7f11-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f7f11-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f7f11-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f7f11-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f7f11-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f7f11-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="f7f11-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f7f11-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
