---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 951f9e5843987d1ad36378716b7a95e5d7a1f0a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886938"
---
# <span data-ttu-id="2daee-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2daee-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="2daee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2daee-102">SYNOPSIS</span></span>
<span data-ttu-id="2daee-103">Cria um objeto criteria local que pode ser usado para criar um novo alerta métrico</span><span class="sxs-lookup"><span data-stu-id="2daee-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="2daee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2daee-104">SYNTAX</span></span>

### <span data-ttu-id="2daee-105">StaticThresholdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2daee-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2daee-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2daee-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2daee-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="2daee-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2daee-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2daee-108">DESCRIPTION</span></span>
<span data-ttu-id="2daee-109">O cmdlet **New-AzMetricAlertRuleV2Criteria** cria um objeto de critérios métricos local a ser usado como um cmdlet [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2) de entrada que cria uma nova regra de alerta métrica.</span><span class="sxs-lookup"><span data-stu-id="2daee-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="2daee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2daee-110">EXAMPLES</span></span>

### <span data-ttu-id="2daee-111">Exemplo 1: Criar um critério de alerta métrico simples</span><span class="sxs-lookup"><span data-stu-id="2daee-111">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="2daee-112">Este comando cria um critério de alerta métrico simples que pode ser usado em uma regra de alerta métrica</span><span class="sxs-lookup"><span data-stu-id="2daee-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="2daee-113">Exemplo 2: Criar um critério dinâmico de alerta métrico</span><span class="sxs-lookup"><span data-stu-id="2daee-113">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="2daee-114">Este comando cria um critério de alerta métrico dinâmico que pode ser usado em uma regra de alerta métrica</span><span class="sxs-lookup"><span data-stu-id="2daee-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="2daee-115">Exemplo 3: Criar um critério de alerta métrico mais complexo</span><span class="sxs-lookup"><span data-stu-id="2daee-115">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="2daee-116">Esse conjunto de comandos cria um critério de alerta métrico mais complexo que inclui seleção de dimensão</span><span class="sxs-lookup"><span data-stu-id="2daee-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="2daee-117">Exemplo 4: Criar um critério de disponibilidade de teste na Web</span><span class="sxs-lookup"><span data-stu-id="2daee-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="2daee-118">Este comando cria um critério de disponibilidade do webtest que pode ser usado em uma regra de alerta métrica</span><span class="sxs-lookup"><span data-stu-id="2daee-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="2daee-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2daee-119">PARAMETERS</span></span>

### <span data-ttu-id="2daee-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="2daee-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="2daee-121">A ID do recurso Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2daee-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2daee-122">-DefaultProfile</span></span>
<span data-ttu-id="2daee-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2daee-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2daee-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2daee-124">-DimensionSelection</span></span>
<span data-ttu-id="2daee-125">Lista de condições de dimensão</span><span class="sxs-lookup"><span data-stu-id="2daee-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="2daee-126">-DynamicThreshold</span></span>
<span data-ttu-id="2daee-127">Parâmetro Switch para usar o Tipo de Limite Dinâmico</span><span class="sxs-lookup"><span data-stu-id="2daee-127">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="2daee-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="2daee-129">O número total de pontos examinados</span><span class="sxs-lookup"><span data-stu-id="2daee-129">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="2daee-130">-FailedLocationCount</span></span>
<span data-ttu-id="2daee-131">O número mínimo de locais com falha para levantar um alerta.</span><span class="sxs-lookup"><span data-stu-id="2daee-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="2daee-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="2daee-133">O parâmetro IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="2daee-133">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2daee-134">-MetricName</span></span>
<span data-ttu-id="2daee-135">O nome métrico da regra</span><span class="sxs-lookup"><span data-stu-id="2daee-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="2daee-136">-MetricNamespace</span></span>
<span data-ttu-id="2daee-137">O Namespace da métrica</span><span class="sxs-lookup"><span data-stu-id="2daee-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="2daee-138">-Operator</span></span>
<span data-ttu-id="2daee-139">O operador de condição de regra</span><span class="sxs-lookup"><span data-stu-id="2daee-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="2daee-140">-SkipMetricValidation</span></span>
<span data-ttu-id="2daee-141">Permite criar uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação métrica seja ignorada</span><span class="sxs-lookup"><span data-stu-id="2daee-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-142">-Threshold</span><span class="sxs-lookup"><span data-stu-id="2daee-142">-Threshold</span></span>
<span data-ttu-id="2daee-143">O limite para a condição de regra</span><span class="sxs-lookup"><span data-stu-id="2daee-143">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="2daee-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="2daee-145">A sensibilidade para a condição de regra</span><span class="sxs-lookup"><span data-stu-id="2daee-145">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="2daee-146">-TimeAggregation</span></span>
<span data-ttu-id="2daee-147">A operação de agregação usada para rolar vários valores métricos no intervalo da janela</span><span class="sxs-lookup"><span data-stu-id="2daee-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="2daee-148">-ViolationCount</span></span>
<span data-ttu-id="2daee-149">O número mínimo de violações necessárias na janela de tempo de retorno selecionado necessária para levantar um alerta</span><span class="sxs-lookup"><span data-stu-id="2daee-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="2daee-150">-WebTest</span></span>
<span data-ttu-id="2daee-151">Parâmetro Switch para usar o tipo de critérios de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="2daee-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="2daee-152">-WebTestId</span></span>
<span data-ttu-id="2daee-153">A ID de teste web do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2daee-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2daee-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2daee-154">CommonParameters</span></span>
<span data-ttu-id="2daee-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2daee-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2daee-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2daee-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2daee-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2daee-157">INPUTS</span></span>

### <span data-ttu-id="2daee-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="2daee-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="2daee-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2daee-159">OUTPUTS</span></span>

### <span data-ttu-id="2daee-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="2daee-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="2daee-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="2daee-161">NOTES</span></span>

## <span data-ttu-id="2daee-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2daee-162">RELATED LINKS</span></span>
