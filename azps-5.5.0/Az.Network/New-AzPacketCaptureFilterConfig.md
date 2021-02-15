---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 194e3c71cc763aeb74091f912b37dd15e4dfe4aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112822"
---
# <span data-ttu-id="0779d-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0779d-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="0779d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0779d-102">SYNOPSIS</span></span>
<span data-ttu-id="0779d-103">Cria um novo objeto de filtro de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="0779d-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="0779d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0779d-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0779d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0779d-105">DESCRIPTION</span></span>
<span data-ttu-id="0779d-106">O New-AzPacketCaptureFilterConfig cmdlet cria um novo objeto de filtro de captura de pacote.</span><span class="sxs-lookup"><span data-stu-id="0779d-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="0779d-107">Esse objeto é usado para restringir o tipo de pacotes capturados durante uma sessão de captura de pacote usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="0779d-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="0779d-108">O New-AzNetworkWatcherPacketCapture cmdlet pode aceitar vários objetos de filtro para habilitar sessões de captura composíveis.</span><span class="sxs-lookup"><span data-stu-id="0779d-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="0779d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0779d-109">EXAMPLES</span></span>

### <span data-ttu-id="0779d-110">Exemplo 1: Criar uma Captura de Pacote com vários filtros</span><span class="sxs-lookup"><span data-stu-id="0779d-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="0779d-111">Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo.</span><span class="sxs-lookup"><span data-stu-id="0779d-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="0779d-112">Quando a sessão for concluída, ela será salva na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="0779d-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="0779d-113">Observação: a extensão do Azure Network Watcher deve ser instalada na máquina virtual de destino para criar capturas de pacotes.</span><span class="sxs-lookup"><span data-stu-id="0779d-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="0779d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0779d-114">PARAMETERS</span></span>

### <span data-ttu-id="0779d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0779d-115">-DefaultProfile</span></span>
<span data-ttu-id="0779d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0779d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0779d-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="0779d-117">-LocalIPAddress</span></span>
<span data-ttu-id="0779d-118">Especifica o Endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="0779d-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="0779d-119">Exemplo de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="0779d-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="0779d-120">"127.0.0.1-127.0.0.255" para intervalo.</span><span class="sxs-lookup"><span data-stu-id="0779d-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="0779d-121">"127.0.0.1;127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="0779d-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="0779d-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="0779d-122">-LocalPort</span></span>
<span data-ttu-id="0779d-123">Especifica o Endereço IP local para filtrar.</span><span class="sxs-lookup"><span data-stu-id="0779d-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="0779d-124">Exemplo de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="0779d-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="0779d-125">"127.0.0.1-127.0.0.255" para intervalo.</span><span class="sxs-lookup"><span data-stu-id="0779d-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="0779d-126">"127.0.0.1;127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="0779d-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="0779d-127">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="0779d-127">-Protocol</span></span>
<span data-ttu-id="0779d-128">Especifica o Protocolo para filtrar.</span><span class="sxs-lookup"><span data-stu-id="0779d-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="0779d-129">Valores aceitáveis "TCP","UDP","Qualquer"</span><span class="sxs-lookup"><span data-stu-id="0779d-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="0779d-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="0779d-130">-RemoteIPAddress</span></span>
<span data-ttu-id="0779d-131">Especifica o endereço IP remoto para filtrar.</span><span class="sxs-lookup"><span data-stu-id="0779d-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="0779d-132">Exemplo de entradas: "127.0.0.1" para entrada de endereço único.</span><span class="sxs-lookup"><span data-stu-id="0779d-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="0779d-133">"127.0.0.1-127.0.0.255" para intervalo.</span><span class="sxs-lookup"><span data-stu-id="0779d-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="0779d-134">"127.0.0.1;127.0.0.5;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="0779d-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="0779d-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="0779d-135">-RemotePort</span></span>
<span data-ttu-id="0779d-136">Especifica a Porta Remota para filtrar.</span><span class="sxs-lookup"><span data-stu-id="0779d-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="0779d-137">Entrada de exemplo de porta remota: "80" para entrada de porta única.</span><span class="sxs-lookup"><span data-stu-id="0779d-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="0779d-138">"80-85" para intervalo.</span><span class="sxs-lookup"><span data-stu-id="0779d-138">"80-85" for range.</span></span>
<span data-ttu-id="0779d-139">"80;443;" para várias entradas.</span><span class="sxs-lookup"><span data-stu-id="0779d-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="0779d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0779d-140">CommonParameters</span></span>
<span data-ttu-id="0779d-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0779d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0779d-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0779d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0779d-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="0779d-143">INPUTS</span></span>

### <span data-ttu-id="0779d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0779d-144">System.String</span></span>

## <span data-ttu-id="0779d-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="0779d-145">OUTPUTS</span></span>

### <span data-ttu-id="0779d-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="0779d-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="0779d-147">Notas</span><span class="sxs-lookup"><span data-stu-id="0779d-147">NOTES</span></span>
<span data-ttu-id="0779d-148">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span><span class="sxs-lookup"><span data-stu-id="0779d-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="0779d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0779d-149">RELATED LINKS</span></span>

[<span data-ttu-id="0779d-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0779d-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0779d-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0779d-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0779d-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0779d-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0779d-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0779d-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0779d-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0779d-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0779d-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0779d-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0779d-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0779d-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0779d-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0779d-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0779d-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0779d-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0779d-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0779d-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0779d-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0779d-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0779d-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0779d-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0779d-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0779d-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0779d-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0779d-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0779d-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0779d-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0779d-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0779d-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0779d-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0779d-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0779d-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0779d-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0779d-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0779d-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0779d-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0779d-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0779d-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0779d-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0779d-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0779d-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0779d-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0779d-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0779d-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0779d-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0779d-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0779d-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0779d-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0779d-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0779d-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0779d-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
