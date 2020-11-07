---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: 2464a3b7fb35cce28dd06884cd8ed69e5197eced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770297"
---
# <span data-ttu-id="7f21a-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="7f21a-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="7f21a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f21a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f21a-103">Cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="7f21a-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="7f21a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f21a-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f21a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f21a-105">DESCRIPTION</span></span>
<span data-ttu-id="7f21a-106">O cmdlet **New-AzAutoscaleRule** cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="7f21a-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="7f21a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f21a-107">EXAMPLES</span></span>

### <span data-ttu-id="7f21a-108">Exemplo 1: criar uma regra</span><span class="sxs-lookup"><span data-stu-id="7f21a-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="7f21a-109">Esse comando cria uma regra.</span><span class="sxs-lookup"><span data-stu-id="7f21a-109">This command creates a rule.</span></span>

### <span data-ttu-id="7f21a-110">Exemplo 2: criar duas regras</span><span class="sxs-lookup"><span data-stu-id="7f21a-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="7f21a-111">O primeiro comando cria uma regra para a métrica de solicitações e a armazena na variável $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="7f21a-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="7f21a-112">O segundo comando cria uma segunda regra para a métrica de solicitações e, em seguida, armazena-a na variável $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="7f21a-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="7f21a-113">OS</span><span class="sxs-lookup"><span data-stu-id="7f21a-113">PARAMETERS</span></span>

### <span data-ttu-id="7f21a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f21a-114">-DefaultProfile</span></span>
<span data-ttu-id="7f21a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7f21a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f21a-116">-Metricname</span><span class="sxs-lookup"><span data-stu-id="7f21a-116">-MetricName</span></span>
<span data-ttu-id="7f21a-117">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="7f21a-117">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="7f21a-118">-MetricResourceId</span></span>
<span data-ttu-id="7f21a-119">Especifica a ID do recurso métrico.</span><span class="sxs-lookup"><span data-stu-id="7f21a-119">Specifies the metric resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="7f21a-120">-MetricStatistic</span></span>
<span data-ttu-id="7f21a-121">Especifica a estatística métrica.</span><span class="sxs-lookup"><span data-stu-id="7f21a-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="7f21a-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f21a-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f21a-123">Médio</span><span class="sxs-lookup"><span data-stu-id="7f21a-123">Average</span></span>
- <span data-ttu-id="7f21a-124">Min</span><span class="sxs-lookup"><span data-stu-id="7f21a-124">Min</span></span>
- <span data-ttu-id="7f21a-125">Máxima</span><span class="sxs-lookup"><span data-stu-id="7f21a-125">Max</span></span>
- <span data-ttu-id="7f21a-126">Soma</span><span class="sxs-lookup"><span data-stu-id="7f21a-126">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-127">-Operador</span><span class="sxs-lookup"><span data-stu-id="7f21a-127">-Operator</span></span>
<span data-ttu-id="7f21a-128">Especifica o operador.</span><span class="sxs-lookup"><span data-stu-id="7f21a-128">Specifies the operator.</span></span>
<span data-ttu-id="7f21a-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f21a-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f21a-130">Seja</span><span class="sxs-lookup"><span data-stu-id="7f21a-130">Equals</span></span>
- <span data-ttu-id="7f21a-131">Não é igual a</span><span class="sxs-lookup"><span data-stu-id="7f21a-131">NotEquals</span></span>
- <span data-ttu-id="7f21a-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="7f21a-132">GreaterThan</span></span>
- <span data-ttu-id="7f21a-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7f21a-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="7f21a-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="7f21a-134">LessThan</span></span>
- <span data-ttu-id="7f21a-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="7f21a-135">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases:
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="7f21a-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="7f21a-137">Especifica a ação de autoescala cooldown o tempo.</span><span class="sxs-lookup"><span data-stu-id="7f21a-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="7f21a-138">-ScaleActionDirection</span></span>
<span data-ttu-id="7f21a-139">Especifica a direção da ação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="7f21a-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="7f21a-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f21a-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f21a-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7f21a-141">None</span></span>
- <span data-ttu-id="7f21a-142">Tornar</span><span class="sxs-lookup"><span data-stu-id="7f21a-142">Increase</span></span>
- <span data-ttu-id="7f21a-143">Reduz</span><span class="sxs-lookup"><span data-stu-id="7f21a-143">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases:
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="7f21a-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="7f21a-145">Especifica o tipo de escala.</span><span class="sxs-lookup"><span data-stu-id="7f21a-145">Specifies the scale type.</span></span>
<span data-ttu-id="7f21a-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f21a-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f21a-147">Alterar</span><span class="sxs-lookup"><span data-stu-id="7f21a-147">ChangeSize</span></span>
- <span data-ttu-id="7f21a-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="7f21a-148">ChangeCount</span></span>
- <span data-ttu-id="7f21a-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="7f21a-149">PercentChangeCount</span></span>
- <span data-ttu-id="7f21a-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="7f21a-150">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases:
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="7f21a-151">-ScaleActionValue</span></span>
<span data-ttu-id="7f21a-152">Especifica o valor da ação.</span><span class="sxs-lookup"><span data-stu-id="7f21a-152">Specifies the action value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-153">-Threshold</span><span class="sxs-lookup"><span data-stu-id="7f21a-153">-Threshold</span></span>
<span data-ttu-id="7f21a-154">Especifica o limite do valor da métrica.</span><span class="sxs-lookup"><span data-stu-id="7f21a-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="7f21a-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="7f21a-156">Especifica o operador de agregação de tempo.</span><span class="sxs-lookup"><span data-stu-id="7f21a-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="7f21a-157">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7f21a-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f21a-158">Médio</span><span class="sxs-lookup"><span data-stu-id="7f21a-158">Average</span></span>
- <span data-ttu-id="7f21a-159">Nível</span><span class="sxs-lookup"><span data-stu-id="7f21a-159">Minimum</span></span>
- <span data-ttu-id="7f21a-160">Melhor</span><span class="sxs-lookup"><span data-stu-id="7f21a-160">Maximum</span></span>
- <span data-ttu-id="7f21a-161">Nome</span><span class="sxs-lookup"><span data-stu-id="7f21a-161">Last</span></span>
- <span data-ttu-id="7f21a-162">Total, contagem</span><span class="sxs-lookup"><span data-stu-id="7f21a-162">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-163">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="7f21a-163">-TimeGrain</span></span>
<span data-ttu-id="7f21a-164">Especifica o intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="7f21a-164">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f21a-165">-Janela de tempo</span><span class="sxs-lookup"><span data-stu-id="7f21a-165">-TimeWindow</span></span>
<span data-ttu-id="7f21a-166">Especifica a janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="7f21a-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="7f21a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f21a-167">CommonParameters</span></span>
<span data-ttu-id="7f21a-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f21a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f21a-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f21a-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f21a-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f21a-170">INPUTS</span></span>

### <span data-ttu-id="7f21a-171">System. String</span><span class="sxs-lookup"><span data-stu-id="7f21a-171">System.String</span></span>

### <span data-ttu-id="7f21a-172">Microsoft. Azure. Management. monitor. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="7f21a-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="7f21a-173">Microsoft. Azure. Management. monitor. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="7f21a-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="7f21a-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="7f21a-174">System.Double</span></span>

### <span data-ttu-id="7f21a-175">Microsoft. Azure. Management. monitor. Management. Models. timeaggregationtype</span><span class="sxs-lookup"><span data-stu-id="7f21a-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="7f21a-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="7f21a-176">System.TimeSpan</span></span>

### <span data-ttu-id="7f21a-177">Microsoft. Azure. Management. monitor. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="7f21a-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="7f21a-178">Microsoft. Azure. Management. monitor. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="7f21a-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="7f21a-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f21a-179">OUTPUTS</span></span>

### <span data-ttu-id="7f21a-180">Microsoft. Azure. Management. monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="7f21a-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="7f21a-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f21a-181">NOTES</span></span>

## <span data-ttu-id="7f21a-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f21a-182">RELATED LINKS</span></span>

[<span data-ttu-id="7f21a-183">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7f21a-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="7f21a-184">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="7f21a-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="7f21a-185">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7f21a-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="7f21a-186">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="7f21a-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="7f21a-187">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7f21a-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


