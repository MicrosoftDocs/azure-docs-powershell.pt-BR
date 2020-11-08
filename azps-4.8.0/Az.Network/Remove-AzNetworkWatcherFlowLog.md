---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 9906af7da12f76650ebbe45ff764da78c90ef340
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110446"
---
# <span data-ttu-id="c39af-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c39af-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="c39af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c39af-102">SYNOPSIS</span></span>
<span data-ttu-id="c39af-103">Exclui o recurso de log de fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="c39af-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="c39af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c39af-104">SYNTAX</span></span>

### <span data-ttu-id="c39af-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c39af-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c39af-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c39af-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c39af-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c39af-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c39af-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c39af-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c39af-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c39af-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c39af-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c39af-110">DESCRIPTION</span></span>
<span data-ttu-id="c39af-111">Exclui o recurso de log de fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="c39af-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="c39af-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c39af-112">EXAMPLES</span></span>

### <span data-ttu-id="c39af-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c39af-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="c39af-114">OS</span><span class="sxs-lookup"><span data-stu-id="c39af-114">PARAMETERS</span></span>

### <span data-ttu-id="c39af-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c39af-115">-AsJob</span></span>
<span data-ttu-id="c39af-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c39af-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39af-117">-DefaultProfile</span></span>
<span data-ttu-id="c39af-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c39af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c39af-119">-InputObject</span></span>
<span data-ttu-id="c39af-120">Objeto de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c39af-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-121">-Local</span><span class="sxs-lookup"><span data-stu-id="c39af-121">-Location</span></span>
<span data-ttu-id="c39af-122">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c39af-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c39af-123">-Name</span></span>
<span data-ttu-id="c39af-124">O nome do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="c39af-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c39af-125">-NetworkWatcher</span></span>
<span data-ttu-id="c39af-126">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c39af-126">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c39af-127">-NetworkWatcherName</span></span>
<span data-ttu-id="c39af-128">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c39af-128">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c39af-129">-PassThru</span></span>
<span data-ttu-id="c39af-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="c39af-130">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39af-131">-ResourceGroupName</span></span>
<span data-ttu-id="c39af-132">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="c39af-132">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c39af-133">-ResourceId</span></span>
<span data-ttu-id="c39af-134">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c39af-134">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c39af-135">-Confirm</span></span>
<span data-ttu-id="c39af-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c39af-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39af-137">-WhatIf</span></span>
<span data-ttu-id="c39af-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c39af-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39af-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c39af-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39af-140">CommonParameters</span></span>
<span data-ttu-id="c39af-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c39af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39af-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c39af-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39af-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c39af-143">INPUTS</span></span>

### <span data-ttu-id="c39af-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c39af-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c39af-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c39af-145">System.String</span></span>

### <span data-ttu-id="c39af-146">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="c39af-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="c39af-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c39af-147">OUTPUTS</span></span>

### <span data-ttu-id="c39af-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c39af-148">System.Boolean</span></span>

## <span data-ttu-id="c39af-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c39af-149">NOTES</span></span>

## <span data-ttu-id="c39af-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c39af-150">RELATED LINKS</span></span>

[<span data-ttu-id="c39af-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c39af-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c39af-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c39af-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c39af-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c39af-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c39af-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c39af-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c39af-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c39af-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c39af-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c39af-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c39af-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c39af-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c39af-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c39af-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c39af-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c39af-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c39af-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c39af-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c39af-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c39af-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c39af-162">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c39af-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c39af-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c39af-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c39af-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c39af-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c39af-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c39af-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c39af-166">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c39af-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c39af-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c39af-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c39af-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c39af-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c39af-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c39af-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c39af-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c39af-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c39af-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c39af-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c39af-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c39af-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c39af-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c39af-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c39af-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c39af-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c39af-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c39af-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c39af-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c39af-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c39af-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c39af-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="c39af-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c39af-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="c39af-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c39af-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="c39af-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="c39af-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
