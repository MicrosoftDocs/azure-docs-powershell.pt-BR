---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 8253e43052203d4f5ba844cec02ec3b2af592b1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942057"
---
# <span data-ttu-id="ae0b6-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae0b6-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="ae0b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae0b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0b6-103">Cria um novo recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="ae0b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae0b6-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae0b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae0b6-105">DESCRIPTION</span></span>
<span data-ttu-id="ae0b6-106">O cmdlet New-AzNetworkWatcher cria um novo recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="ae0b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae0b6-107">EXAMPLES</span></span>

### <span data-ttu-id="ae0b6-108">Exemplo 1: criar um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="ae0b6-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="ae0b6-109">Este exemplo cria um novo inspetor de rede dentro de um grupo de recursos recém-criado.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="ae0b6-110">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="ae0b6-111">OS</span><span class="sxs-lookup"><span data-stu-id="ae0b6-111">PARAMETERS</span></span>

### <span data-ttu-id="ae0b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0b6-112">-DefaultProfile</span></span>
<span data-ttu-id="ae0b6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae0b6-114">-Local</span><span class="sxs-lookup"><span data-stu-id="ae0b6-114">-Location</span></span>
<span data-ttu-id="ae0b6-115">Ponto.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-115">Location.</span></span>

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

### <span data-ttu-id="ae0b6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae0b6-116">-Name</span></span>
<span data-ttu-id="ae0b6-117">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae0b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae0b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="ae0b6-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-119">The resource group name.</span></span>

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

### <span data-ttu-id="ae0b6-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="ae0b6-120">-Tag</span></span>
<span data-ttu-id="ae0b6-121">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae0b6-122">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ae0b6-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae0b6-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae0b6-123">-Confirm</span></span>
<span data-ttu-id="ae0b6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae0b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae0b6-125">-WhatIf</span></span>
<span data-ttu-id="ae0b6-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae0b6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae0b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0b6-128">CommonParameters</span></span>
<span data-ttu-id="ae0b6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0b6-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae0b6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0b6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae0b6-131">INPUTS</span></span>

### <span data-ttu-id="ae0b6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ae0b6-132">System.String</span></span>

### <span data-ttu-id="ae0b6-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae0b6-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ae0b6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae0b6-134">OUTPUTS</span></span>

### <span data-ttu-id="ae0b6-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae0b6-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="ae0b6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae0b6-136">NOTES</span></span>
<span data-ttu-id="ae0b6-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="ae0b6-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="ae0b6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae0b6-138">RELATED LINKS</span></span>

[<span data-ttu-id="ae0b6-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae0b6-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ae0b6-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae0b6-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ae0b6-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae0b6-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ae0b6-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ae0b6-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ae0b6-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ae0b6-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ae0b6-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ae0b6-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ae0b6-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ae0b6-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ae0b6-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae0b6-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae0b6-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ae0b6-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ae0b6-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae0b6-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae0b6-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae0b6-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae0b6-150">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae0b6-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae0b6-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae0b6-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ae0b6-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ae0b6-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ae0b6-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ae0b6-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ae0b6-154">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae0b6-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae0b6-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae0b6-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae0b6-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae0b6-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae0b6-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ae0b6-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ae0b6-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae0b6-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae0b6-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae0b6-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae0b6-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ae0b6-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ae0b6-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ae0b6-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ae0b6-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ae0b6-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ae0b6-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ae0b6-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ae0b6-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ae0b6-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ae0b6-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae0b6-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
