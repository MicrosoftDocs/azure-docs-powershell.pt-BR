---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 922026b14531cc1c65f60901914383b402d06889
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110398"
---
# <span data-ttu-id="1dc27-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1dc27-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="1dc27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dc27-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc27-103">Interrompe uma sessão de captura de pacote em execução</span><span class="sxs-lookup"><span data-stu-id="1dc27-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="1dc27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dc27-104">SYNTAX</span></span>

### <span data-ttu-id="1dc27-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="1dc27-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc27-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1dc27-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc27-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1dc27-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc27-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dc27-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc27-109">O Stop-AzNetworkWatcherPacketCapture para de uma sessão de captura de pacote em execução.</span><span class="sxs-lookup"><span data-stu-id="1dc27-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="1dc27-110">Depois que a sessão for interrompida, o arquivo de captura de pacote será carregado no armazenamento e/ou salvo localmente na VM, dependendo da configuração.</span><span class="sxs-lookup"><span data-stu-id="1dc27-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="1dc27-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dc27-111">EXAMPLES</span></span>

### <span data-ttu-id="1dc27-112">Exemplo 1: parar uma sessão de captura de pacote</span><span class="sxs-lookup"><span data-stu-id="1dc27-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="1dc27-113">Neste exemplo, vamos parar uma sessão de captura de pacote em execução chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="1dc27-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="1dc27-114">Depois que a sessão for interrompida, o arquivo de captura de pacote será carregado no armazenamento e/ou salvo localmente na VM, dependendo da configuração.</span><span class="sxs-lookup"><span data-stu-id="1dc27-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="1dc27-115">OS</span><span class="sxs-lookup"><span data-stu-id="1dc27-115">PARAMETERS</span></span>

### <span data-ttu-id="1dc27-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dc27-116">-AsJob</span></span>
<span data-ttu-id="1dc27-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1dc27-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dc27-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc27-118">-DefaultProfile</span></span>
<span data-ttu-id="1dc27-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc27-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc27-120">-Local</span><span class="sxs-lookup"><span data-stu-id="1dc27-120">-Location</span></span>
<span data-ttu-id="1dc27-121">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1dc27-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1dc27-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1dc27-122">-NetworkWatcher</span></span>
<span data-ttu-id="1dc27-123">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1dc27-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="1dc27-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1dc27-124">-NetworkWatcherName</span></span>
<span data-ttu-id="1dc27-125">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1dc27-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="1dc27-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="1dc27-126">-PacketCaptureName</span></span>
<span data-ttu-id="1dc27-127">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="1dc27-127">The packet capture name.</span></span>

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

### <span data-ttu-id="1dc27-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dc27-128">-PassThru</span></span>
<span data-ttu-id="1dc27-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1dc27-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="1dc27-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc27-130">-ResourceGroupName</span></span>
<span data-ttu-id="1dc27-131">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="1dc27-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1dc27-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1dc27-132">-Confirm</span></span>
<span data-ttu-id="1dc27-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc27-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc27-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc27-134">-WhatIf</span></span>
<span data-ttu-id="1dc27-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1dc27-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc27-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1dc27-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc27-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc27-137">CommonParameters</span></span>
<span data-ttu-id="1dc27-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc27-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc27-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc27-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc27-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dc27-140">INPUTS</span></span>

### <span data-ttu-id="1dc27-141">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1dc27-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1dc27-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc27-142">System.String</span></span>

## <span data-ttu-id="1dc27-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dc27-143">OUTPUTS</span></span>

### <span data-ttu-id="1dc27-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dc27-144">System.Boolean</span></span>

## <span data-ttu-id="1dc27-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dc27-145">NOTES</span></span>
<span data-ttu-id="1dc27-146">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="1dc27-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="1dc27-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dc27-147">RELATED LINKS</span></span>

[<span data-ttu-id="1dc27-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1dc27-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1dc27-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1dc27-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1dc27-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1dc27-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1dc27-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1dc27-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1dc27-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1dc27-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1dc27-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1dc27-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1dc27-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1dc27-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1dc27-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1dc27-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1dc27-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1dc27-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1dc27-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1dc27-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1dc27-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1dc27-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1dc27-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1dc27-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1dc27-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1dc27-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1dc27-161">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1dc27-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1dc27-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dc27-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1dc27-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1dc27-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1dc27-164">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1dc27-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1dc27-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1dc27-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1dc27-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1dc27-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1dc27-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1dc27-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1dc27-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1dc27-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1dc27-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1dc27-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1dc27-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1dc27-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1dc27-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1dc27-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1dc27-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1dc27-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1dc27-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1dc27-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1dc27-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1dc27-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
