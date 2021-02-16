---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d6d11590699b52bb7245222ddaa01fbc42938d22
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398573"
---
# <span data-ttu-id="bb646-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb646-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="bb646-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb646-102">SYNOPSIS</span></span>
<span data-ttu-id="bb646-103">Remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="bb646-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="bb646-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb646-104">SYNTAX</span></span>

### <span data-ttu-id="bb646-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bb646-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb646-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bb646-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb646-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bb646-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb646-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb646-108">DESCRIPTION</span></span>
<span data-ttu-id="bb646-109">A Remove-AzNetworkWatcherPacketCapture remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="bb646-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="bb646-110">É recomendável ligar para Stop-AzNetworkWatcherPacketCapture antes de chamar Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="bb646-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="bb646-111">Se a sessão de captura de pacotes estiver em execução Remove-AzNetworkWatcherPacketCapture chamada de captura de pacote poderá não ser salva.</span><span class="sxs-lookup"><span data-stu-id="bb646-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="bb646-112">Se a sessão for interrompida antes da remoção, o arquivo .cap que contém dados de captura não será removido.</span><span class="sxs-lookup"><span data-stu-id="bb646-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="bb646-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb646-113">EXAMPLES</span></span>

### <span data-ttu-id="bb646-114">Exemplo 1: Remover uma sessão de captura de pacote</span><span class="sxs-lookup"><span data-stu-id="bb646-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="bb646-115">Neste exemplo, removemos uma sessão de captura de pacote existente chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="bb646-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="bb646-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb646-116">PARAMETERS</span></span>

### <span data-ttu-id="bb646-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb646-117">-AsJob</span></span>
<span data-ttu-id="bb646-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bb646-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb646-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb646-119">-DefaultProfile</span></span>
<span data-ttu-id="bb646-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bb646-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb646-121">-Local</span><span class="sxs-lookup"><span data-stu-id="bb646-121">-Location</span></span>
<span data-ttu-id="bb646-122">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="bb646-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bb646-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb646-123">-NetworkWatcher</span></span>
<span data-ttu-id="bb646-124">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="bb646-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="bb646-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bb646-125">-NetworkWatcherName</span></span>
<span data-ttu-id="bb646-126">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="bb646-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="bb646-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="bb646-127">-PacketCaptureName</span></span>
<span data-ttu-id="bb646-128">O nome da captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="bb646-128">The packet capture name.</span></span>

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

### <span data-ttu-id="bb646-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb646-129">-PassThru</span></span>
<span data-ttu-id="bb646-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="bb646-130">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb646-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb646-131">-ResourceGroupName</span></span>
<span data-ttu-id="bb646-132">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="bb646-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bb646-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bb646-133">-Confirm</span></span>
<span data-ttu-id="bb646-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb646-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb646-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb646-135">-WhatIf</span></span>
<span data-ttu-id="bb646-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bb646-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb646-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb646-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb646-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb646-138">CommonParameters</span></span>
<span data-ttu-id="bb646-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb646-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb646-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb646-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb646-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="bb646-141">INPUTS</span></span>

### <span data-ttu-id="bb646-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb646-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="bb646-143">System.String</span><span class="sxs-lookup"><span data-stu-id="bb646-143">System.String</span></span>

## <span data-ttu-id="bb646-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="bb646-144">OUTPUTS</span></span>

### <span data-ttu-id="bb646-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb646-145">System.Boolean</span></span>

## <span data-ttu-id="bb646-146">Notas</span><span class="sxs-lookup"><span data-stu-id="bb646-146">NOTES</span></span>
<span data-ttu-id="bb646-147">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span><span class="sxs-lookup"><span data-stu-id="bb646-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="bb646-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb646-148">RELATED LINKS</span></span>

[<span data-ttu-id="bb646-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb646-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bb646-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb646-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bb646-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bb646-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bb646-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bb646-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bb646-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bb646-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bb646-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bb646-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bb646-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bb646-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bb646-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb646-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb646-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bb646-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bb646-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb646-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb646-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb646-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb646-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bb646-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bb646-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb646-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="bb646-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bb646-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bb646-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bb646-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="bb646-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb646-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb646-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb646-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb646-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb646-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb646-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bb646-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="bb646-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb646-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb646-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb646-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bb646-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bb646-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="bb646-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bb646-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="bb646-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bb646-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="bb646-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bb646-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bb646-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bb646-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="bb646-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bb646-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
