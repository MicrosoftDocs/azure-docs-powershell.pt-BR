---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261191"
---
# <span data-ttu-id="096b4-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="096b4-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="096b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="096b4-102">SYNOPSIS</span></span>
<span data-ttu-id="096b4-103">Cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="096b4-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="096b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="096b4-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="096b4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="096b4-105">DESCRIPTION</span></span>
<span data-ttu-id="096b4-106">O cmdlet **New-AzAutoscaleRule** cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="096b4-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="096b4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="096b4-107">EXAMPLES</span></span>

### <span data-ttu-id="096b4-108">Exemplo 1: criar uma regra</span><span class="sxs-lookup"><span data-stu-id="096b4-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="096b4-109">Esse comando cria uma regra.</span><span class="sxs-lookup"><span data-stu-id="096b4-109">This command creates a rule.</span></span>

### <span data-ttu-id="096b4-110">Exemplo 2: criar duas regras</span><span class="sxs-lookup"><span data-stu-id="096b4-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="096b4-111">O primeiro comando cria uma regra para a métrica de solicitações e a armazena na variável $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="096b4-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="096b4-112">O segundo comando cria uma segunda regra para a métrica de solicitações e, em seguida, armazena-a na variável $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="096b4-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="096b4-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="096b4-113">Example 3</span></span>

<span data-ttu-id="096b4-114">Cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="096b4-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="096b4-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="096b4-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="096b4-116">OS</span><span class="sxs-lookup"><span data-stu-id="096b4-116">PARAMETERS</span></span>

### <span data-ttu-id="096b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096b4-117">-DefaultProfile</span></span>
<span data-ttu-id="096b4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="096b4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="096b4-119">-Metricname</span><span class="sxs-lookup"><span data-stu-id="096b4-119">-MetricName</span></span>
<span data-ttu-id="096b4-120">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="096b4-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="096b4-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="096b4-121">-MetricResourceId</span></span>
<span data-ttu-id="096b4-122">Especifica a ID do recurso métrico.</span><span class="sxs-lookup"><span data-stu-id="096b4-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="096b4-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="096b4-123">-MetricStatistic</span></span>
<span data-ttu-id="096b4-124">Especifica a estatística métrica.</span><span class="sxs-lookup"><span data-stu-id="096b4-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="096b4-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="096b4-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="096b4-126">Médio</span><span class="sxs-lookup"><span data-stu-id="096b4-126">Average</span></span>
- <span data-ttu-id="096b4-127">Min</span><span class="sxs-lookup"><span data-stu-id="096b4-127">Min</span></span>
- <span data-ttu-id="096b4-128">Máxima</span><span class="sxs-lookup"><span data-stu-id="096b4-128">Max</span></span>
- <span data-ttu-id="096b4-129">Soma</span><span class="sxs-lookup"><span data-stu-id="096b4-129">Sum</span></span>

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

### <span data-ttu-id="096b4-130">-Operador</span><span class="sxs-lookup"><span data-stu-id="096b4-130">-Operator</span></span>
<span data-ttu-id="096b4-131">Especifica o operador.</span><span class="sxs-lookup"><span data-stu-id="096b4-131">Specifies the operator.</span></span>
<span data-ttu-id="096b4-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="096b4-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="096b4-133">Seja</span><span class="sxs-lookup"><span data-stu-id="096b4-133">Equals</span></span>
- <span data-ttu-id="096b4-134">Não é igual a</span><span class="sxs-lookup"><span data-stu-id="096b4-134">NotEquals</span></span>
- <span data-ttu-id="096b4-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="096b4-135">GreaterThan</span></span>
- <span data-ttu-id="096b4-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="096b4-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="096b4-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="096b4-137">LessThan</span></span>
- <span data-ttu-id="096b4-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="096b4-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="096b4-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="096b4-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="096b4-140">Especifica a ação de autoescala cooldown o tempo.</span><span class="sxs-lookup"><span data-stu-id="096b4-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="096b4-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="096b4-141">-ScaleActionDirection</span></span>
<span data-ttu-id="096b4-142">Especifica a direção da ação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="096b4-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="096b4-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="096b4-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="096b4-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="096b4-144">None</span></span>
- <span data-ttu-id="096b4-145">Tornar</span><span class="sxs-lookup"><span data-stu-id="096b4-145">Increase</span></span>
- <span data-ttu-id="096b4-146">Reduz</span><span class="sxs-lookup"><span data-stu-id="096b4-146">Decrease</span></span>

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

### <span data-ttu-id="096b4-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="096b4-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="096b4-148">Especifica o tipo de escala.</span><span class="sxs-lookup"><span data-stu-id="096b4-148">Specifies the scale type.</span></span>
<span data-ttu-id="096b4-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="096b4-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="096b4-150">Alterar</span><span class="sxs-lookup"><span data-stu-id="096b4-150">ChangeSize</span></span>
- <span data-ttu-id="096b4-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="096b4-151">ChangeCount</span></span>
- <span data-ttu-id="096b4-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="096b4-152">PercentChangeCount</span></span>
- <span data-ttu-id="096b4-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="096b4-153">ExactCount</span></span>

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

### <span data-ttu-id="096b4-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="096b4-154">-ScaleActionValue</span></span>
<span data-ttu-id="096b4-155">Especifica o valor da ação.</span><span class="sxs-lookup"><span data-stu-id="096b4-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="096b4-156">-Threshold</span><span class="sxs-lookup"><span data-stu-id="096b4-156">-Threshold</span></span>
<span data-ttu-id="096b4-157">Especifica o limite do valor da métrica.</span><span class="sxs-lookup"><span data-stu-id="096b4-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="096b4-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="096b4-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="096b4-159">Especifica o operador de agregação de tempo.</span><span class="sxs-lookup"><span data-stu-id="096b4-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="096b4-160">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="096b4-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="096b4-161">Médio</span><span class="sxs-lookup"><span data-stu-id="096b4-161">Average</span></span>
- <span data-ttu-id="096b4-162">Nível</span><span class="sxs-lookup"><span data-stu-id="096b4-162">Minimum</span></span>
- <span data-ttu-id="096b4-163">Melhor</span><span class="sxs-lookup"><span data-stu-id="096b4-163">Maximum</span></span>
- <span data-ttu-id="096b4-164">Nome</span><span class="sxs-lookup"><span data-stu-id="096b4-164">Last</span></span>
- <span data-ttu-id="096b4-165">Total, contagem</span><span class="sxs-lookup"><span data-stu-id="096b4-165">Total, Count</span></span>

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

### <span data-ttu-id="096b4-166">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="096b4-166">-TimeGrain</span></span>
<span data-ttu-id="096b4-167">Especifica o intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="096b4-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="096b4-168">-Janela de tempo</span><span class="sxs-lookup"><span data-stu-id="096b4-168">-TimeWindow</span></span>
<span data-ttu-id="096b4-169">Especifica a janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="096b4-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="096b4-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096b4-170">CommonParameters</span></span>
<span data-ttu-id="096b4-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096b4-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096b4-172">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="096b4-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096b4-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="096b4-173">INPUTS</span></span>

### <span data-ttu-id="096b4-174">System. String</span><span class="sxs-lookup"><span data-stu-id="096b4-174">System.String</span></span>

### <span data-ttu-id="096b4-175">Microsoft. Azure. Management. monitor. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="096b4-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="096b4-176">Microsoft. Azure. Management. monitor. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="096b4-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="096b4-177">System. Double</span><span class="sxs-lookup"><span data-stu-id="096b4-177">System.Double</span></span>

### <span data-ttu-id="096b4-178">Microsoft. Azure. Management. monitor. Management. Models. timeaggregationtype</span><span class="sxs-lookup"><span data-stu-id="096b4-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="096b4-179">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="096b4-179">System.TimeSpan</span></span>

### <span data-ttu-id="096b4-180">Microsoft. Azure. Management. monitor. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="096b4-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="096b4-181">Microsoft. Azure. Management. monitor. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="096b4-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="096b4-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="096b4-182">OUTPUTS</span></span>

### <span data-ttu-id="096b4-183">Microsoft. Azure. Management. monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="096b4-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="096b4-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="096b4-184">NOTES</span></span>

## <span data-ttu-id="096b4-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="096b4-185">RELATED LINKS</span></span>

[<span data-ttu-id="096b4-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="096b4-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="096b4-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="096b4-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="096b4-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="096b4-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="096b4-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="096b4-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="096b4-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="096b4-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


