---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: f29ab593ffac847ec6b089efdc39bc594ad1d785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412360"
---
# <span data-ttu-id="3969b-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3969b-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="3969b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3969b-102">SYNOPSIS</span></span>
<span data-ttu-id="3969b-103">Obtém a pontuação de latência relativa para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="3969b-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="3969b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3969b-104">SYNTAX</span></span>

### <span data-ttu-id="3969b-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3969b-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3969b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3969b-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3969b-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3969b-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3969b-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3969b-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3969b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3969b-109">DESCRIPTION</span></span>
<span data-ttu-id="3969b-110">A Get-AzNetworkWatcherReachabilityReport obtém a pontuação de latência relativa para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="3969b-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="3969b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3969b-111">EXAMPLES</span></span>

### <span data-ttu-id="3969b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3969b-112">Example 1</span></span>
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

<span data-ttu-id="3969b-113">Obtém latências relativas ao Data Center do Azure no oeste dos EUA de 2017-10-10 a 2017-10-12 no Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="3969b-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="3969b-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3969b-114">Example 2</span></span>

<span data-ttu-id="3969b-115">Obtém a pontuação de latência relativa para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="3969b-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="3969b-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="3969b-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="3969b-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3969b-117">PARAMETERS</span></span>

### <span data-ttu-id="3969b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3969b-118">-AsJob</span></span>
<span data-ttu-id="3969b-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3969b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3969b-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="3969b-120">-City</span></span>
<span data-ttu-id="3969b-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="3969b-121">The name of the city.</span></span>

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

### <span data-ttu-id="3969b-122">-País/Região</span><span class="sxs-lookup"><span data-stu-id="3969b-122">-Country</span></span>
<span data-ttu-id="3969b-123">O nome do país/região.</span><span class="sxs-lookup"><span data-stu-id="3969b-123">The name of the country.</span></span>

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

### <span data-ttu-id="3969b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3969b-124">-DefaultProfile</span></span>
<span data-ttu-id="3969b-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3969b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3969b-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3969b-126">-EndTime</span></span>
<span data-ttu-id="3969b-127">A hora de término do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="3969b-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="3969b-128">-Local</span><span class="sxs-lookup"><span data-stu-id="3969b-128">-Location</span></span>
<span data-ttu-id="3969b-129">Regiões opcionais do Azure para escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="3969b-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="3969b-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3969b-130">-NetworkWatcher</span></span>
<span data-ttu-id="3969b-131">O recurso de watcher de rede</span><span class="sxs-lookup"><span data-stu-id="3969b-131">The network watcher resource</span></span>

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

### <span data-ttu-id="3969b-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="3969b-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="3969b-133">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="3969b-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3969b-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3969b-134">-NetworkWatcherName</span></span>
<span data-ttu-id="3969b-135">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="3969b-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="3969b-136">-Provedor</span><span class="sxs-lookup"><span data-stu-id="3969b-136">-Provider</span></span>
<span data-ttu-id="3969b-137">Lista de provedores de serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="3969b-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="3969b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3969b-138">-ResourceGroupName</span></span>
<span data-ttu-id="3969b-139">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="3969b-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3969b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3969b-140">-ResourceId</span></span>
<span data-ttu-id="3969b-141">A ID do recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="3969b-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="3969b-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3969b-142">-StartTime</span></span>
<span data-ttu-id="3969b-143">A hora de início do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="3969b-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="3969b-144">-Estado</span><span class="sxs-lookup"><span data-stu-id="3969b-144">-State</span></span>
<span data-ttu-id="3969b-145">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="3969b-145">The name of the state.</span></span>

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

### <span data-ttu-id="3969b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3969b-146">CommonParameters</span></span>
<span data-ttu-id="3969b-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3969b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3969b-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3969b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3969b-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="3969b-149">INPUTS</span></span>

### <span data-ttu-id="3969b-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3969b-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3969b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="3969b-151">System.String</span></span>

## <span data-ttu-id="3969b-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="3969b-152">OUTPUTS</span></span>

### <span data-ttu-id="3969b-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3969b-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="3969b-154">Notas</span><span class="sxs-lookup"><span data-stu-id="3969b-154">NOTES</span></span>
<span data-ttu-id="3969b-155">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="3969b-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="3969b-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3969b-156">RELATED LINKS</span></span>

[<span data-ttu-id="3969b-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3969b-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3969b-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3969b-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3969b-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3969b-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3969b-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3969b-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3969b-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3969b-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3969b-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3969b-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3969b-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3969b-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3969b-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3969b-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3969b-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3969b-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3969b-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3969b-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3969b-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3969b-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3969b-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3969b-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3969b-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3969b-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3969b-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3969b-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3969b-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3969b-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3969b-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3969b-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3969b-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3969b-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3969b-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3969b-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3969b-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3969b-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3969b-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3969b-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3969b-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3969b-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3969b-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3969b-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3969b-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3969b-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3969b-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3969b-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3969b-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3969b-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3969b-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3969b-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3969b-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3969b-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
