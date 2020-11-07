---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ceb03c58c7f7c3983f89073b5bad2428a32b7934
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772708"
---
# <span data-ttu-id="28d23-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28d23-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="28d23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28d23-102">SYNOPSIS</span></span>
<span data-ttu-id="28d23-103">Parar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="28d23-103">Stop a connection monitor</span></span>

## <span data-ttu-id="28d23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28d23-104">SYNTAX</span></span>

### <span data-ttu-id="28d23-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="28d23-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d23-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="28d23-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d23-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="28d23-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d23-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="28d23-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d23-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="28d23-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28d23-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28d23-110">DESCRIPTION</span></span>
<span data-ttu-id="28d23-111">O cmdlet Stop-AzNetworkWatcherConnectionMonitor interrompe o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="28d23-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="28d23-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28d23-112">EXAMPLES</span></span>

### <span data-ttu-id="28d23-113">Exemplo 1: parar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="28d23-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="28d23-114">Neste exemplo, interrompemos o monitor de conexão especificado pelo nome e Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="28d23-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="28d23-115">OS</span><span class="sxs-lookup"><span data-stu-id="28d23-115">PARAMETERS</span></span>

### <span data-ttu-id="28d23-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28d23-116">-AsJob</span></span>
<span data-ttu-id="28d23-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28d23-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28d23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d23-118">-DefaultProfile</span></span>
<span data-ttu-id="28d23-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28d23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28d23-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28d23-120">-InputObject</span></span>
<span data-ttu-id="28d23-121">Objeto monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="28d23-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28d23-122">-Local</span><span class="sxs-lookup"><span data-stu-id="28d23-122">-Location</span></span>
<span data-ttu-id="28d23-123">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="28d23-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="28d23-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="28d23-124">-Name</span></span>
<span data-ttu-id="28d23-125">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="28d23-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d23-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28d23-126">-NetworkWatcher</span></span>
<span data-ttu-id="28d23-127">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="28d23-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="28d23-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="28d23-128">-NetworkWatcherName</span></span>
<span data-ttu-id="28d23-129">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="28d23-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d23-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28d23-130">-PassThru</span></span>
<span data-ttu-id="28d23-131">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="28d23-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="28d23-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d23-132">-ResourceGroupName</span></span>
<span data-ttu-id="28d23-133">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="28d23-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d23-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28d23-134">-ResourceId</span></span>
<span data-ttu-id="28d23-135">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="28d23-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28d23-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28d23-136">-Confirm</span></span>
<span data-ttu-id="28d23-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28d23-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d23-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d23-138">-WhatIf</span></span>
<span data-ttu-id="28d23-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28d23-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28d23-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28d23-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d23-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d23-141">CommonParameters</span></span>
<span data-ttu-id="28d23-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28d23-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d23-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d23-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d23-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28d23-144">INPUTS</span></span>

### <span data-ttu-id="28d23-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28d23-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="28d23-146">System. String</span><span class="sxs-lookup"><span data-stu-id="28d23-146">System.String</span></span>

### <span data-ttu-id="28d23-147">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="28d23-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="28d23-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28d23-148">OUTPUTS</span></span>

### <span data-ttu-id="28d23-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28d23-149">System.Boolean</span></span>

## <span data-ttu-id="28d23-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28d23-150">NOTES</span></span>
<span data-ttu-id="28d23-151">Palavras-chave: Azure, azurerm, ARM, recurso, conectividade, gerenciamento, gerente, rede, rede, observador de rede, monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="28d23-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="28d23-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28d23-152">RELATED LINKS</span></span>

[<span data-ttu-id="28d23-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28d23-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="28d23-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28d23-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="28d23-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28d23-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="28d23-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="28d23-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="28d23-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="28d23-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="28d23-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="28d23-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="28d23-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="28d23-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="28d23-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="28d23-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="28d23-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="28d23-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="28d23-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="28d23-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="28d23-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="28d23-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="28d23-164">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="28d23-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="28d23-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28d23-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="28d23-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="28d23-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="28d23-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28d23-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="28d23-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28d23-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="28d23-169">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28d23-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="28d23-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28d23-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="28d23-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="28d23-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="28d23-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="28d23-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="28d23-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="28d23-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="28d23-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="28d23-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="28d23-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28d23-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="28d23-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="28d23-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="28d23-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="28d23-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="28d23-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="28d23-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="28d23-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="28d23-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)