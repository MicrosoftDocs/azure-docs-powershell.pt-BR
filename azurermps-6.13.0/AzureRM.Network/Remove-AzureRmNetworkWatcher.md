---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: a242c1cbeda2a110f7bb58e8c320f2e9b4d60ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440344"
---
# <span data-ttu-id="e2cca-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2cca-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="e2cca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2cca-102">SYNOPSIS</span></span>
<span data-ttu-id="e2cca-103">Remove um inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e2cca-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2cca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2cca-104">SYNTAX</span></span>

### <span data-ttu-id="e2cca-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e2cca-105">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2cca-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e2cca-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2cca-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e2cca-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2cca-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2cca-108">DESCRIPTION</span></span>
<span data-ttu-id="e2cca-109">O cmdlet Remove-AzureRmNetworkWatcher remove um recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e2cca-109">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="e2cca-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2cca-110">EXAMPLES</span></span>

### <span data-ttu-id="e2cca-111">Exemplo 1: criar e excluir um inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="e2cca-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="e2cca-112">Este exemplo cria um inspetor de rede em um grupo de recursos e, em seguida, o exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e2cca-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e2cca-113">Observe que apenas um observador de rede pode ser criado por região por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2cca-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="e2cca-114">Para suprimir o prompt ao excluir a rede virtual, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="e2cca-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="e2cca-115">OS</span><span class="sxs-lookup"><span data-stu-id="e2cca-115">PARAMETERS</span></span>

### <span data-ttu-id="e2cca-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2cca-116">-AsJob</span></span>
<span data-ttu-id="e2cca-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e2cca-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2cca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2cca-118">-DefaultProfile</span></span>
<span data-ttu-id="e2cca-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2cca-120">-Local</span><span class="sxs-lookup"><span data-stu-id="e2cca-120">-Location</span></span>
<span data-ttu-id="e2cca-121">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e2cca-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e2cca-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2cca-122">-Name</span></span>
<span data-ttu-id="e2cca-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e2cca-123">The resource name.</span></span>

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

### <span data-ttu-id="e2cca-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2cca-124">-NetworkWatcher</span></span>
<span data-ttu-id="e2cca-125">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e2cca-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="e2cca-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2cca-126">-PassThru</span></span>
<span data-ttu-id="e2cca-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="e2cca-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e2cca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2cca-128">-ResourceGroupName</span></span>
<span data-ttu-id="e2cca-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2cca-129">The resource group name.</span></span>

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

### <span data-ttu-id="e2cca-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2cca-130">-Confirm</span></span>
<span data-ttu-id="e2cca-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2cca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2cca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2cca-132">-WhatIf</span></span>
<span data-ttu-id="e2cca-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2cca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2cca-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2cca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2cca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2cca-135">CommonParameters</span></span>
<span data-ttu-id="e2cca-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2cca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2cca-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2cca-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2cca-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2cca-138">INPUTS</span></span>

### <span data-ttu-id="e2cca-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2cca-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e2cca-140">Parâmetros: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2cca-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="e2cca-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e2cca-141">System.String</span></span>
<span data-ttu-id="e2cca-142">Parâmetros: nome (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2cca-142">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="e2cca-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2cca-143">OUTPUTS</span></span>

### <span data-ttu-id="e2cca-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2cca-144">System.Boolean</span></span>

## <span data-ttu-id="e2cca-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2cca-145">NOTES</span></span>
<span data-ttu-id="e2cca-146">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="e2cca-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="e2cca-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2cca-147">RELATED LINKS</span></span>

[<span data-ttu-id="e2cca-148">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2cca-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e2cca-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2cca-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e2cca-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2cca-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e2cca-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e2cca-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="e2cca-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e2cca-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e2cca-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e2cca-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e2cca-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e2cca-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e2cca-155">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2cca-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2cca-156">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e2cca-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e2cca-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2cca-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2cca-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2cca-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2cca-159">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2cca-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2cca-160">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2cca-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e2cca-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e2cca-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e2cca-162">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e2cca-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="e2cca-163">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2cca-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2cca-164">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2cca-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2cca-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2cca-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2cca-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e2cca-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e2cca-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2cca-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2cca-168">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2cca-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2cca-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e2cca-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e2cca-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e2cca-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e2cca-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e2cca-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e2cca-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e2cca-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e2cca-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e2cca-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="e2cca-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2cca-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
