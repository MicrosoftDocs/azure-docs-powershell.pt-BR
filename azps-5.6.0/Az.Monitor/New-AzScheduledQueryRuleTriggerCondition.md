---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 1fcafb0eb9e4bd1cfb0cf5b3f5ec770c35ea92d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891178"
---
# <span data-ttu-id="b50d8-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="b50d8-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="b50d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b50d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b50d8-103">Cria um objeto do tipo Condição de Gatilho</span><span class="sxs-lookup"><span data-stu-id="b50d8-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="b50d8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b50d8-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b50d8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b50d8-105">DESCRIPTION</span></span>
<span data-ttu-id="b50d8-106">Cria um objeto do tipo Condição de Gatilho.</span><span class="sxs-lookup"><span data-stu-id="b50d8-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="b50d8-107">Esse objeto deve ser passado para o comando que cria o objeto Ação de Alerta</span><span class="sxs-lookup"><span data-stu-id="b50d8-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="b50d8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b50d8-108">EXAMPLES</span></span>

### <span data-ttu-id="b50d8-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b50d8-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="b50d8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b50d8-110">PARAMETERS</span></span>

### <span data-ttu-id="b50d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50d8-111">-DefaultProfile</span></span>
<span data-ttu-id="b50d8-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b50d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50d8-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="b50d8-113">-MetricTrigger</span></span>
<span data-ttu-id="b50d8-114">Condição de gatilho para regra de consulta métrica</span><span class="sxs-lookup"><span data-stu-id="b50d8-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="b50d8-115">-Threshold</span><span class="sxs-lookup"><span data-stu-id="b50d8-115">-Threshold</span></span>
<span data-ttu-id="b50d8-116">O limite acima do qual o alerta é disparado</span><span class="sxs-lookup"><span data-stu-id="b50d8-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="b50d8-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="b50d8-117">-ThresholdOperator</span></span>
<span data-ttu-id="b50d8-118">O operador de limite : GreaterThan, LessThan ou Equal</span><span class="sxs-lookup"><span data-stu-id="b50d8-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="b50d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50d8-119">CommonParameters</span></span>
<span data-ttu-id="b50d8-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b50d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50d8-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b50d8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50d8-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b50d8-122">INPUTS</span></span>

### <span data-ttu-id="b50d8-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b50d8-123">None</span></span>

## <span data-ttu-id="b50d8-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b50d8-124">OUTPUTS</span></span>

### <span data-ttu-id="b50d8-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="b50d8-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="b50d8-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="b50d8-126">NOTES</span></span>

## <span data-ttu-id="b50d8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b50d8-127">RELATED LINKS</span></span>
