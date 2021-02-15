---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117525"
---
# <span data-ttu-id="318cc-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="318cc-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="318cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="318cc-102">SYNOPSIS</span></span>
<span data-ttu-id="318cc-103">Cria uma regra de Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="318cc-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="318cc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="318cc-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="318cc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="318cc-105">DESCRIPTION</span></span>
<span data-ttu-id="318cc-106">O **cmdlet New-AzAutoscaleRule** cria uma regra de escala automática.</span><span class="sxs-lookup"><span data-stu-id="318cc-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="318cc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="318cc-107">EXAMPLES</span></span>

### <span data-ttu-id="318cc-108">Exemplo 1: Criar uma regra</span><span class="sxs-lookup"><span data-stu-id="318cc-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="318cc-109">Esse comando cria uma regra.</span><span class="sxs-lookup"><span data-stu-id="318cc-109">This command creates a rule.</span></span>

### <span data-ttu-id="318cc-110">Exemplo 2: Criar duas regras</span><span class="sxs-lookup"><span data-stu-id="318cc-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="318cc-111">O primeiro comando cria uma regra para a métrica solicitações e a armazena na variável $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="318cc-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="318cc-112">O segundo comando cria uma segunda regra para a métrica solicitações e a armazena na variável $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="318cc-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="318cc-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="318cc-113">Example 3</span></span>

<span data-ttu-id="318cc-114">Cria uma regra de Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="318cc-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="318cc-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="318cc-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="318cc-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="318cc-116">PARAMETERS</span></span>

### <span data-ttu-id="318cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318cc-117">-DefaultProfile</span></span>
<span data-ttu-id="318cc-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="318cc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="318cc-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="318cc-119">-MetricName</span></span>
<span data-ttu-id="318cc-120">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="318cc-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="318cc-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="318cc-121">-MetricResourceId</span></span>
<span data-ttu-id="318cc-122">Especifica a ID do recurso métrico.</span><span class="sxs-lookup"><span data-stu-id="318cc-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="318cc-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="318cc-123">-MetricStatistic</span></span>
<span data-ttu-id="318cc-124">Especifica a estatística métrica.</span><span class="sxs-lookup"><span data-stu-id="318cc-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="318cc-125">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="318cc-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="318cc-126">Média</span><span class="sxs-lookup"><span data-stu-id="318cc-126">Average</span></span>
- <span data-ttu-id="318cc-127">Min</span><span class="sxs-lookup"><span data-stu-id="318cc-127">Min</span></span>
- <span data-ttu-id="318cc-128">Max</span><span class="sxs-lookup"><span data-stu-id="318cc-128">Max</span></span>
- <span data-ttu-id="318cc-129">Soma</span><span class="sxs-lookup"><span data-stu-id="318cc-129">Sum</span></span>

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

### <span data-ttu-id="318cc-130">-Operador</span><span class="sxs-lookup"><span data-stu-id="318cc-130">-Operator</span></span>
<span data-ttu-id="318cc-131">Especifica o operador.</span><span class="sxs-lookup"><span data-stu-id="318cc-131">Specifies the operator.</span></span>
<span data-ttu-id="318cc-132">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="318cc-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="318cc-133">Equals</span><span class="sxs-lookup"><span data-stu-id="318cc-133">Equals</span></span>
- <span data-ttu-id="318cc-134">Notequals</span><span class="sxs-lookup"><span data-stu-id="318cc-134">NotEquals</span></span>
- <span data-ttu-id="318cc-135">Greaterthan</span><span class="sxs-lookup"><span data-stu-id="318cc-135">GreaterThan</span></span>
- <span data-ttu-id="318cc-136">Greaterthanorequal</span><span class="sxs-lookup"><span data-stu-id="318cc-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="318cc-137">Lessthan</span><span class="sxs-lookup"><span data-stu-id="318cc-137">LessThan</span></span>
- <span data-ttu-id="318cc-138">Lessthanorequal</span><span class="sxs-lookup"><span data-stu-id="318cc-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="318cc-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="318cc-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="318cc-140">Especifica o tempo de recarga da ação de Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="318cc-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="318cc-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="318cc-141">-ScaleActionDirection</span></span>
<span data-ttu-id="318cc-142">Especifica a direção da ação de escala.</span><span class="sxs-lookup"><span data-stu-id="318cc-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="318cc-143">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="318cc-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="318cc-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="318cc-144">None</span></span>
- <span data-ttu-id="318cc-145">Aumentar</span><span class="sxs-lookup"><span data-stu-id="318cc-145">Increase</span></span>
- <span data-ttu-id="318cc-146">Diminuir</span><span class="sxs-lookup"><span data-stu-id="318cc-146">Decrease</span></span>

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

### <span data-ttu-id="318cc-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="318cc-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="318cc-148">Especifica o tipo de escala.</span><span class="sxs-lookup"><span data-stu-id="318cc-148">Specifies the scale type.</span></span>
<span data-ttu-id="318cc-149">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="318cc-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="318cc-150">AlterarEsize</span><span class="sxs-lookup"><span data-stu-id="318cc-150">ChangeSize</span></span>
- <span data-ttu-id="318cc-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="318cc-151">ChangeCount</span></span>
- <span data-ttu-id="318cc-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="318cc-152">PercentChangeCount</span></span>
- <span data-ttu-id="318cc-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="318cc-153">ExactCount</span></span>

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

### <span data-ttu-id="318cc-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="318cc-154">-ScaleActionValue</span></span>
<span data-ttu-id="318cc-155">Especifica o valor da ação.</span><span class="sxs-lookup"><span data-stu-id="318cc-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="318cc-156">-Limite</span><span class="sxs-lookup"><span data-stu-id="318cc-156">-Threshold</span></span>
<span data-ttu-id="318cc-157">Especifica o limite do valor métrico.</span><span class="sxs-lookup"><span data-stu-id="318cc-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="318cc-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="318cc-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="318cc-159">Especifica o operador de agregação de tempo.</span><span class="sxs-lookup"><span data-stu-id="318cc-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="318cc-160">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="318cc-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="318cc-161">Média</span><span class="sxs-lookup"><span data-stu-id="318cc-161">Average</span></span>
- <span data-ttu-id="318cc-162">Mínimo</span><span class="sxs-lookup"><span data-stu-id="318cc-162">Minimum</span></span>
- <span data-ttu-id="318cc-163">Máximo</span><span class="sxs-lookup"><span data-stu-id="318cc-163">Maximum</span></span>
- <span data-ttu-id="318cc-164">Última</span><span class="sxs-lookup"><span data-stu-id="318cc-164">Last</span></span>
- <span data-ttu-id="318cc-165">Total, Contagem</span><span class="sxs-lookup"><span data-stu-id="318cc-165">Total, Count</span></span>

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

### <span data-ttu-id="318cc-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="318cc-166">-TimeGrain</span></span>
<span data-ttu-id="318cc-167">Especifica o tempo de trigo.</span><span class="sxs-lookup"><span data-stu-id="318cc-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="318cc-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="318cc-168">-TimeWindow</span></span>
<span data-ttu-id="318cc-169">Especifica a janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="318cc-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="318cc-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318cc-170">CommonParameters</span></span>
<span data-ttu-id="318cc-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318cc-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318cc-172">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="318cc-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318cc-173">Entradas</span><span class="sxs-lookup"><span data-stu-id="318cc-173">INPUTS</span></span>

### <span data-ttu-id="318cc-174">System.String</span><span class="sxs-lookup"><span data-stu-id="318cc-174">System.String</span></span>

### <span data-ttu-id="318cc-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="318cc-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="318cc-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="318cc-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="318cc-177">System.Double</span><span class="sxs-lookup"><span data-stu-id="318cc-177">System.Double</span></span>

### <span data-ttu-id="318cc-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="318cc-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="318cc-179">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="318cc-179">System.TimeSpan</span></span>

### <span data-ttu-id="318cc-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="318cc-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="318cc-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span><span class="sxs-lookup"><span data-stu-id="318cc-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="318cc-182">Saídas</span><span class="sxs-lookup"><span data-stu-id="318cc-182">OUTPUTS</span></span>

### <span data-ttu-id="318cc-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span><span class="sxs-lookup"><span data-stu-id="318cc-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="318cc-184">Notas</span><span class="sxs-lookup"><span data-stu-id="318cc-184">NOTES</span></span>

## <span data-ttu-id="318cc-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="318cc-185">RELATED LINKS</span></span>

[<span data-ttu-id="318cc-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="318cc-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="318cc-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="318cc-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="318cc-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="318cc-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="318cc-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="318cc-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="318cc-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="318cc-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


