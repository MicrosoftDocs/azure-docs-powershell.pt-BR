---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1276a3c63ec4b9c4ec1c2c4c91ea792013cbacc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110559"
---
# <span data-ttu-id="2441b-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2441b-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="2441b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2441b-102">SYNOPSIS</span></span>
<span data-ttu-id="2441b-103">Obtém informações e propriedades e status de um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="2441b-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="2441b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2441b-104">SYNTAX</span></span>

### <span data-ttu-id="2441b-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="2441b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2441b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2441b-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2441b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2441b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2441b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2441b-108">DESCRIPTION</span></span>
<span data-ttu-id="2441b-109">O Get-AzNetworkWatcherPacketCapture Obtém as propriedades e o status de um recurso de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="2441b-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="2441b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2441b-110">EXAMPLES</span></span>

### <span data-ttu-id="2441b-111">Exemplo 1: criar uma captura de pacote com vários filtros e recuperar seu status</span><span class="sxs-lookup"><span data-stu-id="2441b-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="2441b-112">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="2441b-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="2441b-113">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="2441b-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="2441b-114">Em seguida, chamamos Get-AzNetworkWatcherPacketCapture para recuperar o status da sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="2441b-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="2441b-115">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="2441b-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="2441b-116">Se você criar uma referência à captura de pacotes diretamente do comando New-AzNetworkWatcherPacketCapture, ela não terá todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="2441b-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="2441b-117">Você pode obter todas as propriedades da captura de pacotes fazendo uma chamada para o comando Get-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="2441b-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="2441b-118">Exemplo 2: criar uma captura de pacote com vários filtros e recuperar seu status</span><span class="sxs-lookup"><span data-stu-id="2441b-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="2441b-119">Esse cmdlet retorna todos os PacketCaptures que começam com "PacketCapture" no Inspetor de rede do NW1.</span><span class="sxs-lookup"><span data-stu-id="2441b-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="2441b-120">OS</span><span class="sxs-lookup"><span data-stu-id="2441b-120">PARAMETERS</span></span>

### <span data-ttu-id="2441b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2441b-121">-AsJob</span></span>
<span data-ttu-id="2441b-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2441b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2441b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2441b-123">-DefaultProfile</span></span>
<span data-ttu-id="2441b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2441b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2441b-125">-Local</span><span class="sxs-lookup"><span data-stu-id="2441b-125">-Location</span></span>
<span data-ttu-id="2441b-126">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2441b-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2441b-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2441b-127">-NetworkWatcher</span></span>
<span data-ttu-id="2441b-128">O recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2441b-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="2441b-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2441b-129">-NetworkWatcherName</span></span>
<span data-ttu-id="2441b-130">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2441b-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="2441b-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="2441b-131">-PacketCaptureName</span></span>
<span data-ttu-id="2441b-132">O nome de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="2441b-132">The packet capture name.</span></span>

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

### <span data-ttu-id="2441b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2441b-133">-ResourceGroupName</span></span>
<span data-ttu-id="2441b-134">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="2441b-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2441b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2441b-135">CommonParameters</span></span>
<span data-ttu-id="2441b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2441b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2441b-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2441b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2441b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2441b-138">INPUTS</span></span>

### <span data-ttu-id="2441b-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2441b-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2441b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2441b-140">System.String</span></span>

## <span data-ttu-id="2441b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2441b-141">OUTPUTS</span></span>

### <span data-ttu-id="2441b-142">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2441b-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="2441b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2441b-143">NOTES</span></span>
<span data-ttu-id="2441b-144">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, pacote, captura, tráfego</span><span class="sxs-lookup"><span data-stu-id="2441b-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="2441b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2441b-145">RELATED LINKS</span></span>

[<span data-ttu-id="2441b-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2441b-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2441b-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2441b-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2441b-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2441b-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2441b-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2441b-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2441b-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2441b-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2441b-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2441b-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2441b-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2441b-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2441b-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2441b-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2441b-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2441b-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2441b-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2441b-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2441b-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2441b-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2441b-157">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2441b-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2441b-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2441b-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2441b-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2441b-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2441b-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2441b-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2441b-161">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2441b-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2441b-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2441b-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2441b-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2441b-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2441b-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2441b-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2441b-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2441b-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2441b-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2441b-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2441b-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2441b-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2441b-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2441b-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2441b-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2441b-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2441b-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2441b-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2441b-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2441b-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2441b-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2441b-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

