---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602264"
---
# <span data-ttu-id="44884-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="44884-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="44884-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44884-102">SYNOPSIS</span></span>
<span data-ttu-id="44884-103">Obtém os valores métricos de um recurso.</span><span class="sxs-lookup"><span data-stu-id="44884-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44884-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44884-104">SYNTAX</span></span>

### <span data-ttu-id="44884-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="44884-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44884-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="44884-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44884-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44884-107">DESCRIPTION</span></span>
<span data-ttu-id="44884-108">O cmdlet **Get-AzureRmMetric** Obtém os valores métricos de um recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="44884-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="44884-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44884-109">EXAMPLES</span></span>

### <span data-ttu-id="44884-110">Exemplo 1: obter uma métrica com saída resumida</span><span class="sxs-lookup"><span data-stu-id="44884-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="44884-111">Esse comando obtém os valores métricos de website3 com um intervalo de tempo de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="44884-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="44884-112">Exemplo 2: obter uma métrica com saída detalhada</span><span class="sxs-lookup"><span data-stu-id="44884-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="44884-113">Esse comando obtém os valores métricos de website3 com um intervalo de tempo de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="44884-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="44884-114">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="44884-114">The output is detailed.</span></span>

### <span data-ttu-id="44884-115">Exemplo 3: obter saída detalhada para uma métrica especificada</span><span class="sxs-lookup"><span data-stu-id="44884-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="44884-116">Esse comando obtém a saída detalhada para a métrica de solicitações.</span><span class="sxs-lookup"><span data-stu-id="44884-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="44884-117">OS</span><span class="sxs-lookup"><span data-stu-id="44884-117">PARAMETERS</span></span>

### <span data-ttu-id="44884-118">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="44884-118">-AggregationType</span></span>
<span data-ttu-id="44884-119">O tipo de agregação da consulta</span><span class="sxs-lookup"><span data-stu-id="44884-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44884-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44884-120">-DefaultProfile</span></span>
<span data-ttu-id="44884-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44884-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44884-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="44884-122">-DetailedOutput</span></span>
<span data-ttu-id="44884-123">Indica que esse cmdlet exibe a saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="44884-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="44884-124">Por padrão, a saída é resumida.</span><span class="sxs-lookup"><span data-stu-id="44884-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44884-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="44884-125">-EndTime</span></span>
<span data-ttu-id="44884-126">Especifica a hora de término da consulta na hora local.</span><span class="sxs-lookup"><span data-stu-id="44884-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="44884-127">O padrão é a hora atual.</span><span class="sxs-lookup"><span data-stu-id="44884-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44884-128">-Metricname</span><span class="sxs-lookup"><span data-stu-id="44884-128">-MetricName</span></span>
<span data-ttu-id="44884-129">Especifica uma matriz de nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="44884-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44884-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44884-130">-ResourceId</span></span>
<span data-ttu-id="44884-131">Especifica a ID do recurso da métrica.</span><span class="sxs-lookup"><span data-stu-id="44884-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44884-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="44884-132">-StartTime</span></span>
<span data-ttu-id="44884-133">Especifica a hora de início da consulta na hora local.</span><span class="sxs-lookup"><span data-stu-id="44884-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="44884-134">O padrão é a hora local atual menos uma hora.</span><span class="sxs-lookup"><span data-stu-id="44884-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44884-135">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="44884-135">-TimeGrain</span></span>
<span data-ttu-id="44884-136">Especifica o intervalo de tempo da métrica como um objeto **TimeSpan** no formato hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="44884-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44884-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44884-137">CommonParameters</span></span>
<span data-ttu-id="44884-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44884-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44884-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44884-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44884-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44884-140">INPUTS</span></span>

### <span data-ttu-id="44884-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="44884-141">None</span></span>
<span data-ttu-id="44884-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="44884-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44884-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44884-143">OUTPUTS</span></span>

### <span data-ttu-id="44884-144">Microsoft. Azure. Commands. insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="44884-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="44884-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44884-145">NOTES</span></span>

## <span data-ttu-id="44884-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44884-146">RELATED LINKS</span></span>

[<span data-ttu-id="44884-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="44884-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


