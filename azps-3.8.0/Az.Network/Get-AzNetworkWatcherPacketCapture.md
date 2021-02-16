---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e836bb8738b594e09c65568cc0f454a476db9d34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408875"
---
# <span data-ttu-id="5fc52-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc52-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="5fc52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fc52-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc52-103">Obtém informações, propriedades e status de um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="5fc52-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="5fc52-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fc52-104">SYNTAX</span></span>

### <span data-ttu-id="5fc52-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5fc52-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fc52-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5fc52-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fc52-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5fc52-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fc52-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fc52-108">DESCRIPTION</span></span>
<span data-ttu-id="5fc52-109">A Get-AzNetworkWatcherPacketCapture obtém as propriedades e o status de um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="5fc52-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="5fc52-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5fc52-110">EXAMPLES</span></span>

### <span data-ttu-id="5fc52-111">Exemplo 1: Criar uma Captura de Pacote com vários filtros e recuperar seu status</span><span class="sxs-lookup"><span data-stu-id="5fc52-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="5fc52-112">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="5fc52-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="5fc52-113">Quando a sessão for concluída, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="5fc52-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="5fc52-114">Em seguida, Get-AzNetworkWatcherPacketCapture para recuperar o status da sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="5fc52-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="5fc52-115">Observação: a extensão do Azure Network Watcher deve ser instalada na máquina virtual de destino para criar capturas de pacotes.</span><span class="sxs-lookup"><span data-stu-id="5fc52-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="5fc52-116">Se você criar uma referência à captura de pacote diretamente do comando New-AzNetworkWatcherPacketCapture, ela não terá todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="5fc52-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="5fc52-117">Você pode obter todas as propriedades da captura de pacote fazendo uma chamada para o Get-AzNetworkWatcherPacketCapture comando.</span><span class="sxs-lookup"><span data-stu-id="5fc52-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="5fc52-118">Exemplo 2: Criar uma Captura de Pacote com vários filtros e recuperar seu status</span><span class="sxs-lookup"><span data-stu-id="5fc52-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="5fc52-119">Este cmdlet retorna todas as PacketCaptures que começam com "PacketCapture" no Nw1 Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="5fc52-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="5fc52-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fc52-120">PARAMETERS</span></span>

### <span data-ttu-id="5fc52-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fc52-121">-AsJob</span></span>
<span data-ttu-id="5fc52-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5fc52-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fc52-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc52-123">-DefaultProfile</span></span>
<span data-ttu-id="5fc52-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5fc52-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fc52-125">-Local</span><span class="sxs-lookup"><span data-stu-id="5fc52-125">-Location</span></span>
<span data-ttu-id="5fc52-126">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="5fc52-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5fc52-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc52-127">-NetworkWatcher</span></span>
<span data-ttu-id="5fc52-128">O recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="5fc52-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="5fc52-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5fc52-129">-NetworkWatcherName</span></span>
<span data-ttu-id="5fc52-130">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="5fc52-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="5fc52-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="5fc52-131">-PacketCaptureName</span></span>
<span data-ttu-id="5fc52-132">O nome da captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="5fc52-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5fc52-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc52-133">-ResourceGroupName</span></span>
<span data-ttu-id="5fc52-134">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="5fc52-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5fc52-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc52-135">CommonParameters</span></span>
<span data-ttu-id="5fc52-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc52-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc52-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fc52-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc52-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="5fc52-138">INPUTS</span></span>

### <span data-ttu-id="5fc52-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc52-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="5fc52-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5fc52-140">System.String</span></span>

## <span data-ttu-id="5fc52-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="5fc52-141">OUTPUTS</span></span>

### <span data-ttu-id="5fc52-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="5fc52-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="5fc52-143">Notas</span><span class="sxs-lookup"><span data-stu-id="5fc52-143">NOTES</span></span>
<span data-ttu-id="5fc52-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="5fc52-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="5fc52-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fc52-145">RELATED LINKS</span></span>

[<span data-ttu-id="5fc52-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc52-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5fc52-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc52-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5fc52-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc52-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5fc52-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5fc52-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5fc52-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5fc52-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5fc52-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5fc52-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5fc52-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5fc52-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5fc52-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc52-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5fc52-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5fc52-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5fc52-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc52-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5fc52-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc52-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5fc52-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc52-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5fc52-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fc52-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5fc52-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5fc52-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5fc52-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5fc52-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5fc52-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc52-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc52-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc52-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc52-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc52-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc52-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5fc52-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5fc52-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc52-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc52-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc52-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc52-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5fc52-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5fc52-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5fc52-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5fc52-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5fc52-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5fc52-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5fc52-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5fc52-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5fc52-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5fc52-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc52-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

