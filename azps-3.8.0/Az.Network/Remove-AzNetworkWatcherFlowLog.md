---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 8a5f911529a4fc6f1ceb4e242b0e751e5f1a528f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944062"
---
# <span data-ttu-id="64a1f-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="64a1f-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="64a1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="64a1f-103">Exclui o recurso de log de fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="64a1f-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="64a1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64a1f-104">SYNTAX</span></span>

### <span data-ttu-id="64a1f-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="64a1f-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a1f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="64a1f-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a1f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="64a1f-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a1f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="64a1f-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a1f-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="64a1f-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a1f-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64a1f-110">DESCRIPTION</span></span>
<span data-ttu-id="64a1f-111">Exclui o recurso de log de fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="64a1f-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="64a1f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64a1f-112">EXAMPLES</span></span>

### <span data-ttu-id="64a1f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64a1f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="64a1f-114">OS</span><span class="sxs-lookup"><span data-stu-id="64a1f-114">PARAMETERS</span></span>

### <span data-ttu-id="64a1f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64a1f-115">-AsJob</span></span>
<span data-ttu-id="64a1f-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="64a1f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64a1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a1f-117">-DefaultProfile</span></span>
<span data-ttu-id="64a1f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64a1f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a1f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64a1f-119">-InputObject</span></span>
<span data-ttu-id="64a1f-120">Objeto de log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="64a1f-120">Flow log object.</span></span>

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

### <span data-ttu-id="64a1f-121">-Local</span><span class="sxs-lookup"><span data-stu-id="64a1f-121">-Location</span></span>
<span data-ttu-id="64a1f-122">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="64a1f-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="64a1f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="64a1f-123">-Name</span></span>
<span data-ttu-id="64a1f-124">O nome do log de fluxo.</span><span class="sxs-lookup"><span data-stu-id="64a1f-124">The flow log name.</span></span>

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

### <span data-ttu-id="64a1f-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64a1f-125">-NetworkWatcher</span></span>
<span data-ttu-id="64a1f-126">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="64a1f-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="64a1f-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="64a1f-127">-NetworkWatcherName</span></span>
<span data-ttu-id="64a1f-128">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="64a1f-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="64a1f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64a1f-129">-PassThru</span></span>
<span data-ttu-id="64a1f-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="64a1f-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="64a1f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a1f-131">-ResourceGroupName</span></span>
<span data-ttu-id="64a1f-132">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="64a1f-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="64a1f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64a1f-133">-ResourceId</span></span>
<span data-ttu-id="64a1f-134">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="64a1f-134">Resource ID.</span></span>

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

### <span data-ttu-id="64a1f-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64a1f-135">-Confirm</span></span>
<span data-ttu-id="64a1f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a1f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a1f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a1f-137">-WhatIf</span></span>
<span data-ttu-id="64a1f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64a1f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64a1f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64a1f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a1f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a1f-140">CommonParameters</span></span>
<span data-ttu-id="64a1f-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a1f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a1f-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64a1f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a1f-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64a1f-143">INPUTS</span></span>

### <span data-ttu-id="64a1f-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64a1f-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="64a1f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="64a1f-145">System.String</span></span>

### <span data-ttu-id="64a1f-146">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="64a1f-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="64a1f-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64a1f-147">OUTPUTS</span></span>

### <span data-ttu-id="64a1f-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64a1f-148">System.Boolean</span></span>

## <span data-ttu-id="64a1f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64a1f-149">NOTES</span></span>

## <span data-ttu-id="64a1f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64a1f-150">RELATED LINKS</span></span>

[<span data-ttu-id="64a1f-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64a1f-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="64a1f-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64a1f-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="64a1f-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64a1f-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="64a1f-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="64a1f-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="64a1f-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="64a1f-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="64a1f-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="64a1f-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="64a1f-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="64a1f-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="64a1f-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64a1f-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64a1f-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="64a1f-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="64a1f-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64a1f-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64a1f-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64a1f-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64a1f-162">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64a1f-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64a1f-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="64a1f-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="64a1f-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="64a1f-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="64a1f-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="64a1f-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="64a1f-166">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64a1f-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64a1f-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64a1f-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64a1f-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64a1f-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64a1f-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="64a1f-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="64a1f-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64a1f-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64a1f-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64a1f-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64a1f-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="64a1f-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="64a1f-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="64a1f-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="64a1f-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="64a1f-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="64a1f-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="64a1f-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="64a1f-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="64a1f-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="64a1f-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64a1f-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="64a1f-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="64a1f-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog)

[<span data-ttu-id="64a1f-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="64a1f-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="64a1f-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="64a1f-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)