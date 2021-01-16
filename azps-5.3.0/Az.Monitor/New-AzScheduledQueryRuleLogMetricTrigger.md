---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428246"
---
# <span data-ttu-id="f88ef-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f88ef-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="f88ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f88ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f88ef-103">Cria um objeto do tipo gatilho de métrica de log.</span><span class="sxs-lookup"><span data-stu-id="f88ef-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="f88ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f88ef-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f88ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f88ef-105">DESCRIPTION</span></span>
<span data-ttu-id="f88ef-106">Cria um objeto do tipo gatilho de métrica de log e é opcional.</span><span class="sxs-lookup"><span data-stu-id="f88ef-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="f88ef-107">Esta é a condição de disparo para a regra de consulta métrica, a ser usada quando você precisar declarar o tipo de medição da métrica tipo de alerta.</span><span class="sxs-lookup"><span data-stu-id="f88ef-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="f88ef-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f88ef-108">EXAMPLES</span></span>

### <span data-ttu-id="f88ef-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f88ef-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="f88ef-110">OS</span><span class="sxs-lookup"><span data-stu-id="f88ef-110">PARAMETERS</span></span>

### <span data-ttu-id="f88ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88ef-111">-DefaultProfile</span></span>
<span data-ttu-id="f88ef-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f88ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f88ef-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="f88ef-113">-MetricColumn</span></span>
<span data-ttu-id="f88ef-114">Coluna na qual o valor métrico está sendo agregado.</span><span class="sxs-lookup"><span data-stu-id="f88ef-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="f88ef-115">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="f88ef-115">The input is not validated.</span></span> <span data-ttu-id="f88ef-116">Ele será validado primeiro quando New-AzScheduledQueryRule for eventualmente chamado.</span><span class="sxs-lookup"><span data-stu-id="f88ef-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="f88ef-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="f88ef-117">-MetricTriggerType</span></span>
<span data-ttu-id="f88ef-118">O tipo de gatilho de métrica.</span><span class="sxs-lookup"><span data-stu-id="f88ef-118">The metric trigger type.</span></span>
<span data-ttu-id="f88ef-119">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="f88ef-119">The input is not validated.</span></span> <span data-ttu-id="f88ef-120">Ele será validado primeiro quando New-AzScheduledQueryRule for eventualmente chamado.</span><span class="sxs-lookup"><span data-stu-id="f88ef-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="f88ef-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="f88ef-121">-Threshold</span></span>
<span data-ttu-id="f88ef-122">O valor de limite métrico: consecutivo, total.</span><span class="sxs-lookup"><span data-stu-id="f88ef-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="f88ef-123">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="f88ef-123">The input is not validated.</span></span> <span data-ttu-id="f88ef-124">Ele será validado primeiro quando New-AzScheduledQueryRule for eventualmente chamado.</span><span class="sxs-lookup"><span data-stu-id="f88ef-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="f88ef-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="f88ef-125">-ThresholdOperator</span></span>
<span data-ttu-id="f88ef-126">O limite de métrica Operator: GreaterThan, LessThan, Equals.</span><span class="sxs-lookup"><span data-stu-id="f88ef-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="f88ef-127">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="f88ef-127">The input is not validated.</span></span> <span data-ttu-id="f88ef-128">Ele será validado primeiro quando New-AzScheduledQueryRule for eventualmente chamado.</span><span class="sxs-lookup"><span data-stu-id="f88ef-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="f88ef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88ef-129">CommonParameters</span></span>
<span data-ttu-id="f88ef-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88ef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88ef-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f88ef-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88ef-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f88ef-132">INPUTS</span></span>

### <span data-ttu-id="f88ef-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f88ef-133">None</span></span>

## <span data-ttu-id="f88ef-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f88ef-134">OUTPUTS</span></span>

### <span data-ttu-id="f88ef-135">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f88ef-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="f88ef-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f88ef-136">NOTES</span></span>

## <span data-ttu-id="f88ef-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f88ef-137">RELATED LINKS</span></span>
