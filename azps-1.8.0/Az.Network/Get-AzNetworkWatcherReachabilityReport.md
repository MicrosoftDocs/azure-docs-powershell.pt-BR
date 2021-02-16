---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 1c06b6605cfa7d4b7d402dec2fcb0e33136b125c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400273"
---
# <span data-ttu-id="640db-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="640db-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="640db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="640db-102">SYNOPSIS</span></span>
<span data-ttu-id="640db-103">Obtém a pontuação de latência relativa para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="640db-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="640db-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="640db-104">SYNTAX</span></span>

### <span data-ttu-id="640db-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="640db-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="640db-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="640db-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="640db-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="640db-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="640db-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="640db-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="640db-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="640db-109">DESCRIPTION</span></span>
<span data-ttu-id="640db-110">A Get-AzNetworkWatcherReachabilityReport obtém a pontuação de latência relativa para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="640db-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="640db-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="640db-111">EXAMPLES</span></span>

### <span data-ttu-id="640db-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="640db-112">Example 1</span></span>
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

<span data-ttu-id="640db-113">Obtém latências relativas ao Data Center do Azure no oeste dos EUA de 2017-10-10 a 2017-10-12 no Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="640db-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="640db-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="640db-114">PARAMETERS</span></span>

### <span data-ttu-id="640db-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="640db-115">-AsJob</span></span>
<span data-ttu-id="640db-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="640db-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="640db-117">-Cidade</span><span class="sxs-lookup"><span data-stu-id="640db-117">-City</span></span>
<span data-ttu-id="640db-118">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="640db-118">The name of the city.</span></span>

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

### <span data-ttu-id="640db-119">-País/Região</span><span class="sxs-lookup"><span data-stu-id="640db-119">-Country</span></span>
<span data-ttu-id="640db-120">O nome do país/região.</span><span class="sxs-lookup"><span data-stu-id="640db-120">The name of the country.</span></span>

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

### <span data-ttu-id="640db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640db-121">-DefaultProfile</span></span>
<span data-ttu-id="640db-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="640db-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="640db-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="640db-123">-EndTime</span></span>
<span data-ttu-id="640db-124">A hora de término do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="640db-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="640db-125">-Local</span><span class="sxs-lookup"><span data-stu-id="640db-125">-Location</span></span>
<span data-ttu-id="640db-126">Regiões opcionais do Azure para escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="640db-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="640db-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="640db-127">-NetworkWatcher</span></span>
<span data-ttu-id="640db-128">O recurso de watcher de rede</span><span class="sxs-lookup"><span data-stu-id="640db-128">The network watcher resource</span></span>

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

### <span data-ttu-id="640db-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="640db-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="640db-130">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="640db-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="640db-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="640db-131">-NetworkWatcherName</span></span>
<span data-ttu-id="640db-132">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="640db-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="640db-133">-Provedor</span><span class="sxs-lookup"><span data-stu-id="640db-133">-Provider</span></span>
<span data-ttu-id="640db-134">Lista de provedores de serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="640db-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="640db-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640db-135">-ResourceGroupName</span></span>
<span data-ttu-id="640db-136">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="640db-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="640db-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="640db-137">-ResourceId</span></span>
<span data-ttu-id="640db-138">A ID do recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="640db-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="640db-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="640db-139">-StartTime</span></span>
<span data-ttu-id="640db-140">A hora de início do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="640db-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="640db-141">-Estado</span><span class="sxs-lookup"><span data-stu-id="640db-141">-State</span></span>
<span data-ttu-id="640db-142">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="640db-142">The name of the state.</span></span>

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

### <span data-ttu-id="640db-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640db-143">CommonParameters</span></span>
<span data-ttu-id="640db-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640db-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640db-145">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="640db-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640db-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="640db-146">INPUTS</span></span>

### <span data-ttu-id="640db-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="640db-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="640db-148">System.String</span><span class="sxs-lookup"><span data-stu-id="640db-148">System.String</span></span>

## <span data-ttu-id="640db-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="640db-149">OUTPUTS</span></span>

### <span data-ttu-id="640db-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="640db-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="640db-151">Notas</span><span class="sxs-lookup"><span data-stu-id="640db-151">NOTES</span></span>
<span data-ttu-id="640db-152">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="640db-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="640db-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="640db-153">RELATED LINKS</span></span>

[<span data-ttu-id="640db-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="640db-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="640db-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="640db-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="640db-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="640db-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="640db-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="640db-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="640db-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="640db-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="640db-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="640db-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="640db-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="640db-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="640db-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="640db-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="640db-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="640db-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="640db-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="640db-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="640db-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="640db-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="640db-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="640db-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="640db-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="640db-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="640db-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="640db-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="640db-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="640db-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="640db-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="640db-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="640db-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="640db-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="640db-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="640db-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="640db-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="640db-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="640db-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="640db-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="640db-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="640db-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="640db-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="640db-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="640db-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="640db-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="640db-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="640db-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="640db-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="640db-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="640db-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="640db-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="640db-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="640db-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
