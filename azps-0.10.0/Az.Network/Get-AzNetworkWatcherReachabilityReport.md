---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775503"
---
# <span data-ttu-id="929fb-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="929fb-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="929fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="929fb-102">SYNOPSIS</span></span>
<span data-ttu-id="929fb-103">Obtém a pontuação de latência relativa para provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="929fb-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="929fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="929fb-104">SYNTAX</span></span>

### <span data-ttu-id="929fb-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="929fb-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="929fb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="929fb-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="929fb-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="929fb-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="929fb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="929fb-108">DESCRIPTION</span></span>
<span data-ttu-id="929fb-109">O Get-AzNetworkWatcherReachabilityReport Obtém a pontuação de latência relativa dos provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="929fb-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="929fb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="929fb-110">EXAMPLES</span></span>

### <span data-ttu-id="929fb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="929fb-111">Example 1</span></span>
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

<span data-ttu-id="929fb-112">Obtém latências relativas ao Azure Data Center no oeste dos EUA de 2017-10-10 a 2017-10-12 dentro do estado do país.</span><span class="sxs-lookup"><span data-stu-id="929fb-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="929fb-113">OS</span><span class="sxs-lookup"><span data-stu-id="929fb-113">PARAMETERS</span></span>

### <span data-ttu-id="929fb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="929fb-114">-AsJob</span></span>
<span data-ttu-id="929fb-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="929fb-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-116">-Cidade</span><span class="sxs-lookup"><span data-stu-id="929fb-116">-City</span></span>
<span data-ttu-id="929fb-117">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="929fb-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-118">-País</span><span class="sxs-lookup"><span data-stu-id="929fb-118">-Country</span></span>
<span data-ttu-id="929fb-119">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="929fb-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929fb-120">-DefaultProfile</span></span>
<span data-ttu-id="929fb-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="929fb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="929fb-122">-EndTime</span></span>
<span data-ttu-id="929fb-123">A hora de término do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="929fb-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-124">-Local</span><span class="sxs-lookup"><span data-stu-id="929fb-124">-Location</span></span>
<span data-ttu-id="929fb-125">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="929fb-125">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="929fb-126">-NetworkWatcher</span></span>
<span data-ttu-id="929fb-127">O recurso de Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="929fb-127">The network watcher resource</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="929fb-128">-NetworkWatcherName</span></span>
<span data-ttu-id="929fb-129">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="929fb-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-130">-Provedor</span><span class="sxs-lookup"><span data-stu-id="929fb-130">-Provider</span></span>
<span data-ttu-id="929fb-131">Lista de provedores de serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="929fb-131">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="929fb-132">-ResourceGroupName</span></span>
<span data-ttu-id="929fb-133">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="929fb-133">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="929fb-134">-ResourceId</span></span>
<span data-ttu-id="929fb-135">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="929fb-135">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="929fb-136">-StartTime</span></span>
<span data-ttu-id="929fb-137">A hora de início do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="929fb-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-138">-Estado</span><span class="sxs-lookup"><span data-stu-id="929fb-138">-State</span></span>
<span data-ttu-id="929fb-139">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="929fb-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="929fb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929fb-140">CommonParameters</span></span>
<span data-ttu-id="929fb-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="929fb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929fb-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="929fb-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929fb-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="929fb-143">INPUTS</span></span>

### <span data-ttu-id="929fb-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="929fb-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="929fb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="929fb-145">System.String</span></span>

## <span data-ttu-id="929fb-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="929fb-146">OUTPUTS</span></span>

### <span data-ttu-id="929fb-147">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="929fb-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="929fb-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="929fb-148">NOTES</span></span>
<span data-ttu-id="929fb-149">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, acessibilidade, relatório</span><span class="sxs-lookup"><span data-stu-id="929fb-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="929fb-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="929fb-150">RELATED LINKS</span></span>

[<span data-ttu-id="929fb-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="929fb-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="929fb-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="929fb-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="929fb-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="929fb-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="929fb-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="929fb-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="929fb-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="929fb-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="929fb-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="929fb-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="929fb-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="929fb-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="929fb-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="929fb-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="929fb-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="929fb-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="929fb-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="929fb-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="929fb-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="929fb-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="929fb-162">Parar-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="929fb-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
