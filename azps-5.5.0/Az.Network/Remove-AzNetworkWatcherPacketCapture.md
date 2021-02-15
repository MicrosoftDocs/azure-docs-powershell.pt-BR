---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e22b9d85bbc17897742fa2ac0cbdf3e2d8187d5b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114112"
---
# <span data-ttu-id="576b6-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="576b6-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="576b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="576b6-102">SYNOPSIS</span></span>
<span data-ttu-id="576b6-103">Remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="576b6-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="576b6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="576b6-104">SYNTAX</span></span>

### <span data-ttu-id="576b6-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="576b6-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576b6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="576b6-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576b6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="576b6-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576b6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="576b6-108">DESCRIPTION</span></span>
<span data-ttu-id="576b6-109">A Remove-AzNetworkWatcherPacketCapture remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="576b6-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="576b6-110">É recomendável ligar para Stop-AzNetworkWatcherPacketCapture antes de chamar Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="576b6-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="576b6-111">Se a sessão de captura de pacote estiver em execução Remove-AzNetworkWatcherPacketCapture chamada de captura de pacote poderá não ser salva.</span><span class="sxs-lookup"><span data-stu-id="576b6-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="576b6-112">Se a sessão for interrompida antes da remoção, o arquivo .cap que contém dados de captura não será removido.</span><span class="sxs-lookup"><span data-stu-id="576b6-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="576b6-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="576b6-113">EXAMPLES</span></span>

### <span data-ttu-id="576b6-114">Exemplo 1: Remover uma sessão de captura de pacote</span><span class="sxs-lookup"><span data-stu-id="576b6-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="576b6-115">Neste exemplo, removemos uma sessão de captura de pacote existente chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="576b6-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="576b6-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="576b6-116">PARAMETERS</span></span>

### <span data-ttu-id="576b6-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="576b6-117">-AsJob</span></span>
<span data-ttu-id="576b6-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="576b6-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="576b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576b6-119">-DefaultProfile</span></span>
<span data-ttu-id="576b6-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="576b6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="576b6-121">-Local</span><span class="sxs-lookup"><span data-stu-id="576b6-121">-Location</span></span>
<span data-ttu-id="576b6-122">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="576b6-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="576b6-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="576b6-123">-NetworkWatcher</span></span>
<span data-ttu-id="576b6-124">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="576b6-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="576b6-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="576b6-125">-NetworkWatcherName</span></span>
<span data-ttu-id="576b6-126">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="576b6-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="576b6-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="576b6-127">-PacketCaptureName</span></span>
<span data-ttu-id="576b6-128">O nome da captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="576b6-128">The packet capture name.</span></span>

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

### <span data-ttu-id="576b6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="576b6-129">-PassThru</span></span>
<span data-ttu-id="576b6-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="576b6-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="576b6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="576b6-131">-ResourceGroupName</span></span>
<span data-ttu-id="576b6-132">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="576b6-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="576b6-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="576b6-133">-Confirm</span></span>
<span data-ttu-id="576b6-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576b6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576b6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576b6-135">-WhatIf</span></span>
<span data-ttu-id="576b6-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="576b6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="576b6-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="576b6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576b6-138">CommonParameters</span></span>
<span data-ttu-id="576b6-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576b6-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="576b6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576b6-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="576b6-141">INPUTS</span></span>

### <span data-ttu-id="576b6-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="576b6-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="576b6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="576b6-143">System.String</span></span>

## <span data-ttu-id="576b6-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="576b6-144">OUTPUTS</span></span>

### <span data-ttu-id="576b6-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="576b6-145">System.Boolean</span></span>

## <span data-ttu-id="576b6-146">Notas</span><span class="sxs-lookup"><span data-stu-id="576b6-146">NOTES</span></span>
<span data-ttu-id="576b6-147">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span><span class="sxs-lookup"><span data-stu-id="576b6-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="576b6-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="576b6-148">RELATED LINKS</span></span>

[<span data-ttu-id="576b6-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="576b6-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="576b6-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="576b6-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="576b6-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="576b6-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="576b6-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="576b6-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="576b6-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="576b6-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="576b6-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="576b6-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="576b6-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="576b6-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="576b6-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="576b6-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="576b6-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="576b6-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="576b6-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="576b6-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="576b6-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="576b6-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="576b6-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="576b6-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="576b6-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="576b6-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="576b6-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="576b6-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="576b6-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="576b6-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="576b6-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="576b6-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="576b6-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="576b6-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="576b6-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="576b6-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="576b6-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="576b6-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="576b6-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="576b6-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="576b6-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="576b6-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="576b6-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="576b6-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="576b6-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="576b6-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="576b6-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="576b6-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="576b6-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="576b6-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="576b6-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="576b6-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="576b6-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="576b6-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
