---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 575c6e5b210ca47e1904c5174f97b5886b0428b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603277"
---
# <span data-ttu-id="43a20-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="43a20-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="43a20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43a20-102">SYNOPSIS</span></span>
<span data-ttu-id="43a20-103">Cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="43a20-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43a20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43a20-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43a20-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43a20-105">DESCRIPTION</span></span>
<span data-ttu-id="43a20-106">O cmdlet **New-AzureRmAutoscaleRule** cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="43a20-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="43a20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43a20-107">EXAMPLES</span></span>

### <span data-ttu-id="43a20-108">Exemplo 1: criar uma regra</span><span class="sxs-lookup"><span data-stu-id="43a20-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="43a20-109">Esse comando cria uma regra.</span><span class="sxs-lookup"><span data-stu-id="43a20-109">This command creates a rule.</span></span>

### <span data-ttu-id="43a20-110">Exemplo 2: criar duas regras</span><span class="sxs-lookup"><span data-stu-id="43a20-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="43a20-111">O primeiro comando cria uma regra para a métrica de solicitações e a armazena na variável $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="43a20-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="43a20-112">O segundo comando cria uma segunda regra para a métrica de solicitações e, em seguida, armazena-a na variável $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="43a20-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="43a20-113">OS</span><span class="sxs-lookup"><span data-stu-id="43a20-113">PARAMETERS</span></span>

### <span data-ttu-id="43a20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a20-114">-DefaultProfile</span></span>
<span data-ttu-id="43a20-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="43a20-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43a20-116">-Metricname</span><span class="sxs-lookup"><span data-stu-id="43a20-116">-MetricName</span></span>
<span data-ttu-id="43a20-117">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="43a20-117">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="43a20-118">-MetricResourceId</span></span>
<span data-ttu-id="43a20-119">Especifica a ID do recurso métrico.</span><span class="sxs-lookup"><span data-stu-id="43a20-119">Specifies the metric resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="43a20-120">-MetricStatistic</span></span>
<span data-ttu-id="43a20-121">Especifica a estatística métrica.</span><span class="sxs-lookup"><span data-stu-id="43a20-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="43a20-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="43a20-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43a20-123">Médio</span><span class="sxs-lookup"><span data-stu-id="43a20-123">Average</span></span>
- <span data-ttu-id="43a20-124">Min</span><span class="sxs-lookup"><span data-stu-id="43a20-124">Min</span></span>
- <span data-ttu-id="43a20-125">Máxima</span><span class="sxs-lookup"><span data-stu-id="43a20-125">Max</span></span>
- <span data-ttu-id="43a20-126">Soma</span><span class="sxs-lookup"><span data-stu-id="43a20-126">Sum</span></span>

```yaml
Type: MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-127">-Operador</span><span class="sxs-lookup"><span data-stu-id="43a20-127">-Operator</span></span>
<span data-ttu-id="43a20-128">Especifica o operador.</span><span class="sxs-lookup"><span data-stu-id="43a20-128">Specifies the operator.</span></span>
<span data-ttu-id="43a20-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="43a20-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43a20-130">Seja</span><span class="sxs-lookup"><span data-stu-id="43a20-130">Equals</span></span>
- <span data-ttu-id="43a20-131">Não é igual a</span><span class="sxs-lookup"><span data-stu-id="43a20-131">NotEquals</span></span>
- <span data-ttu-id="43a20-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="43a20-132">GreaterThan</span></span>
- <span data-ttu-id="43a20-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="43a20-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="43a20-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="43a20-134">LessThan</span></span>
- <span data-ttu-id="43a20-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="43a20-135">LessThanOrEqual</span></span>

```yaml
Type: ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="43a20-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="43a20-137">Especifica a ação de autoescala cooldown o tempo.</span><span class="sxs-lookup"><span data-stu-id="43a20-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="43a20-138">-ScaleActionDirection</span></span>
<span data-ttu-id="43a20-139">Especifica a direção da ação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="43a20-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="43a20-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="43a20-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43a20-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="43a20-141">None</span></span>
- <span data-ttu-id="43a20-142">Tornar</span><span class="sxs-lookup"><span data-stu-id="43a20-142">Increase</span></span>
- <span data-ttu-id="43a20-143">Reduz</span><span class="sxs-lookup"><span data-stu-id="43a20-143">Decrease</span></span>

```yaml
Type: ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="43a20-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="43a20-145">Especifica o tipo de escala.</span><span class="sxs-lookup"><span data-stu-id="43a20-145">Specifies the scale type.</span></span>
<span data-ttu-id="43a20-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="43a20-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43a20-147">Alterar</span><span class="sxs-lookup"><span data-stu-id="43a20-147">ChangeSize</span></span>
- <span data-ttu-id="43a20-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="43a20-148">ChangeCount</span></span>
- <span data-ttu-id="43a20-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="43a20-149">PercentChangeCount</span></span>
- <span data-ttu-id="43a20-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="43a20-150">ExactCount</span></span>

```yaml
Type: ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="43a20-151">-ScaleActionValue</span></span>
<span data-ttu-id="43a20-152">Especifica o valor da ação.</span><span class="sxs-lookup"><span data-stu-id="43a20-152">Specifies the action value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-153">-Threshold</span><span class="sxs-lookup"><span data-stu-id="43a20-153">-Threshold</span></span>
<span data-ttu-id="43a20-154">Especifica o limite do valor da métrica.</span><span class="sxs-lookup"><span data-stu-id="43a20-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="43a20-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="43a20-156">Especifica o operador de agregação de tempo.</span><span class="sxs-lookup"><span data-stu-id="43a20-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="43a20-157">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="43a20-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43a20-158">Médio</span><span class="sxs-lookup"><span data-stu-id="43a20-158">Average</span></span>
- <span data-ttu-id="43a20-159">Nível</span><span class="sxs-lookup"><span data-stu-id="43a20-159">Minimum</span></span>
- <span data-ttu-id="43a20-160">Melhor</span><span class="sxs-lookup"><span data-stu-id="43a20-160">Maximum</span></span>
- <span data-ttu-id="43a20-161">Nome</span><span class="sxs-lookup"><span data-stu-id="43a20-161">Last</span></span>
- <span data-ttu-id="43a20-162">Total, contagem</span><span class="sxs-lookup"><span data-stu-id="43a20-162">Total, Count</span></span>

```yaml
Type: TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-163">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="43a20-163">-TimeGrain</span></span>
<span data-ttu-id="43a20-164">Especifica o intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="43a20-164">Specifies the time grain.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-165">-Janela de tempo</span><span class="sxs-lookup"><span data-stu-id="43a20-165">-TimeWindow</span></span>
<span data-ttu-id="43a20-166">Especifica a janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="43a20-166">Specifies the time window.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a20-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a20-167">CommonParameters</span></span>
<span data-ttu-id="43a20-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a20-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a20-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a20-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a20-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43a20-170">INPUTS</span></span>

### <span data-ttu-id="43a20-171">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="43a20-171">None</span></span>
<span data-ttu-id="43a20-172">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="43a20-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43a20-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43a20-173">OUTPUTS</span></span>

### <span data-ttu-id="43a20-174">Microsoft. Azure. Management. monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="43a20-174">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="43a20-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43a20-175">NOTES</span></span>

## <span data-ttu-id="43a20-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43a20-176">RELATED LINKS</span></span>

[<span data-ttu-id="43a20-177">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="43a20-177">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="43a20-178">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="43a20-178">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="43a20-179">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="43a20-179">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="43a20-180">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="43a20-180">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="43a20-181">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="43a20-181">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


