---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111071"
---
# <span data-ttu-id="e21c2-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e21c2-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="e21c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e21c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e21c2-103">Obtém a pontuação de latência relativa para provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="e21c2-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="e21c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e21c2-104">SYNTAX</span></span>

### <span data-ttu-id="e21c2-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e21c2-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e21c2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e21c2-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e21c2-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e21c2-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e21c2-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e21c2-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e21c2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e21c2-109">DESCRIPTION</span></span>
<span data-ttu-id="e21c2-110">O Get-AzNetworkWatcherReachabilityReport Obtém a pontuação de latência relativa dos provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="e21c2-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="e21c2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e21c2-111">EXAMPLES</span></span>

### <span data-ttu-id="e21c2-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e21c2-112">Example 1</span></span>
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

<span data-ttu-id="e21c2-113">Obtém latências relativas ao Azure Data Center no oeste dos EUA de 2017-10-10 a 2017-10-12 dentro do estado do país.</span><span class="sxs-lookup"><span data-stu-id="e21c2-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="e21c2-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e21c2-114">Example 2</span></span>

<span data-ttu-id="e21c2-115">Obtém a pontuação de latência relativa para provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="e21c2-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="e21c2-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e21c2-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="e21c2-117">OS</span><span class="sxs-lookup"><span data-stu-id="e21c2-117">PARAMETERS</span></span>

### <span data-ttu-id="e21c2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e21c2-118">-AsJob</span></span>
<span data-ttu-id="e21c2-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e21c2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e21c2-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="e21c2-120">-City</span></span>
<span data-ttu-id="e21c2-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="e21c2-121">The name of the city.</span></span>

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

### <span data-ttu-id="e21c2-122">-País</span><span class="sxs-lookup"><span data-stu-id="e21c2-122">-Country</span></span>
<span data-ttu-id="e21c2-123">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="e21c2-123">The name of the country.</span></span>

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

### <span data-ttu-id="e21c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21c2-124">-DefaultProfile</span></span>
<span data-ttu-id="e21c2-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e21c2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e21c2-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e21c2-126">-EndTime</span></span>
<span data-ttu-id="e21c2-127">A hora de término do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="e21c2-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="e21c2-128">-Local</span><span class="sxs-lookup"><span data-stu-id="e21c2-128">-Location</span></span>
<span data-ttu-id="e21c2-129">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="e21c2-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="e21c2-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e21c2-130">-NetworkWatcher</span></span>
<span data-ttu-id="e21c2-131">O recurso de Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="e21c2-131">The network watcher resource</span></span>

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

### <span data-ttu-id="e21c2-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="e21c2-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="e21c2-133">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e21c2-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e21c2-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e21c2-134">-NetworkWatcherName</span></span>
<span data-ttu-id="e21c2-135">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e21c2-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="e21c2-136">-Provedor</span><span class="sxs-lookup"><span data-stu-id="e21c2-136">-Provider</span></span>
<span data-ttu-id="e21c2-137">Lista de provedores de serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="e21c2-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="e21c2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21c2-138">-ResourceGroupName</span></span>
<span data-ttu-id="e21c2-139">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e21c2-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e21c2-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e21c2-140">-ResourceId</span></span>
<span data-ttu-id="e21c2-141">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="e21c2-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="e21c2-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e21c2-142">-StartTime</span></span>
<span data-ttu-id="e21c2-143">A hora de início do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="e21c2-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="e21c2-144">-Estado</span><span class="sxs-lookup"><span data-stu-id="e21c2-144">-State</span></span>
<span data-ttu-id="e21c2-145">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="e21c2-145">The name of the state.</span></span>

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

### <span data-ttu-id="e21c2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21c2-146">CommonParameters</span></span>
<span data-ttu-id="e21c2-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e21c2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21c2-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e21c2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21c2-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e21c2-149">INPUTS</span></span>

### <span data-ttu-id="e21c2-150">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e21c2-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e21c2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e21c2-151">System.String</span></span>

## <span data-ttu-id="e21c2-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e21c2-152">OUTPUTS</span></span>

### <span data-ttu-id="e21c2-153">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e21c2-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="e21c2-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e21c2-154">NOTES</span></span>
<span data-ttu-id="e21c2-155">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, acessibilidade, relatório</span><span class="sxs-lookup"><span data-stu-id="e21c2-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="e21c2-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e21c2-156">RELATED LINKS</span></span>

[<span data-ttu-id="e21c2-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e21c2-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e21c2-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e21c2-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e21c2-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e21c2-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e21c2-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e21c2-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e21c2-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e21c2-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e21c2-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e21c2-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e21c2-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e21c2-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e21c2-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e21c2-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e21c2-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e21c2-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e21c2-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e21c2-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e21c2-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e21c2-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e21c2-168">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e21c2-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e21c2-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e21c2-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e21c2-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e21c2-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e21c2-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e21c2-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e21c2-172">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e21c2-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e21c2-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e21c2-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e21c2-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e21c2-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e21c2-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e21c2-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e21c2-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e21c2-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e21c2-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e21c2-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e21c2-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e21c2-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e21c2-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e21c2-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e21c2-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e21c2-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e21c2-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e21c2-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e21c2-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e21c2-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e21c2-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e21c2-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
