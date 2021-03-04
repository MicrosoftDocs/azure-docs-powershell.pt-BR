---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 72aa9748cddee0a8ff894463e569d15a2fa01ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885683"
---
# <span data-ttu-id="47212-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="47212-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="47212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47212-102">SYNOPSIS</span></span>
<span data-ttu-id="47212-103">Obtém a pontuação relativa de latência para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="47212-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="47212-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="47212-104">SYNTAX</span></span>

### <span data-ttu-id="47212-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47212-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47212-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="47212-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47212-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="47212-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47212-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="47212-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47212-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47212-109">DESCRIPTION</span></span>
<span data-ttu-id="47212-110">O Get-AzNetworkWatcherReachabilityReport obtém a pontuação relativa de latência para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="47212-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="47212-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47212-111">EXAMPLES</span></span>

### <span data-ttu-id="47212-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47212-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="47212-113">Obtém latências relativas ao Azure Data Center no Oeste dos EUA de 2017-10-10 a 2017-10-12 no Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="47212-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="47212-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47212-114">Example 2</span></span>

<span data-ttu-id="47212-115">Obtém a pontuação relativa de latência para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="47212-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="47212-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="47212-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="47212-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="47212-117">PARAMETERS</span></span>

### <span data-ttu-id="47212-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47212-118">-AsJob</span></span>
<span data-ttu-id="47212-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="47212-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47212-120">-City</span><span class="sxs-lookup"><span data-stu-id="47212-120">-City</span></span>
<span data-ttu-id="47212-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="47212-121">The name of the city.</span></span>

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

### <span data-ttu-id="47212-122">-Country</span><span class="sxs-lookup"><span data-stu-id="47212-122">-Country</span></span>
<span data-ttu-id="47212-123">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="47212-123">The name of the country.</span></span>

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

### <span data-ttu-id="47212-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47212-124">-DefaultProfile</span></span>
<span data-ttu-id="47212-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="47212-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47212-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="47212-126">-EndTime</span></span>
<span data-ttu-id="47212-127">A hora de término do relatório de capacidade de acesso do Azure.</span><span class="sxs-lookup"><span data-stu-id="47212-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="47212-128">-Location</span><span class="sxs-lookup"><span data-stu-id="47212-128">-Location</span></span>
<span data-ttu-id="47212-129">Regiões opcionais do Azure para escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="47212-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="47212-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47212-130">-NetworkWatcher</span></span>
<span data-ttu-id="47212-131">O recurso do watcher de rede</span><span class="sxs-lookup"><span data-stu-id="47212-131">The network watcher resource</span></span>

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

### <span data-ttu-id="47212-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="47212-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="47212-133">Local do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="47212-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="47212-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="47212-134">-NetworkWatcherName</span></span>
<span data-ttu-id="47212-135">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="47212-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="47212-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="47212-136">-Provider</span></span>
<span data-ttu-id="47212-137">Lista de provedores de serviços da Internet.</span><span class="sxs-lookup"><span data-stu-id="47212-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="47212-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47212-138">-ResourceGroupName</span></span>
<span data-ttu-id="47212-139">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="47212-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="47212-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47212-140">-ResourceId</span></span>
<span data-ttu-id="47212-141">A ID do recurso do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="47212-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="47212-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="47212-142">-StartTime</span></span>
<span data-ttu-id="47212-143">A hora de início do relatório de capacidade de acesso do Azure.</span><span class="sxs-lookup"><span data-stu-id="47212-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="47212-144">-State</span><span class="sxs-lookup"><span data-stu-id="47212-144">-State</span></span>
<span data-ttu-id="47212-145">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="47212-145">The name of the state.</span></span>

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

### <span data-ttu-id="47212-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47212-146">CommonParameters</span></span>
<span data-ttu-id="47212-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47212-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47212-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47212-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47212-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47212-149">INPUTS</span></span>

### <span data-ttu-id="47212-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47212-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="47212-151">System.String</span><span class="sxs-lookup"><span data-stu-id="47212-151">System.String</span></span>

## <span data-ttu-id="47212-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="47212-152">OUTPUTS</span></span>

### <span data-ttu-id="47212-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="47212-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="47212-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="47212-154">NOTES</span></span>
<span data-ttu-id="47212-155">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="47212-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="47212-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47212-156">RELATED LINKS</span></span>

[<span data-ttu-id="47212-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47212-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="47212-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47212-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="47212-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47212-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="47212-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="47212-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="47212-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="47212-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="47212-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="47212-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="47212-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="47212-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="47212-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47212-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47212-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="47212-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="47212-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47212-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47212-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47212-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47212-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47212-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47212-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="47212-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="47212-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="47212-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="47212-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="47212-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="47212-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47212-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47212-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47212-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47212-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47212-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47212-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="47212-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="47212-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47212-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47212-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47212-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47212-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="47212-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="47212-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="47212-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="47212-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="47212-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="47212-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="47212-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="47212-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="47212-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="47212-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47212-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
