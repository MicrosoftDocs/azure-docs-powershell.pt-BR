---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 7f974d9be1faaaf4d78a2527250cdec1775ae49f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114819"
---
# <span data-ttu-id="de87b-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="de87b-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="de87b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de87b-102">SYNOPSIS</span></span>
<span data-ttu-id="de87b-103">Cria um novo objeto de configuração de protocolo.</span><span class="sxs-lookup"><span data-stu-id="de87b-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="de87b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de87b-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de87b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de87b-105">DESCRIPTION</span></span>
<span data-ttu-id="de87b-106">O cmdlet New-AzNetworkWatcherProtocolConfiguration cria um novo objeto de configuração de protocolo.</span><span class="sxs-lookup"><span data-stu-id="de87b-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="de87b-107">Esse objeto é usado para restringir a configuração do protocolo durante uma sessão de verificação de conectividade usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="de87b-107">This object is used to restrict the protocol configuration during a connectivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="de87b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de87b-108">EXAMPLES</span></span>

### <span data-ttu-id="de87b-109">Exemplo 1: testar a conectividade do Inspetor de rede de uma VM para um site com configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="de87b-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="de87b-110">Neste exemplo, testamos a conectividade de uma VM no Azure para www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="de87b-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="de87b-111">OS</span><span class="sxs-lookup"><span data-stu-id="de87b-111">PARAMETERS</span></span>

### <span data-ttu-id="de87b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de87b-112">-DefaultProfile</span></span>
<span data-ttu-id="de87b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de87b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de87b-114">-Header</span><span class="sxs-lookup"><span data-stu-id="de87b-114">-Header</span></span>
<span data-ttu-id="de87b-115">lista de cabeçalhos HTTP</span><span class="sxs-lookup"><span data-stu-id="de87b-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de87b-116">-Método</span><span class="sxs-lookup"><span data-stu-id="de87b-116">-Method</span></span>
<span data-ttu-id="de87b-117">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="de87b-117">HTTP method</span></span>

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

### <span data-ttu-id="de87b-118">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="de87b-118">-Protocol</span></span>
<span data-ttu-id="de87b-119">Tipo de protocolo</span><span class="sxs-lookup"><span data-stu-id="de87b-119">Protocol type</span></span>

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

### <span data-ttu-id="de87b-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="de87b-120">-ValidStatusCode</span></span>
<span data-ttu-id="de87b-121">códigos de status válidos</span><span class="sxs-lookup"><span data-stu-id="de87b-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de87b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de87b-122">CommonParameters</span></span>
<span data-ttu-id="de87b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de87b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de87b-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de87b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de87b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de87b-125">INPUTS</span></span>

### <span data-ttu-id="de87b-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="de87b-126">None</span></span>

## <span data-ttu-id="de87b-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de87b-127">OUTPUTS</span></span>

### <span data-ttu-id="de87b-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="de87b-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="de87b-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de87b-129">NOTES</span></span>
<span data-ttu-id="de87b-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, pacote, captura, tráfego, filtro</span><span class="sxs-lookup"><span data-stu-id="de87b-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="de87b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de87b-131">RELATED LINKS</span></span>

[<span data-ttu-id="de87b-132">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de87b-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="de87b-133">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de87b-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="de87b-134">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de87b-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="de87b-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="de87b-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="de87b-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="de87b-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="de87b-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="de87b-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="de87b-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="de87b-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="de87b-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de87b-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="de87b-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="de87b-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="de87b-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de87b-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="de87b-142">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de87b-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="de87b-143">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de87b-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="de87b-144">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="de87b-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="de87b-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="de87b-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="de87b-146">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="de87b-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="de87b-147">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de87b-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de87b-148">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de87b-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de87b-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de87b-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de87b-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="de87b-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="de87b-151">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de87b-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de87b-152">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de87b-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de87b-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="de87b-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="de87b-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="de87b-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="de87b-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="de87b-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="de87b-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="de87b-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="de87b-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="de87b-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="de87b-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de87b-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
