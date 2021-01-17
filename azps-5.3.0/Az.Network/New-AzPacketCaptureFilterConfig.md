---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 194e3c71cc763aeb74091f912b37dd15e4dfe4aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428128"
---
# <span data-ttu-id="87b5c-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="87b5c-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="87b5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="87b5c-103">Cria um novo objeto de filtro de captura de pacotes.</span><span class="sxs-lookup"><span data-stu-id="87b5c-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="87b5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87b5c-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87b5c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87b5c-105">DESCRIPTION</span></span>
<span data-ttu-id="87b5c-106">O cmdlet New-AzPacketCaptureFilterConfig cria um novo objeto de filtro de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="87b5c-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="87b5c-107">Esse objeto é usado para restringir o tipo de pacotes que são capturados durante uma sessão de captura de pacote usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="87b5c-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="87b5c-108">O cmdlet New-AzNetworkWatcherPacketCapture pode aceitar vários objetos de filtro para habilitar as sessões de captura combináveis.</span><span class="sxs-lookup"><span data-stu-id="87b5c-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="87b5c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87b5c-109">EXAMPLES</span></span>

### <span data-ttu-id="87b5c-110">Exemplo 1: criar uma captura de pacotes com vários filtros</span><span class="sxs-lookup"><span data-stu-id="87b5c-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="87b5c-111">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="87b5c-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="87b5c-112">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="87b5c-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="87b5c-113">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="87b5c-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="87b5c-114">OS</span><span class="sxs-lookup"><span data-stu-id="87b5c-114">PARAMETERS</span></span>

### <span data-ttu-id="87b5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b5c-115">-DefaultProfile</span></span>
<span data-ttu-id="87b5c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87b5c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b5c-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="87b5c-117">-LocalIPAddress</span></span>
<span data-ttu-id="87b5c-118">Especifica o endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="87b5c-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="87b5c-119">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="87b5c-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="87b5c-120">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="87b5c-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="87b5c-121">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="87b5c-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="87b5c-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="87b5c-122">-LocalPort</span></span>
<span data-ttu-id="87b5c-123">Especifica o endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="87b5c-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="87b5c-124">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="87b5c-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="87b5c-125">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="87b5c-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="87b5c-126">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="87b5c-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="87b5c-127">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="87b5c-127">-Protocol</span></span>
<span data-ttu-id="87b5c-128">Especifica o protocolo para filtrar.</span><span class="sxs-lookup"><span data-stu-id="87b5c-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="87b5c-129">Valores aceitáveis "TCP", "UDP", "qualquer"</span><span class="sxs-lookup"><span data-stu-id="87b5c-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87b5c-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="87b5c-130">-RemoteIPAddress</span></span>
<span data-ttu-id="87b5c-131">Especifica o endereço IP remoto para filtrar.</span><span class="sxs-lookup"><span data-stu-id="87b5c-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="87b5c-132">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="87b5c-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="87b5c-133">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="87b5c-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="87b5c-134">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="87b5c-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="87b5c-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="87b5c-135">-RemotePort</span></span>
<span data-ttu-id="87b5c-136">Especifica a porta remota para filtrar.</span><span class="sxs-lookup"><span data-stu-id="87b5c-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="87b5c-137">Entradas de exemplo de porta remota: "80" para entrada de porta única.</span><span class="sxs-lookup"><span data-stu-id="87b5c-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="87b5c-138">"80-85" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="87b5c-138">"80-85" for range.</span></span>
<span data-ttu-id="87b5c-139">"80; 443;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="87b5c-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="87b5c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b5c-140">CommonParameters</span></span>
<span data-ttu-id="87b5c-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b5c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b5c-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b5c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b5c-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87b5c-143">INPUTS</span></span>

### <span data-ttu-id="87b5c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="87b5c-144">System.String</span></span>

## <span data-ttu-id="87b5c-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87b5c-145">OUTPUTS</span></span>

### <span data-ttu-id="87b5c-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="87b5c-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="87b5c-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87b5c-147">NOTES</span></span>
<span data-ttu-id="87b5c-148">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, pacote, captura, tráfego, filtro</span><span class="sxs-lookup"><span data-stu-id="87b5c-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="87b5c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87b5c-149">RELATED LINKS</span></span>

[<span data-ttu-id="87b5c-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87b5c-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="87b5c-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87b5c-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="87b5c-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87b5c-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="87b5c-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="87b5c-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="87b5c-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="87b5c-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="87b5c-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="87b5c-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="87b5c-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="87b5c-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="87b5c-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87b5c-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87b5c-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="87b5c-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="87b5c-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87b5c-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87b5c-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87b5c-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87b5c-161">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87b5c-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87b5c-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="87b5c-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="87b5c-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="87b5c-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="87b5c-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="87b5c-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="87b5c-165">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87b5c-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87b5c-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87b5c-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87b5c-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87b5c-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87b5c-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="87b5c-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="87b5c-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87b5c-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87b5c-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87b5c-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87b5c-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="87b5c-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="87b5c-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="87b5c-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="87b5c-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="87b5c-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="87b5c-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="87b5c-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="87b5c-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="87b5c-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="87b5c-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87b5c-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
