---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6fc406d0af3ed451fbbf2f14c9ca8943256df744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441226"
---
# <span data-ttu-id="2cdbe-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2cdbe-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="2cdbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cdbe-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdbe-103">Retorna se o pacote é permitido ou negado para ou de um destino específico.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cdbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cdbe-104">SYNTAX</span></span>

### <span data-ttu-id="2cdbe-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="2cdbe-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cdbe-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2cdbe-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cdbe-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2cdbe-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cdbe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2cdbe-108">DESCRIPTION</span></span>
<span data-ttu-id="2cdbe-109">O cmdlet Test-AzureRmNetworkWatcherIPFlow, para um recurso VM especificado e um pacote com a direção especificada usando endereços IP e portas locais e remotos, retorna se o pacote é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-109">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="2cdbe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cdbe-110">EXAMPLES</span></span>

### <span data-ttu-id="2cdbe-111">Exemplo 1: executar Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2cdbe-111">Example 1: Run Test-AzureRmNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="2cdbe-112">Obtenha o Inspetor de rede na central oeste dos EUA para esta assinatura e, em seguida, obtenha a VM e as interfaces de rede associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="2cdbe-113">Em seguida, para a primeira interface de rede, executa Test-AzureRmNetworkWatcherIPFlow usando o primeiro IP da primeira interface de rede para uma conexão de saída com um IP na Internet.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-113">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="2cdbe-114">OS</span><span class="sxs-lookup"><span data-stu-id="2cdbe-114">PARAMETERS</span></span>

### <span data-ttu-id="2cdbe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cdbe-115">-AsJob</span></span>
<span data-ttu-id="2cdbe-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2cdbe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cdbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdbe-117">-DefaultProfile</span></span>
<span data-ttu-id="2cdbe-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cdbe-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="2cdbe-119">-Direction</span></span>
<span data-ttu-id="2cdbe-120">Direita.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cdbe-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="2cdbe-121">-LocalIPAddress</span></span>
<span data-ttu-id="2cdbe-122">Endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-122">Local IP Address.</span></span>

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

### <span data-ttu-id="2cdbe-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="2cdbe-123">-LocalPort</span></span>
<span data-ttu-id="2cdbe-124">Porta local.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-124">Local Port.</span></span>

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

### <span data-ttu-id="2cdbe-125">-Local</span><span class="sxs-lookup"><span data-stu-id="2cdbe-125">-Location</span></span>
<span data-ttu-id="2cdbe-126">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2cdbe-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdbe-127">-NetworkWatcher</span></span>
<span data-ttu-id="2cdbe-128">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="2cdbe-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2cdbe-129">-NetworkWatcherName</span></span>
<span data-ttu-id="2cdbe-130">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="2cdbe-131">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="2cdbe-131">-Protocol</span></span>
<span data-ttu-id="2cdbe-132">NNTP.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cdbe-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="2cdbe-133">-RemoteIPAddress</span></span>
<span data-ttu-id="2cdbe-134">Endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="2cdbe-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="2cdbe-135">-RemotePort</span></span>
<span data-ttu-id="2cdbe-136">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-136">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cdbe-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cdbe-137">-ResourceGroupName</span></span>
<span data-ttu-id="2cdbe-138">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2cdbe-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="2cdbe-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="2cdbe-140">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-140">Target network interface Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cdbe-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2cdbe-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2cdbe-142">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="2cdbe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdbe-143">CommonParameters</span></span>
<span data-ttu-id="2cdbe-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cdbe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdbe-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cdbe-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdbe-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2cdbe-146">INPUTS</span></span>

### <span data-ttu-id="2cdbe-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdbe-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2cdbe-148">Parâmetros: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2cdbe-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="2cdbe-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2cdbe-149">System.String</span></span>
<span data-ttu-id="2cdbe-150">Parâmetros: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2cdbe-150">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="2cdbe-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2cdbe-151">OUTPUTS</span></span>

### <span data-ttu-id="2cdbe-152">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="2cdbe-152">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="2cdbe-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2cdbe-153">NOTES</span></span>
<span data-ttu-id="2cdbe-154">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, fluxo, IP</span><span class="sxs-lookup"><span data-stu-id="2cdbe-154">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="2cdbe-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cdbe-155">RELATED LINKS</span></span>

[<span data-ttu-id="2cdbe-156">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdbe-156">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2cdbe-157">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdbe-157">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2cdbe-158">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdbe-158">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2cdbe-159">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2cdbe-159">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2cdbe-160">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2cdbe-160">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2cdbe-161">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2cdbe-161">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2cdbe-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2cdbe-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2cdbe-163">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cdbe-163">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cdbe-164">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2cdbe-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2cdbe-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cdbe-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cdbe-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cdbe-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cdbe-167">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cdbe-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cdbe-168">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cdbe-168">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2cdbe-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2cdbe-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2cdbe-170">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2cdbe-170">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="2cdbe-171">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdbe-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdbe-172">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdbe-172">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdbe-173">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdbe-173">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdbe-174">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2cdbe-174">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2cdbe-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdbe-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdbe-176">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdbe-176">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdbe-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2cdbe-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2cdbe-178">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2cdbe-178">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2cdbe-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2cdbe-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2cdbe-180">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2cdbe-180">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2cdbe-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2cdbe-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2cdbe-182">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdbe-182">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
