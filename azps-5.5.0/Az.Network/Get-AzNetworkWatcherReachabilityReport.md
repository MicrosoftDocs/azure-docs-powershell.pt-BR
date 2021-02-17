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
ms.locfileid: "100412836"
---
# <span data-ttu-id="1b000-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1b000-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="1b000-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b000-102">SYNOPSIS</span></span>
<span data-ttu-id="1b000-103">Obtém a pontuação de latência relativa para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b000-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="1b000-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b000-104">SYNTAX</span></span>

### <span data-ttu-id="1b000-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1b000-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b000-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1b000-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b000-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b000-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b000-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1b000-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b000-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b000-109">DESCRIPTION</span></span>
<span data-ttu-id="1b000-110">A Get-AzNetworkWatcherReachabilityReport obtém a pontuação de latência relativa para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b000-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="1b000-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1b000-111">EXAMPLES</span></span>

### <span data-ttu-id="1b000-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b000-112">Example 1</span></span>
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

<span data-ttu-id="1b000-113">Obtém latências relativas ao Data Center do Azure no oeste dos EUA de 2017-10-10 a 2017-10-12 no Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="1b000-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="1b000-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1b000-114">Example 2</span></span>

<span data-ttu-id="1b000-115">Obtém a pontuação de latência relativa para provedores de serviços de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b000-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="1b000-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="1b000-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="1b000-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b000-117">PARAMETERS</span></span>

### <span data-ttu-id="1b000-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b000-118">-AsJob</span></span>
<span data-ttu-id="1b000-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1b000-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b000-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="1b000-120">-City</span></span>
<span data-ttu-id="1b000-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="1b000-121">The name of the city.</span></span>

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

### <span data-ttu-id="1b000-122">-País/Região</span><span class="sxs-lookup"><span data-stu-id="1b000-122">-Country</span></span>
<span data-ttu-id="1b000-123">O nome do país/região.</span><span class="sxs-lookup"><span data-stu-id="1b000-123">The name of the country.</span></span>

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

### <span data-ttu-id="1b000-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b000-124">-DefaultProfile</span></span>
<span data-ttu-id="1b000-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1b000-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b000-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1b000-126">-EndTime</span></span>
<span data-ttu-id="1b000-127">A hora de término do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b000-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="1b000-128">-Local</span><span class="sxs-lookup"><span data-stu-id="1b000-128">-Location</span></span>
<span data-ttu-id="1b000-129">Regiões opcionais do Azure para escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="1b000-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="1b000-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b000-130">-NetworkWatcher</span></span>
<span data-ttu-id="1b000-131">O recurso de watcher de rede</span><span class="sxs-lookup"><span data-stu-id="1b000-131">The network watcher resource</span></span>

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

### <span data-ttu-id="1b000-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="1b000-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="1b000-133">Localização do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="1b000-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1b000-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1b000-134">-NetworkWatcherName</span></span>
<span data-ttu-id="1b000-135">O nome do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="1b000-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="1b000-136">-Provedor</span><span class="sxs-lookup"><span data-stu-id="1b000-136">-Provider</span></span>
<span data-ttu-id="1b000-137">Lista de provedores de serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="1b000-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="1b000-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b000-138">-ResourceGroupName</span></span>
<span data-ttu-id="1b000-139">O nome do grupo de recursos do watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="1b000-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1b000-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b000-140">-ResourceId</span></span>
<span data-ttu-id="1b000-141">A ID do recurso de watcher de rede.</span><span class="sxs-lookup"><span data-stu-id="1b000-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="1b000-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1b000-142">-StartTime</span></span>
<span data-ttu-id="1b000-143">A hora de início do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b000-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="1b000-144">-Estado</span><span class="sxs-lookup"><span data-stu-id="1b000-144">-State</span></span>
<span data-ttu-id="1b000-145">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="1b000-145">The name of the state.</span></span>

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

### <span data-ttu-id="1b000-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b000-146">CommonParameters</span></span>
<span data-ttu-id="1b000-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b000-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b000-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b000-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b000-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="1b000-149">INPUTS</span></span>

### <span data-ttu-id="1b000-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b000-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1b000-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1b000-151">System.String</span></span>

## <span data-ttu-id="1b000-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="1b000-152">OUTPUTS</span></span>

### <span data-ttu-id="1b000-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1b000-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="1b000-154">Notas</span><span class="sxs-lookup"><span data-stu-id="1b000-154">NOTES</span></span>
<span data-ttu-id="1b000-155">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="1b000-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="1b000-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b000-156">RELATED LINKS</span></span>

[<span data-ttu-id="1b000-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b000-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1b000-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b000-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1b000-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b000-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1b000-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1b000-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1b000-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1b000-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1b000-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1b000-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1b000-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1b000-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1b000-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b000-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b000-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1b000-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1b000-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b000-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b000-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b000-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b000-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b000-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b000-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b000-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1b000-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1b000-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1b000-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1b000-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1b000-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b000-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b000-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b000-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b000-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b000-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b000-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1b000-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1b000-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b000-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b000-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b000-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b000-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1b000-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1b000-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1b000-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1b000-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1b000-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1b000-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1b000-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1b000-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1b000-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1b000-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b000-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
