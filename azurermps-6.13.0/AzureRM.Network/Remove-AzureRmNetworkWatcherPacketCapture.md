---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0c0568dc11411e27af1db9d9e3d59c0026b0a39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440342"
---
# <span data-ttu-id="4a71a-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a71a-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="4a71a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a71a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a71a-103">Remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="4a71a-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a71a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a71a-104">SYNTAX</span></span>

### <span data-ttu-id="4a71a-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a71a-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a71a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4a71a-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a71a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4a71a-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a71a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a71a-108">DESCRIPTION</span></span>
<span data-ttu-id="4a71a-109">O Remove-AzureRmNetworkWatcherPacketCapture remove um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="4a71a-109">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="4a71a-110">É recomendável chamar Stop-AzureRmNetworkWatcherPacketCapture antes de chamar remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="4a71a-110">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="4a71a-111">Se a sessão de captura de pacotes estiver em execução quando Remove-AzureRmNetworkWatcherPacketCapture for chamado, a captura de pacotes pode não ser salva.</span><span class="sxs-lookup"><span data-stu-id="4a71a-111">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="4a71a-112">Se a sessão for interrompida antes da remoção, o arquivo. Cap contendo dados de captura não será removido.</span><span class="sxs-lookup"><span data-stu-id="4a71a-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="4a71a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a71a-113">EXAMPLES</span></span>

### <span data-ttu-id="4a71a-114">Exemplo 1: remover uma sessão de captura de pacote</span><span class="sxs-lookup"><span data-stu-id="4a71a-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="4a71a-115">Neste exemplo, removemos uma sessão de captura de pacote existente chamada "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="4a71a-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="4a71a-116">OS</span><span class="sxs-lookup"><span data-stu-id="4a71a-116">PARAMETERS</span></span>

### <span data-ttu-id="4a71a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a71a-117">-AsJob</span></span>
<span data-ttu-id="4a71a-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4a71a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a71a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a71a-119">-DefaultProfile</span></span>
<span data-ttu-id="4a71a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a71a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a71a-121">-Local</span><span class="sxs-lookup"><span data-stu-id="4a71a-121">-Location</span></span>
<span data-ttu-id="4a71a-122">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="4a71a-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4a71a-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a71a-123">-NetworkWatcher</span></span>
<span data-ttu-id="4a71a-124">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="4a71a-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="4a71a-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4a71a-125">-NetworkWatcherName</span></span>
<span data-ttu-id="4a71a-126">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="4a71a-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="4a71a-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="4a71a-127">-PacketCaptureName</span></span>
<span data-ttu-id="4a71a-128">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="4a71a-128">The packet capture name.</span></span>

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

### <span data-ttu-id="4a71a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a71a-129">-PassThru</span></span>
<span data-ttu-id="4a71a-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="4a71a-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4a71a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a71a-131">-ResourceGroupName</span></span>
<span data-ttu-id="4a71a-132">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="4a71a-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4a71a-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a71a-133">-Confirm</span></span>
<span data-ttu-id="4a71a-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a71a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a71a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a71a-135">-WhatIf</span></span>
<span data-ttu-id="4a71a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a71a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a71a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a71a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a71a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a71a-138">CommonParameters</span></span>
<span data-ttu-id="4a71a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a71a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a71a-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a71a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a71a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a71a-141">INPUTS</span></span>

### <span data-ttu-id="4a71a-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a71a-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4a71a-143">Parâmetros: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4a71a-143">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="4a71a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4a71a-144">System.String</span></span>
<span data-ttu-id="4a71a-145">Parâmetros: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4a71a-145">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="4a71a-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a71a-146">OUTPUTS</span></span>

### <span data-ttu-id="4a71a-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a71a-147">System.Boolean</span></span>

## <span data-ttu-id="4a71a-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a71a-148">NOTES</span></span>
<span data-ttu-id="4a71a-149">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego, remover</span><span class="sxs-lookup"><span data-stu-id="4a71a-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="4a71a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a71a-150">RELATED LINKS</span></span>

[<span data-ttu-id="4a71a-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a71a-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4a71a-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a71a-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4a71a-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a71a-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4a71a-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4a71a-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4a71a-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4a71a-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4a71a-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4a71a-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4a71a-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4a71a-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4a71a-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a71a-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a71a-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4a71a-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4a71a-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a71a-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a71a-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a71a-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a71a-162">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a71a-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a71a-163">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a71a-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4a71a-164">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4a71a-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4a71a-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4a71a-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="4a71a-166">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a71a-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a71a-167">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a71a-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a71a-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a71a-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a71a-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4a71a-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4a71a-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a71a-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a71a-171">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a71a-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a71a-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4a71a-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4a71a-173">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4a71a-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4a71a-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4a71a-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4a71a-175">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4a71a-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4a71a-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4a71a-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4a71a-177">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a71a-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
