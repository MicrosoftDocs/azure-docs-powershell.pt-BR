---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 0270c9bf6d543455772095a6d0fe3f0f1a55a416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888689"
---
# <span data-ttu-id="dbf7c-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="dbf7c-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="dbf7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf7c-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf7c-103">Cria um objeto do tipo Gatilho Métrico de Log.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="dbf7c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dbf7c-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbf7c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dbf7c-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf7c-106">Cria um objeto do tipo Gatilho Métrico de Log e é opcional.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="dbf7c-107">Essa é a condição de gatilho para a regra de consulta métrica, a ser usada quando você precisar estado tipo de alerta de medida métrica.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="dbf7c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbf7c-108">EXAMPLES</span></span>

### <span data-ttu-id="dbf7c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dbf7c-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="dbf7c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dbf7c-110">PARAMETERS</span></span>

### <span data-ttu-id="dbf7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf7c-111">-DefaultProfile</span></span>
<span data-ttu-id="dbf7c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf7c-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="dbf7c-113">-MetricColumn</span></span>
<span data-ttu-id="dbf7c-114">Coluna em que valor métrico está sendo agregado.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="dbf7c-115">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-115">The input is not validated.</span></span> <span data-ttu-id="dbf7c-116">Ele será validado pela primeira vez quando New-AzScheduledQueryRule for chamado.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="dbf7c-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="dbf7c-117">-MetricTriggerType</span></span>
<span data-ttu-id="dbf7c-118">O tipo de gatilho métrico.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-118">The metric trigger type.</span></span>
<span data-ttu-id="dbf7c-119">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-119">The input is not validated.</span></span> <span data-ttu-id="dbf7c-120">Ele será validado pela primeira vez quando New-AzScheduledQueryRule for chamado.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="dbf7c-121">-Threshold</span><span class="sxs-lookup"><span data-stu-id="dbf7c-121">-Threshold</span></span>
<span data-ttu-id="dbf7c-122">O valor limite métrico: Consecutivo, Total.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="dbf7c-123">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-123">The input is not validated.</span></span> <span data-ttu-id="dbf7c-124">Ele será validado pela primeira vez quando New-AzScheduledQueryRule for chamado.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="dbf7c-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="dbf7c-125">-ThresholdOperator</span></span>
<span data-ttu-id="dbf7c-126">O operador de limite métrico : GreaterThan, LessThan, Equal.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="dbf7c-127">A entrada não é validada.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-127">The input is not validated.</span></span> <span data-ttu-id="dbf7c-128">Ele será validado pela primeira vez quando New-AzScheduledQueryRule for chamado.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="dbf7c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf7c-129">CommonParameters</span></span>
<span data-ttu-id="dbf7c-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf7c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf7c-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbf7c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf7c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbf7c-132">INPUTS</span></span>

### <span data-ttu-id="dbf7c-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dbf7c-133">None</span></span>

## <span data-ttu-id="dbf7c-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dbf7c-134">OUTPUTS</span></span>

### <span data-ttu-id="dbf7c-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="dbf7c-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="dbf7c-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="dbf7c-136">NOTES</span></span>

## <span data-ttu-id="dbf7c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbf7c-137">RELATED LINKS</span></span>
