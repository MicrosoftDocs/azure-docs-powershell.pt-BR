---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c5fb336d7ba105469506bb0a80a5b69036e5474b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775704"
---
# <span data-ttu-id="7ca69-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7ca69-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="7ca69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ca69-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca69-103">Cria um objeto do tipo gatilho de métrica de log</span><span class="sxs-lookup"><span data-stu-id="7ca69-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="7ca69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ca69-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ca69-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ca69-105">DESCRIPTION</span></span>
<span data-ttu-id="7ca69-106">Cria um objeto do tipo gatilho de métrica de log e é opcional.</span><span class="sxs-lookup"><span data-stu-id="7ca69-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="7ca69-107">Esta é a condição de disparo para a regra de consulta métrica, a ser usada quando você precisar declarar o tipo de medição da métrica tipo de alerta.</span><span class="sxs-lookup"><span data-stu-id="7ca69-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="7ca69-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ca69-108">EXAMPLES</span></span>

### <span data-ttu-id="7ca69-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ca69-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="7ca69-110">OS</span><span class="sxs-lookup"><span data-stu-id="7ca69-110">PARAMETERS</span></span>

### <span data-ttu-id="7ca69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca69-111">-DefaultProfile</span></span>
<span data-ttu-id="7ca69-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca69-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca69-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="7ca69-113">-MetricColumn</span></span>
<span data-ttu-id="7ca69-114">Coluna na qual o valor métrico está sendo agregado</span><span class="sxs-lookup"><span data-stu-id="7ca69-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="7ca69-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="7ca69-115">-MetricTriggerType</span></span>
<span data-ttu-id="7ca69-116">O tipo de gatilho de métrica</span><span class="sxs-lookup"><span data-stu-id="7ca69-116">The metric trigger type</span></span>

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

### <span data-ttu-id="7ca69-117">-Threshold</span><span class="sxs-lookup"><span data-stu-id="7ca69-117">-Threshold</span></span>
<span data-ttu-id="7ca69-118">O valor de limite métrico</span><span class="sxs-lookup"><span data-stu-id="7ca69-118">The metric threshold value</span></span>

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

### <span data-ttu-id="7ca69-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="7ca69-119">-ThresholdOperator</span></span>
<span data-ttu-id="7ca69-120">A operadora de limite métrico: GreaterThan, LessThan, igual</span><span class="sxs-lookup"><span data-stu-id="7ca69-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="7ca69-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca69-121">CommonParameters</span></span>
<span data-ttu-id="7ca69-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ca69-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca69-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ca69-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca69-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ca69-124">INPUTS</span></span>

### <span data-ttu-id="7ca69-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7ca69-125">None</span></span>

## <span data-ttu-id="7ca69-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ca69-126">OUTPUTS</span></span>

### <span data-ttu-id="7ca69-127">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7ca69-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="7ca69-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ca69-128">NOTES</span></span>

## <span data-ttu-id="7ca69-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ca69-129">RELATED LINKS</span></span>
