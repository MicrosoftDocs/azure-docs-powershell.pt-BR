---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: bb2301fceef993e131472e497e2c89e7ef6ecbf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888880"
---
# <span data-ttu-id="94098-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="94098-101">Get-AzMetric</span></span>

## <span data-ttu-id="94098-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94098-102">SYNOPSIS</span></span>
<span data-ttu-id="94098-103">Obtém os valores métricos de um recurso.</span><span class="sxs-lookup"><span data-stu-id="94098-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="94098-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="94098-104">SYNTAX</span></span>

### <span data-ttu-id="94098-105">GetWithDefaultParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="94098-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94098-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="94098-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94098-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="94098-107">DESCRIPTION</span></span>
<span data-ttu-id="94098-108">O cmdlet **Get-AzMetric** obtém os valores métricos de um recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="94098-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="94098-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94098-109">EXAMPLES</span></span>

### <span data-ttu-id="94098-110">Exemplo 1: Obter uma métrica com saída resumida</span><span class="sxs-lookup"><span data-stu-id="94098-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
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

<span data-ttu-id="94098-111">Este comando obtém os valores métricos do site3 com um tempo de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="94098-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="94098-112">Exemplo 2: Obter uma métrica com saída detalhada</span><span class="sxs-lookup"><span data-stu-id="94098-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="94098-113">Este comando obtém os valores métricos do site3 com um tempo de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="94098-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="94098-114">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="94098-114">The output is detailed.</span></span>

### <span data-ttu-id="94098-115">Exemplo 3: Obter saída detalhada para uma métrica especificada</span><span class="sxs-lookup"><span data-stu-id="94098-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricName "Requests" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="94098-116">Este comando obtém uma saída detalhada para a métrica Solicitações.</span><span class="sxs-lookup"><span data-stu-id="94098-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="94098-117">Exemplo 4: Obter saída resumida para uma métrica especificada com filtro de dimensão especificado</span><span class="sxs-lookup"><span data-stu-id="94098-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","Toronto"), (New-AzMetricFilter -Dimension AuthenticationType -Operator eq -Value User))

PS C:\> Get-AzMetric -ResourceId <resourceId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="94098-118">Este comando obtém uma saída resumida para a métrica PageViews com filtro de dimensão especificado e tipo de agregação.</span><span class="sxs-lookup"><span data-stu-id="94098-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="94098-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="94098-119">PARAMETERS</span></span>

### <span data-ttu-id="94098-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="94098-120">-AggregationType</span></span>
<span data-ttu-id="94098-121">O tipo de agregação da consulta</span><span class="sxs-lookup"><span data-stu-id="94098-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94098-122">-DefaultProfile</span></span>
<span data-ttu-id="94098-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="94098-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94098-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="94098-124">-DetailedOutput</span></span>
<span data-ttu-id="94098-125">Indica que esse cmdlet exibe saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="94098-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="94098-126">Por padrão, a saída é resumida.</span><span class="sxs-lookup"><span data-stu-id="94098-126">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="94098-127">-EndTime</span></span>
<span data-ttu-id="94098-128">Especifica a hora de término da consulta em horário local.</span><span class="sxs-lookup"><span data-stu-id="94098-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="94098-129">O padrão é a hora atual.</span><span class="sxs-lookup"><span data-stu-id="94098-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="94098-130">-MetricFilter</span></span>
<span data-ttu-id="94098-131">Especifica o filtro de dimensão métrica para o qual as métricas de consulta são consultadas.</span><span class="sxs-lookup"><span data-stu-id="94098-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="94098-132">-MetricName</span></span>
<span data-ttu-id="94098-133">Especifica uma matriz de nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="94098-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="94098-134">-MetricNamespace</span></span>
<span data-ttu-id="94098-135">Especifica o namespace métrico para o qual consultar métricas.</span><span class="sxs-lookup"><span data-stu-id="94098-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="94098-136">-OrderBy</span></span>
<span data-ttu-id="94098-137">Especifica a agregação a ser usada para classificar resultados e a direção da classificação (Exemplo: soma asc).</span><span class="sxs-lookup"><span data-stu-id="94098-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94098-138">-ResourceId</span></span>
<span data-ttu-id="94098-139">Especifica a ID de recurso da métrica.</span><span class="sxs-lookup"><span data-stu-id="94098-139">Specifies the resource ID of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="94098-140">-ResultType</span></span>
<span data-ttu-id="94098-141">Especifica o tipo de resultado a ser retornado (metadados ou dados).</span><span class="sxs-lookup"><span data-stu-id="94098-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="94098-142">-StartTime</span></span>
<span data-ttu-id="94098-143">Especifica a hora de início da consulta em horário local.</span><span class="sxs-lookup"><span data-stu-id="94098-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="94098-144">O padrão é a hora local atual menos uma hora.</span><span class="sxs-lookup"><span data-stu-id="94098-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="94098-145">-TimeGrain</span></span>
<span data-ttu-id="94098-146">Especifica o grain de tempo da métrica como um **objeto TimeSpan** no formato hh:mm:ss.</span><span class="sxs-lookup"><span data-stu-id="94098-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-147">-Top</span><span class="sxs-lookup"><span data-stu-id="94098-147">-Top</span></span>
<span data-ttu-id="94098-148">Especifica o número máximo de registros a serem recuperados (padrão:10), a ser especificado com $filter.</span><span class="sxs-lookup"><span data-stu-id="94098-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94098-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94098-149">CommonParameters</span></span>
<span data-ttu-id="94098-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94098-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94098-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94098-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94098-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94098-152">INPUTS</span></span>

### <span data-ttu-id="94098-153">System.String</span><span class="sxs-lookup"><span data-stu-id="94098-153">System.String</span></span>

### <span data-ttu-id="94098-154">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="94098-154">System.TimeSpan</span></span>

### <span data-ttu-id="94098-155">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="94098-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="94098-156">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="94098-156">System.DateTime</span></span>

### <span data-ttu-id="94098-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="94098-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="94098-158">System.Nullable'1[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="94098-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="94098-159">System.String[]</span><span class="sxs-lookup"><span data-stu-id="94098-159">System.String[]</span></span>

### <span data-ttu-id="94098-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94098-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="94098-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="94098-161">OUTPUTS</span></span>

### <span data-ttu-id="94098-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span><span class="sxs-lookup"><span data-stu-id="94098-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="94098-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="94098-163">NOTES</span></span>

<span data-ttu-id="94098-164">Mais informações sobre as métricas suportadas podem ser encontradas em: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="94098-164">More information about the supported metrics may be found at: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="94098-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94098-165">RELATED LINKS</span></span>

<span data-ttu-id="94098-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="94098-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


