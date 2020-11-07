---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954844"
---
# <span data-ttu-id="eebde-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eebde-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="eebde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eebde-102">SYNOPSIS</span></span>
<span data-ttu-id="eebde-103">Cria um novo recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="eebde-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="eebde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eebde-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eebde-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eebde-105">DESCRIPTION</span></span>
<span data-ttu-id="eebde-106">O cmdlet New-AzNetworkWatcher cria um novo recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="eebde-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="eebde-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eebde-107">EXAMPLES</span></span>

### <span data-ttu-id="eebde-108">Exemplo 1: criar um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="eebde-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="eebde-109">Este exemplo cria um novo inspetor de rede dentro de um grupo de recursos recém-criado.</span><span class="sxs-lookup"><span data-stu-id="eebde-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="eebde-110">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="eebde-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="eebde-111">OS</span><span class="sxs-lookup"><span data-stu-id="eebde-111">PARAMETERS</span></span>

### <span data-ttu-id="eebde-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebde-112">-DefaultProfile</span></span>
<span data-ttu-id="eebde-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eebde-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eebde-114">-Local</span><span class="sxs-lookup"><span data-stu-id="eebde-114">-Location</span></span>
<span data-ttu-id="eebde-115">Ponto.</span><span class="sxs-lookup"><span data-stu-id="eebde-115">Location.</span></span>

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

### <span data-ttu-id="eebde-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="eebde-116">-Name</span></span>
<span data-ttu-id="eebde-117">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="eebde-117">The network watcher name.</span></span>

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

### <span data-ttu-id="eebde-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eebde-118">-ResourceGroupName</span></span>
<span data-ttu-id="eebde-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eebde-119">The resource group name.</span></span>

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

### <span data-ttu-id="eebde-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="eebde-120">-Tag</span></span>
<span data-ttu-id="eebde-121">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="eebde-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eebde-122">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="eebde-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eebde-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eebde-123">-Confirm</span></span>
<span data-ttu-id="eebde-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eebde-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eebde-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eebde-125">-WhatIf</span></span>
<span data-ttu-id="eebde-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eebde-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eebde-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eebde-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eebde-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebde-128">CommonParameters</span></span>
<span data-ttu-id="eebde-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eebde-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebde-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eebde-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebde-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eebde-131">INPUTS</span></span>

### <span data-ttu-id="eebde-132">System. String</span><span class="sxs-lookup"><span data-stu-id="eebde-132">System.String</span></span>

### <span data-ttu-id="eebde-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eebde-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eebde-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eebde-134">OUTPUTS</span></span>

### <span data-ttu-id="eebde-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eebde-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="eebde-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eebde-136">NOTES</span></span>
<span data-ttu-id="eebde-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="eebde-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="eebde-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eebde-138">RELATED LINKS</span></span>

[<span data-ttu-id="eebde-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eebde-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="eebde-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eebde-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="eebde-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eebde-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="eebde-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="eebde-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="eebde-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="eebde-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="eebde-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="eebde-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="eebde-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="eebde-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="eebde-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eebde-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eebde-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="eebde-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="eebde-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eebde-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eebde-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eebde-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eebde-150">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eebde-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eebde-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="eebde-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="eebde-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="eebde-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="eebde-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="eebde-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="eebde-154">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="eebde-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="eebde-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="eebde-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="eebde-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="eebde-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="eebde-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="eebde-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="eebde-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="eebde-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="eebde-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="eebde-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="eebde-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="eebde-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="eebde-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="eebde-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="eebde-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="eebde-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="eebde-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="eebde-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="eebde-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="eebde-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="eebde-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="eebde-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
