---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 6e50269e98a942d425f914eed5cc0a75938d0e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940409"
---
# <span data-ttu-id="e6ac1-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e6ac1-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="e6ac1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ac1-103">Cria um objeto de critério local que pode ser usado para criar um novo alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="e6ac1-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="e6ac1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6ac1-104">SYNTAX</span></span>

### <span data-ttu-id="e6ac1-105">StaticThresholdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6ac1-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6ac1-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6ac1-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6ac1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6ac1-107">DESCRIPTION</span></span>
<span data-ttu-id="e6ac1-108">O cmdlet **New-AzMetricAlertRuleV2Criteria** cria um objeto de critérios métrico local a ser usado como um cmdlet Add-AzMetricAlertRuleV2 de entrada, que cria uma nova regra de alerta de métrica.</span><span class="sxs-lookup"><span data-stu-id="e6ac1-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="e6ac1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6ac1-109">EXAMPLES</span></span>

### <span data-ttu-id="e6ac1-110">Exemplo 1: criar um critério simples de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="e6ac1-110">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="e6ac1-111">Esse comando cria um critério simples de alerta de métrica que pode ser usado em uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="e6ac1-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="e6ac1-112">Exemplo 2: criar um critério de alerta de métrica dinâmica</span><span class="sxs-lookup"><span data-stu-id="e6ac1-112">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="e6ac1-113">Esse comando cria um critério de alerta de métrica dinâmica que pode ser usado em uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="e6ac1-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="e6ac1-114">Exemplo 3: criar um critério de alerta métrico mais complexo</span><span class="sxs-lookup"><span data-stu-id="e6ac1-114">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="e6ac1-115">Esse conjunto de comandos cria um critério de alerta métrico mais complexo que inclui a seleção de dimensão</span><span class="sxs-lookup"><span data-stu-id="e6ac1-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="e6ac1-116">OS</span><span class="sxs-lookup"><span data-stu-id="e6ac1-116">PARAMETERS</span></span>

### <span data-ttu-id="e6ac1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ac1-117">-DefaultProfile</span></span>
<span data-ttu-id="e6ac1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ac1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ac1-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e6ac1-119">-DimensionSelection</span></span>
<span data-ttu-id="e6ac1-120">Lista de condições de dimensão</span><span class="sxs-lookup"><span data-stu-id="e6ac1-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ac1-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="e6ac1-121">-DynamicThreshold</span></span>
<span data-ttu-id="e6ac1-122">Parâmetro de opção para usar o tipo de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="e6ac1-122">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="e6ac1-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="e6ac1-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="e6ac1-124">O número total de pontos examinados</span><span class="sxs-lookup"><span data-stu-id="e6ac1-124">The Total number of examined points</span></span>

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

### <span data-ttu-id="e6ac1-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="e6ac1-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="e6ac1-126">O parâmetro IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="e6ac1-126">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="e6ac1-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="e6ac1-127">-MetricName</span></span>
<span data-ttu-id="e6ac1-128">O nome da métrica para a regra</span><span class="sxs-lookup"><span data-stu-id="e6ac1-128">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ac1-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="e6ac1-129">-MetricNamespace</span></span>
<span data-ttu-id="e6ac1-130">O namespace da métrica</span><span class="sxs-lookup"><span data-stu-id="e6ac1-130">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ac1-131">-Operador</span><span class="sxs-lookup"><span data-stu-id="e6ac1-131">-Operator</span></span>
<span data-ttu-id="e6ac1-132">O operador de condição da regra</span><span class="sxs-lookup"><span data-stu-id="e6ac1-132">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ac1-133">-Threshold</span><span class="sxs-lookup"><span data-stu-id="e6ac1-133">-Threshold</span></span>
<span data-ttu-id="e6ac1-134">O limite para a condição da regra</span><span class="sxs-lookup"><span data-stu-id="e6ac1-134">The threshold for rule condition</span></span>

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

### <span data-ttu-id="e6ac1-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="e6ac1-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="e6ac1-136">A sensibilidade para a condição da regra</span><span class="sxs-lookup"><span data-stu-id="e6ac1-136">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="e6ac1-137">-Agregação de TimeSerial</span><span class="sxs-lookup"><span data-stu-id="e6ac1-137">-TimeAggregation</span></span>
<span data-ttu-id="e6ac1-138">A operação de agregação usada para acumular vários valores métricos ao longo do intervalo de janela</span><span class="sxs-lookup"><span data-stu-id="e6ac1-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ac1-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="e6ac1-139">-ViolationCount</span></span>
<span data-ttu-id="e6ac1-140">O número mínimo de violações necessárias dentro da janela de tempo do lookback selecionada necessária para acionar um alerta</span><span class="sxs-lookup"><span data-stu-id="e6ac1-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="e6ac1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ac1-141">CommonParameters</span></span>
<span data-ttu-id="e6ac1-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ac1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ac1-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6ac1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ac1-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6ac1-144">INPUTS</span></span>

### <span data-ttu-id="e6ac1-145">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="e6ac1-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="e6ac1-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6ac1-146">OUTPUTS</span></span>

### <span data-ttu-id="e6ac1-147">Microsoft. Azure. Commands. insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="e6ac1-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="e6ac1-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6ac1-148">NOTES</span></span>

## <span data-ttu-id="e6ac1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6ac1-149">RELATED LINKS</span></span>
