---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440654"
---
# <span data-ttu-id="9e6fd-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="9e6fd-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="9e6fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6fd-103">Cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e6fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e6fd-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6fd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e6fd-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6fd-106">O cmdlet **New-AzureRmAutoscaleRule** cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="9e6fd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e6fd-107">EXAMPLES</span></span>

### <span data-ttu-id="9e6fd-108">Exemplo 1: criar uma regra</span><span class="sxs-lookup"><span data-stu-id="9e6fd-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="9e6fd-109">Esse comando cria uma regra.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-109">This command creates a rule.</span></span>

### <span data-ttu-id="9e6fd-110">Exemplo 2: criar duas regras</span><span class="sxs-lookup"><span data-stu-id="9e6fd-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="9e6fd-111">O primeiro comando cria uma regra para a métrica de solicitações e a armazena na variável $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="9e6fd-112">O segundo comando cria uma segunda regra para a métrica de solicitações e, em seguida, armazena-a na variável $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="9e6fd-113">OS</span><span class="sxs-lookup"><span data-stu-id="9e6fd-113">PARAMETERS</span></span>

### <span data-ttu-id="9e6fd-114">-Metricname</span><span class="sxs-lookup"><span data-stu-id="9e6fd-114">-MetricName</span></span>
<span data-ttu-id="9e6fd-115">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-115">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="9e6fd-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="9e6fd-116">-MetricResourceId</span></span>
<span data-ttu-id="9e6fd-117">Especifica a ID do recurso métrico.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-117">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="9e6fd-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="9e6fd-118">-MetricStatistic</span></span>
<span data-ttu-id="9e6fd-119">Especifica a estatística métrica.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="9e6fd-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e6fd-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e6fd-121">Médio</span><span class="sxs-lookup"><span data-stu-id="9e6fd-121">Average</span></span>
- <span data-ttu-id="9e6fd-122">Min</span><span class="sxs-lookup"><span data-stu-id="9e6fd-122">Min</span></span>
- <span data-ttu-id="9e6fd-123">Máxima</span><span class="sxs-lookup"><span data-stu-id="9e6fd-123">Max</span></span>
- <span data-ttu-id="9e6fd-124">Soma</span><span class="sxs-lookup"><span data-stu-id="9e6fd-124">Sum</span></span>

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

### <span data-ttu-id="9e6fd-125">-Operador</span><span class="sxs-lookup"><span data-stu-id="9e6fd-125">-Operator</span></span>
<span data-ttu-id="9e6fd-126">Especifica o operador.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-126">Specifies the operator.</span></span>
<span data-ttu-id="9e6fd-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e6fd-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e6fd-128">Seja</span><span class="sxs-lookup"><span data-stu-id="9e6fd-128">Equals</span></span>
- <span data-ttu-id="9e6fd-129">Não é igual a</span><span class="sxs-lookup"><span data-stu-id="9e6fd-129">NotEquals</span></span>
- <span data-ttu-id="9e6fd-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="9e6fd-130">GreaterThan</span></span>
- <span data-ttu-id="9e6fd-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="9e6fd-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="9e6fd-132">LessThan</span><span class="sxs-lookup"><span data-stu-id="9e6fd-132">LessThan</span></span>
- <span data-ttu-id="9e6fd-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="9e6fd-133">LessThanOrEqual</span></span>

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

### <span data-ttu-id="9e6fd-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="9e6fd-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="9e6fd-135">Especifica a ação de autoescala cooldown o tempo.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-135">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="9e6fd-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="9e6fd-136">-ScaleActionDirection</span></span>
<span data-ttu-id="9e6fd-137">Especifica a direção da ação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="9e6fd-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e6fd-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e6fd-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9e6fd-139">None</span></span>
- <span data-ttu-id="9e6fd-140">Tornar</span><span class="sxs-lookup"><span data-stu-id="9e6fd-140">Increase</span></span>
- <span data-ttu-id="9e6fd-141">Reduz</span><span class="sxs-lookup"><span data-stu-id="9e6fd-141">Decrease</span></span>

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

### <span data-ttu-id="9e6fd-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="9e6fd-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="9e6fd-143">Especifica o tipo de escala.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-143">Specifies the scale type.</span></span>
<span data-ttu-id="9e6fd-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e6fd-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e6fd-145">Alterar</span><span class="sxs-lookup"><span data-stu-id="9e6fd-145">ChangeSize</span></span>
- <span data-ttu-id="9e6fd-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="9e6fd-146">ChangeCount</span></span>
- <span data-ttu-id="9e6fd-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="9e6fd-147">PercentChangeCount</span></span>
- <span data-ttu-id="9e6fd-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="9e6fd-148">ExactCount</span></span>

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

### <span data-ttu-id="9e6fd-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="9e6fd-149">-ScaleActionValue</span></span>
<span data-ttu-id="9e6fd-150">Especifica o valor da ação.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-150">Specifies the action value.</span></span>

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

### <span data-ttu-id="9e6fd-151">-Threshold</span><span class="sxs-lookup"><span data-stu-id="9e6fd-151">-Threshold</span></span>
<span data-ttu-id="9e6fd-152">Especifica o limite do valor da métrica.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-152">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="9e6fd-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="9e6fd-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="9e6fd-154">Especifica o operador de agregação de tempo.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="9e6fd-155">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e6fd-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e6fd-156">Médio</span><span class="sxs-lookup"><span data-stu-id="9e6fd-156">Average</span></span>
- <span data-ttu-id="9e6fd-157">Nível</span><span class="sxs-lookup"><span data-stu-id="9e6fd-157">Minimum</span></span>
- <span data-ttu-id="9e6fd-158">Melhor</span><span class="sxs-lookup"><span data-stu-id="9e6fd-158">Maximum</span></span>
- <span data-ttu-id="9e6fd-159">Nome</span><span class="sxs-lookup"><span data-stu-id="9e6fd-159">Last</span></span>
- <span data-ttu-id="9e6fd-160">Total, contagem</span><span class="sxs-lookup"><span data-stu-id="9e6fd-160">Total, Count</span></span>

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

### <span data-ttu-id="9e6fd-161">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="9e6fd-161">-TimeGrain</span></span>
<span data-ttu-id="9e6fd-162">Especifica o intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-162">Specifies the time grain.</span></span>

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

### <span data-ttu-id="9e6fd-163">-Janela de tempo</span><span class="sxs-lookup"><span data-stu-id="9e6fd-163">-TimeWindow</span></span>
<span data-ttu-id="9e6fd-164">Especifica a janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="9e6fd-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6fd-165">-DefaultProfile</span></span>
<span data-ttu-id="9e6fd-166">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e6fd-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6fd-167">CommonParameters</span></span>
<span data-ttu-id="9e6fd-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6fd-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6fd-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6fd-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6fd-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e6fd-170">INPUTS</span></span>

## <span data-ttu-id="9e6fd-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e6fd-171">OUTPUTS</span></span>

### <span data-ttu-id="9e6fd-172">Microsoft. Azure. Management. monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="9e6fd-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="9e6fd-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e6fd-173">NOTES</span></span>

## <span data-ttu-id="9e6fd-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e6fd-174">RELATED LINKS</span></span>

[<span data-ttu-id="9e6fd-175">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9e6fd-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9e6fd-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="9e6fd-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="9e6fd-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9e6fd-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9e6fd-178">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9e6fd-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="9e6fd-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9e6fd-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


