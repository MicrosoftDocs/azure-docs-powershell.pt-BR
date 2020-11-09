---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: cf120e8e9ca9e0dad8f4d430c7f207d40fcfab3b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282242"
---
# <span data-ttu-id="2bffc-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2bffc-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="2bffc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bffc-102">SYNOPSIS</span></span>
<span data-ttu-id="2bffc-103">Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="2bffc-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="2bffc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bffc-104">SYNTAX</span></span>

### <span data-ttu-id="2bffc-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="2bffc-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bffc-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2bffc-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bffc-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2bffc-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bffc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bffc-108">DESCRIPTION</span></span>
<span data-ttu-id="2bffc-109">O cmdlet Get-AzNetworkWatcherNextHop Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="2bffc-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="2bffc-110">Próximo nó permite exibir o tipo de recurso do Azure, o endereço IP associado do recurso e a regra da tabela de roteamento que é responsável pela rota.</span><span class="sxs-lookup"><span data-stu-id="2bffc-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="2bffc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bffc-111">EXAMPLES</span></span>

### <span data-ttu-id="2bffc-112">Exemplo 1: obter o próximo salto ao se comunicar com um IP de Internet</span><span class="sxs-lookup"><span data-stu-id="2bffc-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="2bffc-113">Obtém o próximo salto para comunicação de saída da interface de rede principal na máquina virtual especificada para 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="2bffc-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="2bffc-114">OS</span><span class="sxs-lookup"><span data-stu-id="2bffc-114">PARAMETERS</span></span>

### <span data-ttu-id="2bffc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bffc-115">-AsJob</span></span>
<span data-ttu-id="2bffc-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2bffc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bffc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bffc-117">-DefaultProfile</span></span>
<span data-ttu-id="2bffc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bffc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bffc-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="2bffc-119">-DestinationIPAddress</span></span>
<span data-ttu-id="2bffc-120">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="2bffc-120">Destination IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bffc-121">-Local</span><span class="sxs-lookup"><span data-stu-id="2bffc-121">-Location</span></span>
<span data-ttu-id="2bffc-122">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2bffc-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2bffc-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2bffc-123">-NetworkWatcher</span></span>
<span data-ttu-id="2bffc-124">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2bffc-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="2bffc-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2bffc-125">-NetworkWatcherName</span></span>
<span data-ttu-id="2bffc-126">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2bffc-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="2bffc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bffc-127">-ResourceGroupName</span></span>
<span data-ttu-id="2bffc-128">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2bffc-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2bffc-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="2bffc-129">-SourceIPAddress</span></span>
<span data-ttu-id="2bffc-130">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="2bffc-130">Source IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bffc-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="2bffc-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="2bffc-132">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="2bffc-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="2bffc-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2bffc-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2bffc-134">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="2bffc-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="2bffc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bffc-135">CommonParameters</span></span>
<span data-ttu-id="2bffc-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bffc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bffc-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bffc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bffc-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bffc-138">INPUTS</span></span>

### <span data-ttu-id="2bffc-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2bffc-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2bffc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2bffc-140">System.String</span></span>

## <span data-ttu-id="2bffc-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bffc-141">OUTPUTS</span></span>

### <span data-ttu-id="2bffc-142">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="2bffc-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="2bffc-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bffc-143">NOTES</span></span>
<span data-ttu-id="2bffc-144">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="2bffc-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="2bffc-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bffc-145">RELATED LINKS</span></span>

[<span data-ttu-id="2bffc-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2bffc-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2bffc-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2bffc-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2bffc-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2bffc-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2bffc-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2bffc-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2bffc-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2bffc-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2bffc-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2bffc-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2bffc-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2bffc-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2bffc-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2bffc-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2bffc-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2bffc-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2bffc-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2bffc-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2bffc-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2bffc-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2bffc-157">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2bffc-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2bffc-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bffc-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2bffc-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2bffc-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2bffc-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2bffc-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2bffc-161">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2bffc-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2bffc-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2bffc-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2bffc-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2bffc-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2bffc-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2bffc-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2bffc-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2bffc-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2bffc-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2bffc-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2bffc-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2bffc-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2bffc-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2bffc-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2bffc-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2bffc-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2bffc-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2bffc-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2bffc-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2bffc-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2bffc-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2bffc-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
