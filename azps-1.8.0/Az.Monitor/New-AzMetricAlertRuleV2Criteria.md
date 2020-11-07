---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770296"
---
# <span data-ttu-id="fc16d-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="fc16d-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="fc16d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc16d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc16d-103">Cria um objeto de critério local que pode ser usado para criar um novo alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="fc16d-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="fc16d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc16d-104">SYNTAX</span></span>

### <span data-ttu-id="fc16d-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc16d-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc16d-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc16d-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc16d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc16d-107">DESCRIPTION</span></span>
<span data-ttu-id="fc16d-108">O cmdlet **New-AzMetricAlertRuleV2Criteria** cria um objeto de critérios métrico local a ser usado como um cmdlet Add-AzMetricAlertRuleV2 de entrada, que cria uma nova regra de alerta de métrica.</span><span class="sxs-lookup"><span data-stu-id="fc16d-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="fc16d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc16d-109">EXAMPLES</span></span>

### <span data-ttu-id="fc16d-110">Exemplo 1: criar um critério simples de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="fc16d-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="fc16d-111">Esse comando cria um critério simples de alerta de métrica que pode ser usado em uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="fc16d-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="fc16d-112">Exemplo 2: criar um critério de alerta métrico mais complexo</span><span class="sxs-lookup"><span data-stu-id="fc16d-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="fc16d-113">Esse conjunto de comandos cria um critério de alerta métrico mais complexo que inclui a seleção de dimensão</span><span class="sxs-lookup"><span data-stu-id="fc16d-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="fc16d-114">OS</span><span class="sxs-lookup"><span data-stu-id="fc16d-114">PARAMETERS</span></span>

### <span data-ttu-id="fc16d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc16d-115">-DefaultProfile</span></span>
<span data-ttu-id="fc16d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc16d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="fc16d-117">-DimensionSelection</span></span>
<span data-ttu-id="fc16d-118">Lista de condições de dimensão</span><span class="sxs-lookup"><span data-stu-id="fc16d-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="fc16d-119">-DynamicThreshold</span></span>
<span data-ttu-id="fc16d-120">O limite dinâmico para a condição da regra</span><span class="sxs-lookup"><span data-stu-id="fc16d-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="fc16d-121">-FailingPeriod</span></span>
<span data-ttu-id="fc16d-122">O período de falha para a condição da regra</span><span class="sxs-lookup"><span data-stu-id="fc16d-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="fc16d-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="fc16d-124">O parâmetro IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="fc16d-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-125">-Metricname</span><span class="sxs-lookup"><span data-stu-id="fc16d-125">-MetricName</span></span>
<span data-ttu-id="fc16d-126">O nome da métrica para a regra</span><span class="sxs-lookup"><span data-stu-id="fc16d-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="fc16d-127">-MetricNamespace</span></span>
<span data-ttu-id="fc16d-128">O namespace da métrica</span><span class="sxs-lookup"><span data-stu-id="fc16d-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-129">-Operador</span><span class="sxs-lookup"><span data-stu-id="fc16d-129">-Operator</span></span>
<span data-ttu-id="fc16d-130">O operador de condição da regra</span><span class="sxs-lookup"><span data-stu-id="fc16d-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-131">-Sensibilidade</span><span class="sxs-lookup"><span data-stu-id="fc16d-131">-Sensitivity</span></span>
<span data-ttu-id="fc16d-132">A sensibilidade para a condição da regra</span><span class="sxs-lookup"><span data-stu-id="fc16d-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-133">-Threshold</span><span class="sxs-lookup"><span data-stu-id="fc16d-133">-Threshold</span></span>
<span data-ttu-id="fc16d-134">O limite para a condição da regra</span><span class="sxs-lookup"><span data-stu-id="fc16d-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-135">-Agregação de TimeSerial</span><span class="sxs-lookup"><span data-stu-id="fc16d-135">-TimeAggregation</span></span>
<span data-ttu-id="fc16d-136">A operação de agregação usada para acumular vários valores métricos ao longo do intervalo de janela</span><span class="sxs-lookup"><span data-stu-id="fc16d-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="fc16d-137">-TotalPeriod</span></span>
<span data-ttu-id="fc16d-138">O período total para a condição de regra</span><span class="sxs-lookup"><span data-stu-id="fc16d-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc16d-139">CommonParameters</span></span>
<span data-ttu-id="fc16d-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc16d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fc16d-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc16d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc16d-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc16d-142">INPUTS</span></span>

### <span data-ttu-id="fc16d-143">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="fc16d-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="fc16d-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc16d-144">OUTPUTS</span></span>

### <span data-ttu-id="fc16d-145">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="fc16d-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="fc16d-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc16d-146">NOTES</span></span>

## <span data-ttu-id="fc16d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc16d-147">RELATED LINKS</span></span>
