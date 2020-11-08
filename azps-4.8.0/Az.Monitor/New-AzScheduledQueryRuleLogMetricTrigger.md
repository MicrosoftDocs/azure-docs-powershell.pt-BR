---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111799"
---
# <span data-ttu-id="7e119-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7e119-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="7e119-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e119-102">SYNOPSIS</span></span>
<span data-ttu-id="7e119-103">Cria um objeto do tipo gatilho de métrica de log.</span><span class="sxs-lookup"><span data-stu-id="7e119-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="7e119-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e119-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e119-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e119-105">DESCRIPTION</span></span>
<span data-ttu-id="7e119-106">Cria um objeto do tipo gatilho de métrica de log e é opcional.</span><span class="sxs-lookup"><span data-stu-id="7e119-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="7e119-107">Esta é a condição de disparo para a regra de consulta métrica, a ser usada quando você precisar declarar o tipo de medição da métrica tipo de alerta.</span><span class="sxs-lookup"><span data-stu-id="7e119-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="7e119-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e119-108">EXAMPLES</span></span>

### <span data-ttu-id="7e119-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e119-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="7e119-110">OS</span><span class="sxs-lookup"><span data-stu-id="7e119-110">PARAMETERS</span></span>

### <span data-ttu-id="7e119-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e119-111">-DefaultProfile</span></span>
<span data-ttu-id="7e119-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e119-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e119-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="7e119-113">-MetricColumn</span></span>
<span data-ttu-id="7e119-114">Coluna na qual o valor métrico está sendo agregado.</span><span class="sxs-lookup"><span data-stu-id="7e119-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="7e119-115">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="7e119-115">The input is not validated.</span></span> <span data-ttu-id="7e119-116">Ele será validado primeiro quando New-AzScheduledQueryRule for eventualmente chamado.</span><span class="sxs-lookup"><span data-stu-id="7e119-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="7e119-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="7e119-117">-MetricTriggerType</span></span>
<span data-ttu-id="7e119-118">O tipo de gatilho de métrica.</span><span class="sxs-lookup"><span data-stu-id="7e119-118">The metric trigger type.</span></span>
<span data-ttu-id="7e119-119">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="7e119-119">The input is not validated.</span></span> <span data-ttu-id="7e119-120">Ele será validado primeiro quando New-AzScheduledQueryRule for eventualmente chamado.</span><span class="sxs-lookup"><span data-stu-id="7e119-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="7e119-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="7e119-121">-Threshold</span></span>
<span data-ttu-id="7e119-122">O valor de limite métrico: consecutivo, total.</span><span class="sxs-lookup"><span data-stu-id="7e119-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="7e119-123">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="7e119-123">The input is not validated.</span></span> <span data-ttu-id="7e119-124">Ele será validado primeiro quando New-AzScheduledQueryRule for eventualmente chamado.</span><span class="sxs-lookup"><span data-stu-id="7e119-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e119-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="7e119-125">-ThresholdOperator</span></span>
<span data-ttu-id="7e119-126">O limite de métrica Operator: GreaterThan, LessThan, Equals.</span><span class="sxs-lookup"><span data-stu-id="7e119-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="7e119-127">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="7e119-127">The input is not validated.</span></span> <span data-ttu-id="7e119-128">Ele será validado primeiro quando New-AzScheduledQueryRule for eventualmente chamado.</span><span class="sxs-lookup"><span data-stu-id="7e119-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="7e119-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e119-129">CommonParameters</span></span>
<span data-ttu-id="7e119-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e119-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e119-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e119-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e119-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e119-132">INPUTS</span></span>

### <span data-ttu-id="7e119-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7e119-133">None</span></span>

## <span data-ttu-id="7e119-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e119-134">OUTPUTS</span></span>

### <span data-ttu-id="7e119-135">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7e119-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="7e119-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e119-136">NOTES</span></span>

## <span data-ttu-id="7e119-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e119-137">RELATED LINKS</span></span>
