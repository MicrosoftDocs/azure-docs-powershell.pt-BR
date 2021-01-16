---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260235"
---
# <span data-ttu-id="60bb9-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60bb9-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="60bb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="60bb9-103">Remove um inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="60bb9-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="60bb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60bb9-104">SYNTAX</span></span>

### <span data-ttu-id="60bb9-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="60bb9-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60bb9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="60bb9-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60bb9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="60bb9-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60bb9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60bb9-108">DESCRIPTION</span></span>
<span data-ttu-id="60bb9-109">O cmdlet Remove-AzNetworkWatcher remove um recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="60bb9-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="60bb9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60bb9-110">EXAMPLES</span></span>

### <span data-ttu-id="60bb9-111">Exemplo 1: criar e excluir um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="60bb9-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="60bb9-112">Este exemplo cria um inspetor de rede em um grupo de recursos e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="60bb9-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="60bb9-113">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="60bb9-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="60bb9-114">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="60bb9-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="60bb9-115">OS</span><span class="sxs-lookup"><span data-stu-id="60bb9-115">PARAMETERS</span></span>

### <span data-ttu-id="60bb9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60bb9-116">-AsJob</span></span>
<span data-ttu-id="60bb9-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="60bb9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60bb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60bb9-118">-DefaultProfile</span></span>
<span data-ttu-id="60bb9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60bb9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60bb9-120">-Local</span><span class="sxs-lookup"><span data-stu-id="60bb9-120">-Location</span></span>
<span data-ttu-id="60bb9-121">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="60bb9-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="60bb9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="60bb9-122">-Name</span></span>
<span data-ttu-id="60bb9-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="60bb9-123">The resource name.</span></span>

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

### <span data-ttu-id="60bb9-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60bb9-124">-NetworkWatcher</span></span>
<span data-ttu-id="60bb9-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="60bb9-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="60bb9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60bb9-126">-PassThru</span></span>
<span data-ttu-id="60bb9-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="60bb9-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="60bb9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60bb9-128">-ResourceGroupName</span></span>
<span data-ttu-id="60bb9-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60bb9-129">The resource group name.</span></span>

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

### <span data-ttu-id="60bb9-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60bb9-130">-Confirm</span></span>
<span data-ttu-id="60bb9-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60bb9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60bb9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60bb9-132">-WhatIf</span></span>
<span data-ttu-id="60bb9-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60bb9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60bb9-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60bb9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60bb9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60bb9-135">CommonParameters</span></span>
<span data-ttu-id="60bb9-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60bb9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60bb9-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60bb9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60bb9-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60bb9-138">INPUTS</span></span>

### <span data-ttu-id="60bb9-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60bb9-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="60bb9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="60bb9-140">System.String</span></span>

## <span data-ttu-id="60bb9-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60bb9-141">OUTPUTS</span></span>

### <span data-ttu-id="60bb9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60bb9-142">System.Boolean</span></span>

## <span data-ttu-id="60bb9-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60bb9-143">NOTES</span></span>
<span data-ttu-id="60bb9-144">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="60bb9-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="60bb9-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60bb9-145">RELATED LINKS</span></span>

[<span data-ttu-id="60bb9-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60bb9-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="60bb9-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60bb9-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="60bb9-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="60bb9-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="60bb9-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="60bb9-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="60bb9-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="60bb9-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="60bb9-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="60bb9-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="60bb9-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="60bb9-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="60bb9-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60bb9-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="60bb9-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="60bb9-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="60bb9-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60bb9-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="60bb9-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60bb9-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="60bb9-157">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60bb9-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="60bb9-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="60bb9-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="60bb9-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="60bb9-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="60bb9-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="60bb9-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="60bb9-161">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="60bb9-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="60bb9-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="60bb9-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="60bb9-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="60bb9-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="60bb9-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="60bb9-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="60bb9-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="60bb9-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="60bb9-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="60bb9-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="60bb9-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="60bb9-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="60bb9-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="60bb9-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="60bb9-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="60bb9-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="60bb9-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="60bb9-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="60bb9-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="60bb9-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="60bb9-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="60bb9-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
