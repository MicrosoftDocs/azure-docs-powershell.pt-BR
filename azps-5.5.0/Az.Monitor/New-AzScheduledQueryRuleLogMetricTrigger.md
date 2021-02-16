---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113564"
---
# <span data-ttu-id="f703a-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f703a-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="f703a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f703a-102">SYNOPSIS</span></span>
<span data-ttu-id="f703a-103">Cria um objeto do tipo Gatilho Métrico de Log.</span><span class="sxs-lookup"><span data-stu-id="f703a-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="f703a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f703a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f703a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f703a-105">DESCRIPTION</span></span>
<span data-ttu-id="f703a-106">Cria um objeto do tipo Gatilho Métrico de Log e é opcional.</span><span class="sxs-lookup"><span data-stu-id="f703a-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="f703a-107">Essa é a condição de acionamento para a regra de consulta métrica, a ser usada quando você precisar estado tipo de alerta de medida métrica.</span><span class="sxs-lookup"><span data-stu-id="f703a-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="f703a-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f703a-108">EXAMPLES</span></span>

### <span data-ttu-id="f703a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f703a-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="f703a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f703a-110">PARAMETERS</span></span>

### <span data-ttu-id="f703a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f703a-111">-DefaultProfile</span></span>
<span data-ttu-id="f703a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f703a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f703a-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="f703a-113">-MetricColumn</span></span>
<span data-ttu-id="f703a-114">Coluna na qual o valor métrico está sendo agregado.</span><span class="sxs-lookup"><span data-stu-id="f703a-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="f703a-115">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="f703a-115">The input is not validated.</span></span> <span data-ttu-id="f703a-116">Ele será validado primeiro quando o New-AzScheduledQueryRule for chamado.</span><span class="sxs-lookup"><span data-stu-id="f703a-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="f703a-117">-MetricTritype</span><span class="sxs-lookup"><span data-stu-id="f703a-117">-MetricTriggerType</span></span>
<span data-ttu-id="f703a-118">O tipo de gatilho métrico.</span><span class="sxs-lookup"><span data-stu-id="f703a-118">The metric trigger type.</span></span>
<span data-ttu-id="f703a-119">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="f703a-119">The input is not validated.</span></span> <span data-ttu-id="f703a-120">Ele será validado primeiro quando o New-AzScheduledQueryRule for chamado.</span><span class="sxs-lookup"><span data-stu-id="f703a-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="f703a-121">-Limite</span><span class="sxs-lookup"><span data-stu-id="f703a-121">-Threshold</span></span>
<span data-ttu-id="f703a-122">O valor limite da métrica: Consecutiva, Total.</span><span class="sxs-lookup"><span data-stu-id="f703a-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="f703a-123">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="f703a-123">The input is not validated.</span></span> <span data-ttu-id="f703a-124">Ele será validado primeiro quando o New-AzScheduledQueryRule for chamado.</span><span class="sxs-lookup"><span data-stu-id="f703a-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="f703a-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="f703a-125">-ThresholdOperator</span></span>
<span data-ttu-id="f703a-126">O operador de limite métrico: GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="f703a-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="f703a-127">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="f703a-127">The input is not validated.</span></span> <span data-ttu-id="f703a-128">Ele será validado primeiro quando o New-AzScheduledQueryRule for chamado.</span><span class="sxs-lookup"><span data-stu-id="f703a-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="f703a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f703a-129">CommonParameters</span></span>
<span data-ttu-id="f703a-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f703a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f703a-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f703a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f703a-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="f703a-132">INPUTS</span></span>

### <span data-ttu-id="f703a-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f703a-133">None</span></span>

## <span data-ttu-id="f703a-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="f703a-134">OUTPUTS</span></span>

### <span data-ttu-id="f703a-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f703a-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="f703a-136">Notas</span><span class="sxs-lookup"><span data-stu-id="f703a-136">NOTES</span></span>

## <span data-ttu-id="f703a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f703a-137">RELATED LINKS</span></span>
