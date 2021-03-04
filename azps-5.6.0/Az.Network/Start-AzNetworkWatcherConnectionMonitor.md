---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f04fade3fcee4651c71432e7648fbec9725b6b01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885384"
---
# <span data-ttu-id="c153e-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c153e-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="c153e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c153e-102">SYNOPSIS</span></span>
<span data-ttu-id="c153e-103">Iniciar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="c153e-103">Start a connection monitor</span></span>

## <span data-ttu-id="c153e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c153e-104">SYNTAX</span></span>

### <span data-ttu-id="c153e-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c153e-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c153e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c153e-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c153e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c153e-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c153e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c153e-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c153e-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c153e-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c153e-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c153e-110">DESCRIPTION</span></span>
<span data-ttu-id="c153e-111">O Start-AzNetworkWatcherConnectionMonitor cmdlet inicia o monitor de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="c153e-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="c153e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c153e-112">EXAMPLES</span></span>

### <span data-ttu-id="c153e-113">Exemplo 1: Iniciar um monitor de conexão</span><span class="sxs-lookup"><span data-stu-id="c153e-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="c153e-114">Neste exemplo, iniciamos o monitor de conexão especificado pelo nome e pelo watcher de rede</span><span class="sxs-lookup"><span data-stu-id="c153e-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="c153e-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c153e-115">PARAMETERS</span></span>

### <span data-ttu-id="c153e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c153e-116">-AsJob</span></span>
<span data-ttu-id="c153e-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c153e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c153e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c153e-118">-DefaultProfile</span></span>
<span data-ttu-id="c153e-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c153e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c153e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c153e-120">-InputObject</span></span>
<span data-ttu-id="c153e-121">Objeto de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="c153e-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="c153e-122">-Location</span><span class="sxs-lookup"><span data-stu-id="c153e-122">-Location</span></span>
<span data-ttu-id="c153e-123">Local do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="c153e-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c153e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c153e-124">-Name</span></span>
<span data-ttu-id="c153e-125">O nome do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="c153e-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="c153e-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c153e-126">-NetworkWatcher</span></span>
<span data-ttu-id="c153e-127">O recurso do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="c153e-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="c153e-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c153e-128">-NetworkWatcherName</span></span>
<span data-ttu-id="c153e-129">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="c153e-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="c153e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c153e-130">-PassThru</span></span>
<span data-ttu-id="c153e-131">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c153e-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="c153e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c153e-132">-ResourceGroupName</span></span>
<span data-ttu-id="c153e-133">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="c153e-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c153e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c153e-134">-ResourceId</span></span>
<span data-ttu-id="c153e-135">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c153e-135">Resource ID.</span></span>

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

### <span data-ttu-id="c153e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c153e-136">-Confirm</span></span>
<span data-ttu-id="c153e-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c153e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c153e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c153e-138">-WhatIf</span></span>
<span data-ttu-id="c153e-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c153e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c153e-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c153e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c153e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c153e-141">CommonParameters</span></span>
<span data-ttu-id="c153e-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c153e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c153e-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c153e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c153e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c153e-144">INPUTS</span></span>

### <span data-ttu-id="c153e-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c153e-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c153e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c153e-146">System.String</span></span>

### <span data-ttu-id="c153e-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="c153e-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="c153e-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c153e-148">OUTPUTS</span></span>

### <span data-ttu-id="c153e-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c153e-149">System.Boolean</span></span>

## <span data-ttu-id="c153e-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="c153e-150">NOTES</span></span>
<span data-ttu-id="c153e-151">Palavras-chave: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span><span class="sxs-lookup"><span data-stu-id="c153e-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="c153e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c153e-152">RELATED LINKS</span></span>

[<span data-ttu-id="c153e-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c153e-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c153e-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c153e-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c153e-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c153e-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c153e-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c153e-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c153e-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c153e-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c153e-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c153e-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c153e-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c153e-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c153e-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c153e-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c153e-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c153e-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c153e-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c153e-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c153e-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c153e-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c153e-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c153e-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c153e-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c153e-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c153e-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c153e-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c153e-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c153e-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c153e-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c153e-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c153e-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c153e-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c153e-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c153e-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c153e-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c153e-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c153e-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c153e-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c153e-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c153e-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c153e-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c153e-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c153e-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c153e-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c153e-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c153e-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c153e-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c153e-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c153e-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c153e-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c153e-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c153e-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
