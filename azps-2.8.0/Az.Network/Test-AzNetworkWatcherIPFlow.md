---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 1d4bcd95ba526b8fc2d9c9bdc94e5fed3c042940
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408331"
---
# <span data-ttu-id="25d4e-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="25d4e-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="25d4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="25d4e-103">Retorna se o pacote é permitido ou negado a ou de um destino específico.</span><span class="sxs-lookup"><span data-stu-id="25d4e-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="25d4e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25d4e-104">SYNTAX</span></span>

### <span data-ttu-id="25d4e-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25d4e-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d4e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="25d4e-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d4e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="25d4e-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25d4e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="25d4e-108">DESCRIPTION</span></span>
<span data-ttu-id="25d4e-109">O cmdlet Test-AzNetworkWatcherIPFlow, para um recurso VM especificado e um pacote com direção especificada usando endereços IP locais e remotos, endereços IP e portas, retorna se o pacote é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="25d4e-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="25d4e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25d4e-110">EXAMPLES</span></span>

### <span data-ttu-id="25d4e-111">Exemplo 1: Executar Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="25d4e-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="25d4e-112">Obtém o Watcher de Rede na West Central US para esta assinatura, obtém o VM e as Interfaces de Rede associadas.</span><span class="sxs-lookup"><span data-stu-id="25d4e-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="25d4e-113">Em seguida, para a primeira Interface de Rede, executa Test-AzNetworkWatcherIPFlow usando o primeiro IP da primeira Interface de Rede para uma conexão de saída para um IP na Internet.</span><span class="sxs-lookup"><span data-stu-id="25d4e-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="25d4e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25d4e-114">PARAMETERS</span></span>

### <span data-ttu-id="25d4e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25d4e-115">-AsJob</span></span>
<span data-ttu-id="25d4e-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="25d4e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25d4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d4e-117">-DefaultProfile</span></span>
<span data-ttu-id="25d4e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="25d4e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25d4e-119">-Direção</span><span class="sxs-lookup"><span data-stu-id="25d4e-119">-Direction</span></span>
<span data-ttu-id="25d4e-120">Direção.</span><span class="sxs-lookup"><span data-stu-id="25d4e-120">Direction.</span></span>

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

### <span data-ttu-id="25d4e-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="25d4e-121">-LocalIPAddress</span></span>
<span data-ttu-id="25d4e-122">Endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="25d4e-122">Local IP Address.</span></span>

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

### <span data-ttu-id="25d4e-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="25d4e-123">-LocalPort</span></span>
<span data-ttu-id="25d4e-124">Porta local.</span><span class="sxs-lookup"><span data-stu-id="25d4e-124">Local Port.</span></span>

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

### <span data-ttu-id="25d4e-125">-Local</span><span class="sxs-lookup"><span data-stu-id="25d4e-125">-Location</span></span>
<span data-ttu-id="25d4e-126">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="25d4e-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="25d4e-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25d4e-127">-NetworkWatcher</span></span>
<span data-ttu-id="25d4e-128">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="25d4e-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="25d4e-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="25d4e-129">-NetworkWatcherName</span></span>
<span data-ttu-id="25d4e-130">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="25d4e-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="25d4e-131">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="25d4e-131">-Protocol</span></span>
<span data-ttu-id="25d4e-132">Protocolo.</span><span class="sxs-lookup"><span data-stu-id="25d4e-132">Protocol.</span></span>

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

### <span data-ttu-id="25d4e-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="25d4e-133">-RemoteIPAddress</span></span>
<span data-ttu-id="25d4e-134">Endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="25d4e-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="25d4e-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="25d4e-135">-RemotePort</span></span>
<span data-ttu-id="25d4e-136">Porta remota.</span><span class="sxs-lookup"><span data-stu-id="25d4e-136">Remote port.</span></span>

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

### <span data-ttu-id="25d4e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d4e-137">-ResourceGroupName</span></span>
<span data-ttu-id="25d4e-138">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="25d4e-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="25d4e-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="25d4e-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="25d4e-140">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="25d4e-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="25d4e-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="25d4e-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="25d4e-142">A ID do computador virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="25d4e-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="25d4e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d4e-143">CommonParameters</span></span>
<span data-ttu-id="25d4e-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d4e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d4e-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d4e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d4e-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="25d4e-146">INPUTS</span></span>

### <span data-ttu-id="25d4e-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25d4e-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="25d4e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="25d4e-148">System.String</span></span>

## <span data-ttu-id="25d4e-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="25d4e-149">OUTPUTS</span></span>

### <span data-ttu-id="25d4e-150">Microsoft.Azure.Commands.Network.Models.CASOPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="25d4e-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="25d4e-151">Notas</span><span class="sxs-lookup"><span data-stu-id="25d4e-151">NOTES</span></span>
<span data-ttu-id="25d4e-152">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="25d4e-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="25d4e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25d4e-153">RELATED LINKS</span></span>

[<span data-ttu-id="25d4e-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25d4e-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="25d4e-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25d4e-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="25d4e-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25d4e-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="25d4e-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="25d4e-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="25d4e-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="25d4e-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="25d4e-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="25d4e-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="25d4e-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="25d4e-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="25d4e-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25d4e-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="25d4e-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="25d4e-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="25d4e-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25d4e-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="25d4e-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25d4e-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="25d4e-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25d4e-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="25d4e-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="25d4e-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="25d4e-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="25d4e-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="25d4e-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="25d4e-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="25d4e-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25d4e-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="25d4e-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25d4e-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="25d4e-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25d4e-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="25d4e-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="25d4e-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="25d4e-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25d4e-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="25d4e-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25d4e-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="25d4e-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="25d4e-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="25d4e-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="25d4e-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="25d4e-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="25d4e-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="25d4e-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="25d4e-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="25d4e-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="25d4e-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="25d4e-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="25d4e-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
