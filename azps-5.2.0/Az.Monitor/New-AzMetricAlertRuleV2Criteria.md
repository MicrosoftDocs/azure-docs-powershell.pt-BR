---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257977"
---
# <span data-ttu-id="cc16c-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cc16c-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="cc16c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc16c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc16c-103">Cria um objeto de critério local que pode ser usado para criar um novo alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="cc16c-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="cc16c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc16c-104">SYNTAX</span></span>

### <span data-ttu-id="cc16c-105">StaticThresholdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc16c-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc16c-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc16c-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc16c-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc16c-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc16c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc16c-108">DESCRIPTION</span></span>
<span data-ttu-id="cc16c-109">O cmdlet **New-AzMetricAlertRuleV2Criteria** cria um objeto de critérios métrico local para ser usado como um cmdlet [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) de entrada que cria uma nova regra de alerta de métrica.</span><span class="sxs-lookup"><span data-stu-id="cc16c-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="cc16c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc16c-110">EXAMPLES</span></span>

### <span data-ttu-id="cc16c-111">Exemplo 1: criar um critério simples de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="cc16c-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="cc16c-112">Esse comando cria um critério simples de alerta de métrica que pode ser usado em uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="cc16c-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="cc16c-113">Exemplo 2: criar um critério de alerta de métrica dinâmica</span><span class="sxs-lookup"><span data-stu-id="cc16c-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="cc16c-114">Esse comando cria um critério de alerta de métrica dinâmica que pode ser usado em uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="cc16c-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="cc16c-115">Exemplo 3: criar um critério de alerta métrico mais complexo</span><span class="sxs-lookup"><span data-stu-id="cc16c-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="cc16c-116">Esse conjunto de comandos cria um critério de alerta métrico mais complexo que inclui a seleção de dimensão</span><span class="sxs-lookup"><span data-stu-id="cc16c-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="cc16c-117">Exemplo 4: criar um critério de disponibilidade do WebTest</span><span class="sxs-lookup"><span data-stu-id="cc16c-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="cc16c-118">Esse comando cria um critério de disponibilidade de WebTest que pode ser usado em uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="cc16c-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="cc16c-119">OS</span><span class="sxs-lookup"><span data-stu-id="cc16c-119">PARAMETERS</span></span>

### <span data-ttu-id="cc16c-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="cc16c-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="cc16c-121">A ID do recurso insights do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cc16c-121">The Application Insights resource Id.</span></span>

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

### <span data-ttu-id="cc16c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc16c-122">-DefaultProfile</span></span>
<span data-ttu-id="cc16c-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc16c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc16c-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cc16c-124">-DimensionSelection</span></span>
<span data-ttu-id="cc16c-125">Lista de condições de dimensão</span><span class="sxs-lookup"><span data-stu-id="cc16c-125">List of dimension conditions</span></span>

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

### <span data-ttu-id="cc16c-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="cc16c-126">-DynamicThreshold</span></span>
<span data-ttu-id="cc16c-127">Parâmetro de opção para usar o tipo de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="cc16c-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="cc16c-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="cc16c-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="cc16c-129">O número total de pontos examinados</span><span class="sxs-lookup"><span data-stu-id="cc16c-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="cc16c-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="cc16c-130">-FailedLocationCount</span></span>
<span data-ttu-id="cc16c-131">O número mínimo de locais com falha para gerar um alerta.</span><span class="sxs-lookup"><span data-stu-id="cc16c-131">The minimum number of failed locations to raise an alert.</span></span>

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

### <span data-ttu-id="cc16c-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="cc16c-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="cc16c-133">O parâmetro IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="cc16c-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="cc16c-134">-Metricname</span><span class="sxs-lookup"><span data-stu-id="cc16c-134">-MetricName</span></span>
<span data-ttu-id="cc16c-135">O nome da métrica para a regra</span><span class="sxs-lookup"><span data-stu-id="cc16c-135">The metric name for rule</span></span>

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

### <span data-ttu-id="cc16c-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="cc16c-136">-MetricNamespace</span></span>
<span data-ttu-id="cc16c-137">O namespace da métrica</span><span class="sxs-lookup"><span data-stu-id="cc16c-137">The Namespace of the metric</span></span>

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

### <span data-ttu-id="cc16c-138">-Operador</span><span class="sxs-lookup"><span data-stu-id="cc16c-138">-Operator</span></span>
<span data-ttu-id="cc16c-139">O operador de condição da regra</span><span class="sxs-lookup"><span data-stu-id="cc16c-139">The rule condition operator</span></span>

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

### <span data-ttu-id="cc16c-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="cc16c-140">-SkipMetricValidation</span></span>
<span data-ttu-id="cc16c-141">Permite a criação de uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação métrica seja ignorada</span><span class="sxs-lookup"><span data-stu-id="cc16c-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

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

### <span data-ttu-id="cc16c-142">-Threshold</span><span class="sxs-lookup"><span data-stu-id="cc16c-142">-Threshold</span></span>
<span data-ttu-id="cc16c-143">O limite para a condição da regra</span><span class="sxs-lookup"><span data-stu-id="cc16c-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="cc16c-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="cc16c-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="cc16c-145">A sensibilidade para a condição da regra</span><span class="sxs-lookup"><span data-stu-id="cc16c-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="cc16c-146">-Agregação de TimeSerial</span><span class="sxs-lookup"><span data-stu-id="cc16c-146">-TimeAggregation</span></span>
<span data-ttu-id="cc16c-147">A operação de agregação usada para acumular vários valores métricos ao longo do intervalo de janela</span><span class="sxs-lookup"><span data-stu-id="cc16c-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="cc16c-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="cc16c-148">-ViolationCount</span></span>
<span data-ttu-id="cc16c-149">O número mínimo de violações necessárias dentro da janela de tempo do lookback selecionada necessária para acionar um alerta</span><span class="sxs-lookup"><span data-stu-id="cc16c-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="cc16c-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="cc16c-150">-WebTest</span></span>
<span data-ttu-id="cc16c-151">Parâmetro de alternância para usar o tipo de critérios de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="cc16c-151">Switch parameter for using availability criteria Type</span></span>

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

### <span data-ttu-id="cc16c-152">-Webtestid</span><span class="sxs-lookup"><span data-stu-id="cc16c-152">-WebTestId</span></span>
<span data-ttu-id="cc16c-153">A ID do teste da Web do Application insights.</span><span class="sxs-lookup"><span data-stu-id="cc16c-153">The Application Insights web test Id.</span></span>

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

### <span data-ttu-id="cc16c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc16c-154">CommonParameters</span></span>
<span data-ttu-id="cc16c-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc16c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc16c-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc16c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc16c-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc16c-157">INPUTS</span></span>

### <span data-ttu-id="cc16c-158">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="cc16c-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="cc16c-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc16c-159">OUTPUTS</span></span>

### <span data-ttu-id="cc16c-160">Microsoft. Azure. Commands. insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="cc16c-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="cc16c-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc16c-161">NOTES</span></span>

## <span data-ttu-id="cc16c-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc16c-162">RELATED LINKS</span></span>
