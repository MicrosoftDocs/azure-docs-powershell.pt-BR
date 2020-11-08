---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118344"
---
# <span data-ttu-id="b8180-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b8180-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="b8180-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8180-102">SYNOPSIS</span></span>
<span data-ttu-id="b8180-103">Obtém a pontuação de latência relativa para provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8180-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="b8180-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8180-104">SYNTAX</span></span>

### <span data-ttu-id="b8180-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8180-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8180-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b8180-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8180-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8180-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8180-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b8180-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8180-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8180-109">DESCRIPTION</span></span>
<span data-ttu-id="b8180-110">O Get-AzNetworkWatcherReachabilityReport Obtém a pontuação de latência relativa dos provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8180-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="b8180-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8180-111">EXAMPLES</span></span>

### <span data-ttu-id="b8180-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8180-112">Example 1</span></span>
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

<span data-ttu-id="b8180-113">Obtém latências relativas ao Azure Data Center no oeste dos EUA de 2017-10-10 a 2017-10-12 dentro do estado do país.</span><span class="sxs-lookup"><span data-stu-id="b8180-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="b8180-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b8180-114">Example 2</span></span>

<span data-ttu-id="b8180-115">Obtém a pontuação de latência relativa para provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8180-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="b8180-116">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="b8180-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="b8180-117">OS</span><span class="sxs-lookup"><span data-stu-id="b8180-117">PARAMETERS</span></span>

### <span data-ttu-id="b8180-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8180-118">-AsJob</span></span>
<span data-ttu-id="b8180-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b8180-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8180-120">-Cidade</span><span class="sxs-lookup"><span data-stu-id="b8180-120">-City</span></span>
<span data-ttu-id="b8180-121">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="b8180-121">The name of the city.</span></span>

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

### <span data-ttu-id="b8180-122">-País</span><span class="sxs-lookup"><span data-stu-id="b8180-122">-Country</span></span>
<span data-ttu-id="b8180-123">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="b8180-123">The name of the country.</span></span>

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

### <span data-ttu-id="b8180-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8180-124">-DefaultProfile</span></span>
<span data-ttu-id="b8180-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8180-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8180-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b8180-126">-EndTime</span></span>
<span data-ttu-id="b8180-127">A hora de término do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8180-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="b8180-128">-Local</span><span class="sxs-lookup"><span data-stu-id="b8180-128">-Location</span></span>
<span data-ttu-id="b8180-129">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="b8180-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="b8180-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8180-130">-NetworkWatcher</span></span>
<span data-ttu-id="b8180-131">O recurso de Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="b8180-131">The network watcher resource</span></span>

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

### <span data-ttu-id="b8180-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="b8180-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="b8180-133">Localização do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b8180-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b8180-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b8180-134">-NetworkWatcherName</span></span>
<span data-ttu-id="b8180-135">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b8180-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="b8180-136">-Provedor</span><span class="sxs-lookup"><span data-stu-id="b8180-136">-Provider</span></span>
<span data-ttu-id="b8180-137">Lista de provedores de serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="b8180-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="b8180-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8180-138">-ResourceGroupName</span></span>
<span data-ttu-id="b8180-139">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b8180-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b8180-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8180-140">-ResourceId</span></span>
<span data-ttu-id="b8180-141">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="b8180-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="b8180-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b8180-142">-StartTime</span></span>
<span data-ttu-id="b8180-143">A hora de início do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8180-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="b8180-144">-Estado</span><span class="sxs-lookup"><span data-stu-id="b8180-144">-State</span></span>
<span data-ttu-id="b8180-145">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="b8180-145">The name of the state.</span></span>

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

### <span data-ttu-id="b8180-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8180-146">CommonParameters</span></span>
<span data-ttu-id="b8180-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8180-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8180-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8180-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8180-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8180-149">INPUTS</span></span>

### <span data-ttu-id="b8180-150">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8180-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b8180-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b8180-151">System.String</span></span>

## <span data-ttu-id="b8180-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8180-152">OUTPUTS</span></span>

### <span data-ttu-id="b8180-153">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b8180-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="b8180-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8180-154">NOTES</span></span>
<span data-ttu-id="b8180-155">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, acessibilidade, relatório</span><span class="sxs-lookup"><span data-stu-id="b8180-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="b8180-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8180-156">RELATED LINKS</span></span>

[<span data-ttu-id="b8180-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8180-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b8180-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8180-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b8180-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8180-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b8180-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b8180-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b8180-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b8180-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b8180-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b8180-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b8180-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b8180-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b8180-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8180-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8180-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b8180-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b8180-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8180-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8180-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8180-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8180-168">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8180-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8180-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8180-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b8180-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b8180-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b8180-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b8180-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b8180-172">Parar-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8180-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8180-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8180-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8180-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8180-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8180-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b8180-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b8180-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8180-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8180-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8180-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8180-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b8180-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b8180-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b8180-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b8180-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b8180-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b8180-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b8180-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b8180-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b8180-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b8180-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8180-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
