---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
ms.openlocfilehash: 75335fb09bb8f4187879ab69ab138952cc873993
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786489"
---
# <span data-ttu-id="f96e0-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f96e0-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="f96e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f96e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f96e0-103">Obtém a pontuação de latência relativa para provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="f96e0-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f96e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f96e0-104">SYNTAX</span></span>

### <span data-ttu-id="f96e0-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f96e0-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f96e0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f96e0-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f96e0-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f96e0-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f96e0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f96e0-108">DESCRIPTION</span></span>
<span data-ttu-id="f96e0-109">O Get-AzureRmNetworkWatcherReachabilityReport Obtém a pontuação de latência relativa dos provedores de serviço de Internet de um local especificado para regiões do Azure.</span><span class="sxs-lookup"><span data-stu-id="f96e0-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f96e0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f96e0-110">EXAMPLES</span></span>

### <span data-ttu-id="f96e0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f96e0-111">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="f96e0-112">Obtém latências relativas ao Azure Data Center no oeste dos EUA de 2017-10-10 a 2017-10-12 dentro do estado do país.</span><span class="sxs-lookup"><span data-stu-id="f96e0-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="f96e0-113">OS</span><span class="sxs-lookup"><span data-stu-id="f96e0-113">PARAMETERS</span></span>

### <span data-ttu-id="f96e0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f96e0-114">-AsJob</span></span>
<span data-ttu-id="f96e0-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f96e0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f96e0-116">-Cidade</span><span class="sxs-lookup"><span data-stu-id="f96e0-116">-City</span></span>
<span data-ttu-id="f96e0-117">O nome da cidade.</span><span class="sxs-lookup"><span data-stu-id="f96e0-117">The name of the city.</span></span>

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

### <span data-ttu-id="f96e0-118">-País</span><span class="sxs-lookup"><span data-stu-id="f96e0-118">-Country</span></span>
<span data-ttu-id="f96e0-119">O nome do país.</span><span class="sxs-lookup"><span data-stu-id="f96e0-119">The name of the country.</span></span>

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

### <span data-ttu-id="f96e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f96e0-120">-DefaultProfile</span></span>
<span data-ttu-id="f96e0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f96e0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f96e0-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f96e0-122">-EndTime</span></span>
<span data-ttu-id="f96e0-123">A hora de término do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="f96e0-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="f96e0-124">-Local</span><span class="sxs-lookup"><span data-stu-id="f96e0-124">-Location</span></span>
<span data-ttu-id="f96e0-125">Regiões do Azure opcionais para fazer o escopo da consulta.</span><span class="sxs-lookup"><span data-stu-id="f96e0-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="f96e0-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f96e0-126">-NetworkWatcher</span></span>
<span data-ttu-id="f96e0-127">O recurso de Inspetor de rede</span><span class="sxs-lookup"><span data-stu-id="f96e0-127">The network watcher resource</span></span>

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

### <span data-ttu-id="f96e0-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f96e0-128">-NetworkWatcherName</span></span>
<span data-ttu-id="f96e0-129">O nome do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f96e0-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="f96e0-130">-Provedor</span><span class="sxs-lookup"><span data-stu-id="f96e0-130">-Provider</span></span>
<span data-ttu-id="f96e0-131">Lista de provedores de serviços de Internet.</span><span class="sxs-lookup"><span data-stu-id="f96e0-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="f96e0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f96e0-132">-ResourceGroupName</span></span>
<span data-ttu-id="f96e0-133">O nome do grupo de recursos do Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f96e0-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f96e0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f96e0-134">-ResourceId</span></span>
<span data-ttu-id="f96e0-135">A ID do recurso de Inspetor de rede.</span><span class="sxs-lookup"><span data-stu-id="f96e0-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="f96e0-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f96e0-136">-StartTime</span></span>
<span data-ttu-id="f96e0-137">A hora de início do relatório de acessibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="f96e0-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="f96e0-138">-Estado</span><span class="sxs-lookup"><span data-stu-id="f96e0-138">-State</span></span>
<span data-ttu-id="f96e0-139">O nome do estado.</span><span class="sxs-lookup"><span data-stu-id="f96e0-139">The name of the state.</span></span>

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

### <span data-ttu-id="f96e0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f96e0-140">CommonParameters</span></span>
<span data-ttu-id="f96e0-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f96e0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f96e0-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f96e0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f96e0-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f96e0-143">INPUTS</span></span>

### <span data-ttu-id="f96e0-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f96e0-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f96e0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f96e0-145">System.String</span></span>

## <span data-ttu-id="f96e0-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f96e0-146">OUTPUTS</span></span>

### <span data-ttu-id="f96e0-147">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f96e0-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="f96e0-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f96e0-148">NOTES</span></span>
<span data-ttu-id="f96e0-149">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor de rede, acessibilidade, relatório</span><span class="sxs-lookup"><span data-stu-id="f96e0-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="f96e0-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f96e0-150">RELATED LINKS</span></span>

[<span data-ttu-id="f96e0-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f96e0-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f96e0-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f96e0-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f96e0-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f96e0-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f96e0-154">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f96e0-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f96e0-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f96e0-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f96e0-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f96e0-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f96e0-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f96e0-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f96e0-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f96e0-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f96e0-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f96e0-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f96e0-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f96e0-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f96e0-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f96e0-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f96e0-162">Parar-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f96e0-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
