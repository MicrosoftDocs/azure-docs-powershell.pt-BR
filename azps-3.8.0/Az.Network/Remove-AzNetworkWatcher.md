---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: fb2dfd74e4807aab76fb48a4593a8a46c4fe6f3f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398624"
---
# <span data-ttu-id="a858f-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a858f-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="a858f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a858f-102">SYNOPSIS</span></span>
<span data-ttu-id="a858f-103">Remove um Watcher de Rede.</span><span class="sxs-lookup"><span data-stu-id="a858f-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="a858f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a858f-104">SYNTAX</span></span>

### <span data-ttu-id="a858f-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a858f-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a858f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a858f-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a858f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a858f-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a858f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a858f-108">DESCRIPTION</span></span>
<span data-ttu-id="a858f-109">O Remove-AzNetworkWatcher cmdlet remove um recurso do Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="a858f-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="a858f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a858f-110">EXAMPLES</span></span>

### <span data-ttu-id="a858f-111">Exemplo 1: Criar e excluir um Watcher de Rede</span><span class="sxs-lookup"><span data-stu-id="a858f-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="a858f-112">Este exemplo cria um Watcher de Rede em um grupo de recursos e o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a858f-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="a858f-113">Observe que somente um Watcher de Rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="a858f-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="a858f-114">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador -Force.</span><span class="sxs-lookup"><span data-stu-id="a858f-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="a858f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a858f-115">PARAMETERS</span></span>

### <span data-ttu-id="a858f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a858f-116">-AsJob</span></span>
<span data-ttu-id="a858f-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a858f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a858f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a858f-118">-DefaultProfile</span></span>
<span data-ttu-id="a858f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a858f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a858f-120">-Local</span><span class="sxs-lookup"><span data-stu-id="a858f-120">-Location</span></span>
<span data-ttu-id="a858f-121">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="a858f-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a858f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a858f-122">-Name</span></span>
<span data-ttu-id="a858f-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a858f-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a858f-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a858f-124">-NetworkWatcher</span></span>
<span data-ttu-id="a858f-125">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="a858f-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="a858f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a858f-126">-PassThru</span></span>
<span data-ttu-id="a858f-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a858f-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="a858f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a858f-128">-ResourceGroupName</span></span>
<span data-ttu-id="a858f-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a858f-129">The resource group name.</span></span>

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

### <span data-ttu-id="a858f-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a858f-130">-Confirm</span></span>
<span data-ttu-id="a858f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a858f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a858f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a858f-132">-WhatIf</span></span>
<span data-ttu-id="a858f-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a858f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a858f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a858f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a858f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a858f-135">CommonParameters</span></span>
<span data-ttu-id="a858f-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a858f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a858f-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a858f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a858f-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="a858f-138">INPUTS</span></span>

### <span data-ttu-id="a858f-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a858f-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a858f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a858f-140">System.String</span></span>

## <span data-ttu-id="a858f-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="a858f-141">OUTPUTS</span></span>

### <span data-ttu-id="a858f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a858f-142">System.Boolean</span></span>

## <span data-ttu-id="a858f-143">Notas</span><span class="sxs-lookup"><span data-stu-id="a858f-143">NOTES</span></span>
<span data-ttu-id="a858f-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="a858f-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="a858f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a858f-145">RELATED LINKS</span></span>

[<span data-ttu-id="a858f-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a858f-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a858f-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a858f-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a858f-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a858f-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a858f-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a858f-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a858f-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a858f-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a858f-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a858f-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a858f-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a858f-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a858f-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a858f-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a858f-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a858f-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a858f-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a858f-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a858f-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a858f-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a858f-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a858f-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a858f-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a858f-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a858f-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a858f-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a858f-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a858f-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a858f-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a858f-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a858f-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a858f-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a858f-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a858f-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a858f-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a858f-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a858f-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a858f-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a858f-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a858f-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a858f-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a858f-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a858f-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a858f-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a858f-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a858f-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a858f-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a858f-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a858f-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a858f-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a858f-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a858f-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
