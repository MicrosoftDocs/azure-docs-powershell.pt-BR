---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 51fea717c352f00b4f356e6bb07b730cdeb60966
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600521"
---
# <span data-ttu-id="f72ce-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f72ce-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="f72ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f72ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f72ce-103">Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="f72ce-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="f72ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f72ce-104">SYNTAX</span></span>

### <span data-ttu-id="f72ce-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f72ce-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f72ce-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f72ce-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f72ce-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f72ce-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f72ce-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f72ce-108">DESCRIPTION</span></span>
<span data-ttu-id="f72ce-109">O cmdlet Get-AzNetworkWatcherNextHop Obtém o próximo salto de uma VM.</span><span class="sxs-lookup"><span data-stu-id="f72ce-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="f72ce-110">Próximo nó permite exibir o tipo de recurso do Azure, o endereço IP associado do recurso e a regra da tabela de roteamento que é responsável pela rota.</span><span class="sxs-lookup"><span data-stu-id="f72ce-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="f72ce-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f72ce-111">EXAMPLES</span></span>

### <span data-ttu-id="f72ce-112">Exemplo 1: obter o próximo salto ao se comunicar com um IP de Internet</span><span class="sxs-lookup"><span data-stu-id="f72ce-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="f72ce-113">Obter o próximo salto para a comunicação de saída da interface de rede principal no Vachine virtual especificado para 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="f72ce-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="f72ce-114">OS</span><span class="sxs-lookup"><span data-stu-id="f72ce-114">PARAMETERS</span></span>

### <span data-ttu-id="f72ce-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f72ce-115">-AsJob</span></span>
<span data-ttu-id="f72ce-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f72ce-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f72ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72ce-117">-DefaultProfile</span></span>
<span data-ttu-id="f72ce-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f72ce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f72ce-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="f72ce-119">-DestinationIPAddress</span></span>
<span data-ttu-id="f72ce-120">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="f72ce-120">Destination IP address.</span></span>

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

### <span data-ttu-id="f72ce-121">-Local</span><span class="sxs-lookup"><span data-stu-id="f72ce-121">-Location</span></span>
<span data-ttu-id="f72ce-122">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f72ce-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f72ce-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f72ce-123">-NetworkWatcher</span></span>
<span data-ttu-id="f72ce-124">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f72ce-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="f72ce-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f72ce-125">-NetworkWatcherName</span></span>
<span data-ttu-id="f72ce-126">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f72ce-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="f72ce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f72ce-127">-ResourceGroupName</span></span>
<span data-ttu-id="f72ce-128">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f72ce-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f72ce-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="f72ce-129">-SourceIPAddress</span></span>
<span data-ttu-id="f72ce-130">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="f72ce-130">Source IP address.</span></span>

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

### <span data-ttu-id="f72ce-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="f72ce-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f72ce-132">ID da interface de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="f72ce-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="f72ce-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f72ce-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f72ce-134">A ID da máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="f72ce-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f72ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72ce-135">CommonParameters</span></span>
<span data-ttu-id="f72ce-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72ce-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f72ce-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72ce-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f72ce-138">INPUTS</span></span>

### <span data-ttu-id="f72ce-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f72ce-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f72ce-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f72ce-140">System.String</span></span>

## <span data-ttu-id="f72ce-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f72ce-141">OUTPUTS</span></span>

### <span data-ttu-id="f72ce-142">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="f72ce-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="f72ce-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f72ce-143">NOTES</span></span>
<span data-ttu-id="f72ce-144">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, observador de rede, próximo, salto</span><span class="sxs-lookup"><span data-stu-id="f72ce-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="f72ce-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f72ce-145">RELATED LINKS</span></span>

[<span data-ttu-id="f72ce-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f72ce-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f72ce-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f72ce-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f72ce-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f72ce-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f72ce-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f72ce-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f72ce-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f72ce-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f72ce-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f72ce-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f72ce-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f72ce-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f72ce-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f72ce-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f72ce-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f72ce-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f72ce-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f72ce-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f72ce-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f72ce-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f72ce-157">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f72ce-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f72ce-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f72ce-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f72ce-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f72ce-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f72ce-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f72ce-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f72ce-161">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f72ce-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f72ce-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f72ce-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f72ce-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f72ce-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f72ce-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f72ce-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f72ce-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f72ce-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f72ce-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f72ce-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f72ce-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f72ce-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f72ce-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f72ce-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f72ce-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f72ce-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f72ce-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f72ce-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f72ce-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f72ce-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="f72ce-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f72ce-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
