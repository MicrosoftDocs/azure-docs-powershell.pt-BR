---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: ccc81854cf2f1075a6973fa8ed4685faba713a2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772171"
---
# <span data-ttu-id="c51ae-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="c51ae-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="c51ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c51ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c51ae-103">Cria um objeto do tipo de condição disparador</span><span class="sxs-lookup"><span data-stu-id="c51ae-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="c51ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c51ae-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c51ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c51ae-105">DESCRIPTION</span></span>
<span data-ttu-id="c51ae-106">Cria um objeto do tipo de condição disparador.</span><span class="sxs-lookup"><span data-stu-id="c51ae-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="c51ae-107">Esse objeto deve ser passado para o comando que cria o objeto Action de alerta</span><span class="sxs-lookup"><span data-stu-id="c51ae-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="c51ae-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c51ae-108">EXAMPLES</span></span>

### <span data-ttu-id="c51ae-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c51ae-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="c51ae-110">OS</span><span class="sxs-lookup"><span data-stu-id="c51ae-110">PARAMETERS</span></span>

### <span data-ttu-id="c51ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51ae-111">-DefaultProfile</span></span>
<span data-ttu-id="c51ae-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c51ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c51ae-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="c51ae-113">-MetricTrigger</span></span>
<span data-ttu-id="c51ae-114">Condição de gatilho para a regra de consulta métrica</span><span class="sxs-lookup"><span data-stu-id="c51ae-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51ae-115">-Threshold</span><span class="sxs-lookup"><span data-stu-id="c51ae-115">-Threshold</span></span>
<span data-ttu-id="c51ae-116">O limite acima do qual o alerta é acionado</span><span class="sxs-lookup"><span data-stu-id="c51ae-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="c51ae-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="c51ae-117">-ThresholdOperator</span></span>
<span data-ttu-id="c51ae-118">O operador Threshold: GreaterThan, LessThan ou Equals</span><span class="sxs-lookup"><span data-stu-id="c51ae-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="c51ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51ae-119">CommonParameters</span></span>
<span data-ttu-id="c51ae-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c51ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51ae-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c51ae-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51ae-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c51ae-122">INPUTS</span></span>

### <span data-ttu-id="c51ae-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c51ae-123">None</span></span>

## <span data-ttu-id="c51ae-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c51ae-124">OUTPUTS</span></span>

### <span data-ttu-id="c51ae-125">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="c51ae-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="c51ae-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c51ae-126">NOTES</span></span>

## <span data-ttu-id="c51ae-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c51ae-127">RELATED LINKS</span></span>
