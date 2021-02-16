---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 048eeb08b820f5eccd76a74587d4949f1f9de110
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408399"
---
# <span data-ttu-id="6d471-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d471-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="6d471-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d471-102">SYNOPSIS</span></span>
<span data-ttu-id="6d471-103">Interrompe uma sessão de captura de pacote em execução</span><span class="sxs-lookup"><span data-stu-id="6d471-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="6d471-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d471-104">SYNTAX</span></span>

### <span data-ttu-id="6d471-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d471-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d471-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6d471-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d471-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6d471-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d471-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d471-108">DESCRIPTION</span></span>
<span data-ttu-id="6d471-109">A Stop-AzNetworkWatcherPacketCapture interrompe uma sessão de captura de pacote em execução.</span><span class="sxs-lookup"><span data-stu-id="6d471-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="6d471-110">Depois que a sessão é interrompida, o arquivo de captura de pacote é carregado para armazenamento e/ou salvo localmente no VM, dependendo de sua configuração.</span><span class="sxs-lookup"><span data-stu-id="6d471-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="6d471-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d471-111">EXAMPLES</span></span>

### <span data-ttu-id="6d471-112">Exemplo 1: Interromper uma sessão de captura de pacote</span><span class="sxs-lookup"><span data-stu-id="6d471-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="6d471-113">Neste exemplo, paramos uma sessão de captura de pacote em execução chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="6d471-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="6d471-114">Depois que a sessão é interrompida, o arquivo de captura de pacote é carregado para armazenamento e/ou salvo localmente no VM, dependendo de sua configuração.</span><span class="sxs-lookup"><span data-stu-id="6d471-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="6d471-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d471-115">PARAMETERS</span></span>

### <span data-ttu-id="6d471-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d471-116">-AsJob</span></span>
<span data-ttu-id="6d471-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6d471-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d471-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d471-118">-DefaultProfile</span></span>
<span data-ttu-id="6d471-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6d471-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d471-120">-Local</span><span class="sxs-lookup"><span data-stu-id="6d471-120">-Location</span></span>
<span data-ttu-id="6d471-121">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="6d471-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6d471-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d471-122">-NetworkWatcher</span></span>
<span data-ttu-id="6d471-123">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="6d471-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="6d471-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6d471-124">-NetworkWatcherName</span></span>
<span data-ttu-id="6d471-125">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="6d471-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="6d471-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="6d471-126">-PacketCaptureName</span></span>
<span data-ttu-id="6d471-127">O nome da captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="6d471-127">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d471-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d471-128">-PassThru</span></span>
<span data-ttu-id="6d471-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="6d471-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="6d471-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d471-130">-ResourceGroupName</span></span>
<span data-ttu-id="6d471-131">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="6d471-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6d471-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6d471-132">-Confirm</span></span>
<span data-ttu-id="6d471-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d471-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d471-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d471-134">-WhatIf</span></span>
<span data-ttu-id="6d471-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6d471-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d471-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d471-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d471-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d471-137">CommonParameters</span></span>
<span data-ttu-id="6d471-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d471-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d471-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d471-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d471-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="6d471-140">INPUTS</span></span>

### <span data-ttu-id="6d471-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d471-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6d471-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6d471-142">System.String</span></span>

## <span data-ttu-id="6d471-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="6d471-143">OUTPUTS</span></span>

### <span data-ttu-id="6d471-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d471-144">System.Boolean</span></span>

## <span data-ttu-id="6d471-145">Notas</span><span class="sxs-lookup"><span data-stu-id="6d471-145">NOTES</span></span>
<span data-ttu-id="6d471-146">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="6d471-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="6d471-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d471-147">RELATED LINKS</span></span>

[<span data-ttu-id="6d471-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d471-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d471-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6d471-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6d471-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d471-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d471-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d471-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d471-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d471-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6d471-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d471-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6d471-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d471-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6d471-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6d471-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6d471-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6d471-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6d471-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6d471-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6d471-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6d471-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6d471-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6d471-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6d471-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6d471-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6d471-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d471-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d471-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d471-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6d471-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6d471-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6d471-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d471-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d471-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d471-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d471-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d471-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d471-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6d471-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6d471-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d471-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d471-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d471-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d471-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6d471-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6d471-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6d471-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6d471-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6d471-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6d471-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6d471-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6d471-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d471-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
