---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: f38250a4beed7eb05f758e17a1d3d17f1d76f86e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405186"
---
# <span data-ttu-id="fcf5c-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcf5c-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="fcf5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcf5c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf5c-103">Cria um novo recurso de Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="fcf5c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcf5c-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf5c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fcf5c-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf5c-106">O New-AzNetworkWatcher cmdlet cria um novo recurso do Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="fcf5c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fcf5c-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf5c-108">Exemplo 1: Criar um Watcher de Rede</span><span class="sxs-lookup"><span data-stu-id="fcf5c-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="fcf5c-109">Este exemplo cria um novo Watcher de Rede dentro de um Grupo de Recursos recém-criado.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="fcf5c-110">Observe que somente um Watcher de Rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="fcf5c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcf5c-111">PARAMETERS</span></span>

### <span data-ttu-id="fcf5c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf5c-112">-DefaultProfile</span></span>
<span data-ttu-id="fcf5c-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcf5c-114">-Local</span><span class="sxs-lookup"><span data-stu-id="fcf5c-114">-Location</span></span>
<span data-ttu-id="fcf5c-115">Localização.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-115">Location.</span></span>

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

### <span data-ttu-id="fcf5c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcf5c-116">-Name</span></span>
<span data-ttu-id="fcf5c-117">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-117">The network watcher name.</span></span>

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

### <span data-ttu-id="fcf5c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf5c-118">-ResourceGroupName</span></span>
<span data-ttu-id="fcf5c-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-119">The resource group name.</span></span>

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

### <span data-ttu-id="fcf5c-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="fcf5c-120">-Tag</span></span>
<span data-ttu-id="fcf5c-121">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fcf5c-122">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="fcf5c-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fcf5c-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fcf5c-123">-Confirm</span></span>
<span data-ttu-id="fcf5c-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf5c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf5c-125">-WhatIf</span></span>
<span data-ttu-id="fcf5c-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf5c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf5c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf5c-128">CommonParameters</span></span>
<span data-ttu-id="fcf5c-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf5c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf5c-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf5c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf5c-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="fcf5c-131">INPUTS</span></span>

### <span data-ttu-id="fcf5c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fcf5c-132">System.String</span></span>

### <span data-ttu-id="fcf5c-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fcf5c-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fcf5c-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="fcf5c-134">OUTPUTS</span></span>

### <span data-ttu-id="fcf5c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcf5c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="fcf5c-136">Notas</span><span class="sxs-lookup"><span data-stu-id="fcf5c-136">NOTES</span></span>
<span data-ttu-id="fcf5c-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="fcf5c-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="fcf5c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcf5c-138">RELATED LINKS</span></span>

[<span data-ttu-id="fcf5c-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcf5c-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fcf5c-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcf5c-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="fcf5c-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcf5c-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fcf5c-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fcf5c-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fcf5c-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fcf5c-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fcf5c-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fcf5c-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fcf5c-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fcf5c-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fcf5c-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcf5c-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcf5c-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fcf5c-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fcf5c-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcf5c-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcf5c-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcf5c-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcf5c-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcf5c-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcf5c-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fcf5c-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fcf5c-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fcf5c-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fcf5c-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fcf5c-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="fcf5c-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcf5c-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcf5c-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcf5c-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcf5c-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcf5c-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcf5c-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fcf5c-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fcf5c-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcf5c-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcf5c-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcf5c-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcf5c-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fcf5c-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fcf5c-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fcf5c-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fcf5c-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fcf5c-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fcf5c-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fcf5c-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fcf5c-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fcf5c-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="fcf5c-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcf5c-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
