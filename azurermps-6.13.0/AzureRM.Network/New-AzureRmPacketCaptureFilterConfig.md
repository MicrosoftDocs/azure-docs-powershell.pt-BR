---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: 3c69884e988b10f41da4d41d98318ee96c019112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441241"
---
# <span data-ttu-id="d7adb-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d7adb-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="d7adb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7adb-102">SYNOPSIS</span></span>
<span data-ttu-id="d7adb-103">Cria um novo objeto de filtro de captura de pacotes.</span><span class="sxs-lookup"><span data-stu-id="d7adb-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7adb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7adb-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7adb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7adb-105">DESCRIPTION</span></span>
<span data-ttu-id="d7adb-106">O cmdlet New-AzureRmPacketCaptureFilterConfig cria um novo objeto de filtro de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="d7adb-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="d7adb-107">Esse objeto é usado para restringir o tipo de pacotes que são capturados durante uma sessão de captura de pacote usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="d7adb-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="d7adb-108">O cmdlet New-AzureRmNetworkWatcherPacketCapture pode aceitar vários objetos de filtro para habilitar as sessões de captura combináveis.</span><span class="sxs-lookup"><span data-stu-id="d7adb-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="d7adb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7adb-109">EXAMPLES</span></span>

### <span data-ttu-id="d7adb-110">Exemplo 1: criar uma captura de pacotes com vários filtros</span><span class="sxs-lookup"><span data-stu-id="d7adb-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="d7adb-111">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="d7adb-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d7adb-112">Após a conclusão da sessão, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="d7adb-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="d7adb-113">Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.</span><span class="sxs-lookup"><span data-stu-id="d7adb-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="d7adb-114">OS</span><span class="sxs-lookup"><span data-stu-id="d7adb-114">PARAMETERS</span></span>

### <span data-ttu-id="d7adb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7adb-115">-DefaultProfile</span></span>
<span data-ttu-id="d7adb-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7adb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7adb-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="d7adb-117">-LocalIPAddress</span></span>
<span data-ttu-id="d7adb-118">Especifica o endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="d7adb-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="d7adb-119">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="d7adb-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d7adb-120">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="d7adb-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d7adb-121">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="d7adb-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d7adb-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="d7adb-122">-LocalPort</span></span>
<span data-ttu-id="d7adb-123">Especifica o endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="d7adb-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="d7adb-124">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="d7adb-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d7adb-125">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="d7adb-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d7adb-126">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="d7adb-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d7adb-127">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="d7adb-127">-Protocol</span></span>
<span data-ttu-id="d7adb-128">Especifica o Procotol para filtrar.</span><span class="sxs-lookup"><span data-stu-id="d7adb-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="d7adb-129">Valores aceitáveis "TCP", "UDP", "qualquer"</span><span class="sxs-lookup"><span data-stu-id="d7adb-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="d7adb-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="d7adb-130">-RemoteIPAddress</span></span>
<span data-ttu-id="d7adb-131">Especifica o endereço IP remoto para filtrar.</span><span class="sxs-lookup"><span data-stu-id="d7adb-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="d7adb-132">Exemplos de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="d7adb-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d7adb-133">"127.0.0.1-127.0.0.255" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="d7adb-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d7adb-134">"127.0.0.1; 127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="d7adb-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d7adb-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="d7adb-135">-RemotePort</span></span>
<span data-ttu-id="d7adb-136">Especifica a porta remota para filtrar.</span><span class="sxs-lookup"><span data-stu-id="d7adb-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="d7adb-137">Entradas de exemplo de porta remota: "80" para entrada de porta única.</span><span class="sxs-lookup"><span data-stu-id="d7adb-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="d7adb-138">"80-85" para o intervalo.</span><span class="sxs-lookup"><span data-stu-id="d7adb-138">"80-85" for range.</span></span>
<span data-ttu-id="d7adb-139">"80; 443;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="d7adb-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="d7adb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7adb-140">CommonParameters</span></span>
<span data-ttu-id="d7adb-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7adb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7adb-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7adb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7adb-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7adb-143">INPUTS</span></span>

### <span data-ttu-id="d7adb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d7adb-144">System.String</span></span>
<span data-ttu-id="d7adb-145">Parâmetros: Protocol (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7adb-145">Parameters: Protocol (ByValue)</span></span>

## <span data-ttu-id="d7adb-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7adb-146">OUTPUTS</span></span>

### <span data-ttu-id="d7adb-147">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="d7adb-147">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="d7adb-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7adb-148">NOTES</span></span>
<span data-ttu-id="d7adb-149">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, pacote, captura, tráfego, filtro</span><span class="sxs-lookup"><span data-stu-id="d7adb-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="d7adb-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7adb-150">RELATED LINKS</span></span>

[<span data-ttu-id="d7adb-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7adb-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d7adb-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7adb-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d7adb-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7adb-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d7adb-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d7adb-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d7adb-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d7adb-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d7adb-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d7adb-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d7adb-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d7adb-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d7adb-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7adb-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7adb-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d7adb-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d7adb-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7adb-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7adb-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7adb-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7adb-162">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7adb-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7adb-163">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7adb-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d7adb-164">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d7adb-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d7adb-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d7adb-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="d7adb-166">Parar-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7adb-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7adb-167">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7adb-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7adb-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7adb-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7adb-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d7adb-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d7adb-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7adb-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7adb-171">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7adb-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7adb-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d7adb-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d7adb-173">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d7adb-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d7adb-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d7adb-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d7adb-175">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d7adb-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d7adb-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d7adb-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d7adb-177">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7adb-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
