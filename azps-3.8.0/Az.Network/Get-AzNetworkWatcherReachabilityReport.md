---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 0ad2b1fa6278e085a57d94f2fec9be2c6853993d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777679"
---
# <span data-ttu-id="47d95-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="47d95-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="47d95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47d95-102">SYNOPSIS</span></span>
<span data-ttu-id="47d95-103">Obtém a pontuação de latência relativa para provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="47d95-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="47d95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47d95-104">SYNTAX</span></span>

### <span data-ttu-id="47d95-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="47d95-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47d95-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="47d95-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47d95-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="47d95-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47d95-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="47d95-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47d95-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47d95-109">DESCRIPTION</span></span>
<span data-ttu-id="47d95-110">O Get-AzNetworkWatcherReachabilityReport Obtém a pontuação de latência relativa dos provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="47d95-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="47d95-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47d95-111">EXAMPLES</span></span>

### <span data-ttu-id="47d95-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47d95-112">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="47d95-113">Obtém latências relativas ao Azure Data Center no oeste dos EUA de 2017-10-10 a 2017-10-12 dentro do estado do país.</span><span class="sxs-lookup"><span data-stu-id="47d95-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="47d95-114">OS</span><span class="sxs-lookup"><span data-stu-id="47d95-114">PARAMETERS</span></span>

### <span data-ttu-id="47d95-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47d95-115">-AsJob</span></span>
<span data-ttu-id="47d95-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="47d95-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47d95-117">-Cidade</span><span class="sxs-lookup"><span data-stu-id="47d95-117">-City</span></span>
<span data-ttu-id="47d95-118">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="47d95-118">The name of the city.</span></span>

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

### <span data-ttu-id="47d95-119">-País</span><span class="sxs-lookup"><span data-stu-id="47d95-119">-Country</span></span>
<span data-ttu-id="47d95-120">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="47d95-120">The name of the country.</span></span>

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

### <span data-ttu-id="47d95-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d95-121">-DefaultProfile</span></span>
<span data-ttu-id="47d95-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47d95-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47d95-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="47d95-123">-EndTime</span></span>
<span data-ttu-id="47d95-124">A hora de término do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="47d95-124">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d95-125">-Local</span><span class="sxs-lookup"><span data-stu-id="47d95-125">-Location</span></span>
<span data-ttu-id="47d95-126">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="47d95-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d95-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47d95-127">-NetworkWatcher</span></span>
<span data-ttu-id="47d95-128">O recurso de Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="47d95-128">The network watcher resource</span></span>

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

### <span data-ttu-id="47d95-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="47d95-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="47d95-130">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="47d95-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="47d95-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="47d95-131">-NetworkWatcherName</span></span>
<span data-ttu-id="47d95-132">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="47d95-132">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d95-133">-Provedor</span><span class="sxs-lookup"><span data-stu-id="47d95-133">-Provider</span></span>
<span data-ttu-id="47d95-134">Lista de provedores de serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="47d95-134">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d95-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d95-135">-ResourceGroupName</span></span>
<span data-ttu-id="47d95-136">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="47d95-136">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d95-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47d95-137">-ResourceId</span></span>
<span data-ttu-id="47d95-138">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="47d95-138">The Id of network watcher resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47d95-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="47d95-139">-StartTime</span></span>
<span data-ttu-id="47d95-140">A hora de início do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="47d95-140">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d95-141">-Estado</span><span class="sxs-lookup"><span data-stu-id="47d95-141">-State</span></span>
<span data-ttu-id="47d95-142">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="47d95-142">The name of the state.</span></span>

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

### <span data-ttu-id="47d95-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d95-143">CommonParameters</span></span>
<span data-ttu-id="47d95-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d95-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d95-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47d95-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d95-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47d95-146">INPUTS</span></span>

### <span data-ttu-id="47d95-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47d95-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="47d95-148">System. String</span><span class="sxs-lookup"><span data-stu-id="47d95-148">System.String</span></span>

## <span data-ttu-id="47d95-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47d95-149">OUTPUTS</span></span>

### <span data-ttu-id="47d95-150">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="47d95-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="47d95-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47d95-151">NOTES</span></span>
<span data-ttu-id="47d95-152">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, acessibilidade, relatório</span><span class="sxs-lookup"><span data-stu-id="47d95-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="47d95-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47d95-153">RELATED LINKS</span></span>

[<span data-ttu-id="47d95-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47d95-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="47d95-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47d95-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="47d95-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47d95-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="47d95-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="47d95-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="47d95-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="47d95-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="47d95-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="47d95-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="47d95-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="47d95-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="47d95-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47d95-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47d95-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="47d95-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="47d95-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47d95-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47d95-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47d95-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47d95-165">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47d95-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47d95-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="47d95-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="47d95-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="47d95-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="47d95-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="47d95-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="47d95-169">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47d95-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47d95-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47d95-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47d95-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47d95-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47d95-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="47d95-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="47d95-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47d95-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47d95-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47d95-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47d95-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="47d95-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="47d95-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="47d95-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="47d95-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="47d95-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="47d95-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="47d95-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="47d95-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="47d95-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="47d95-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47d95-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)