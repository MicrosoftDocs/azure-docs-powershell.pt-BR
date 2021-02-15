---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111747"
---
# <span data-ttu-id="a3da7-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a3da7-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="a3da7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3da7-102">SYNOPSIS</span></span>
<span data-ttu-id="a3da7-103">Cria um objeto do tipo Condição de Gatilho</span><span class="sxs-lookup"><span data-stu-id="a3da7-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="a3da7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3da7-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3da7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3da7-105">DESCRIPTION</span></span>
<span data-ttu-id="a3da7-106">Cria um objeto do tipo Condição de Gatilho.</span><span class="sxs-lookup"><span data-stu-id="a3da7-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="a3da7-107">Esse objeto deve ser passado para o comando que cria o objeto Ação de Alerta</span><span class="sxs-lookup"><span data-stu-id="a3da7-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="a3da7-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3da7-108">EXAMPLES</span></span>

### <span data-ttu-id="a3da7-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3da7-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="a3da7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3da7-110">PARAMETERS</span></span>

### <span data-ttu-id="a3da7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3da7-111">-DefaultProfile</span></span>
<span data-ttu-id="a3da7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3da7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3da7-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a3da7-113">-MetricTrigger</span></span>
<span data-ttu-id="a3da7-114">Condição de acionamento para a regra de consulta métrica</span><span class="sxs-lookup"><span data-stu-id="a3da7-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="a3da7-115">-Limite</span><span class="sxs-lookup"><span data-stu-id="a3da7-115">-Threshold</span></span>
<span data-ttu-id="a3da7-116">O limite acima do qual o alerta é disparado</span><span class="sxs-lookup"><span data-stu-id="a3da7-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="a3da7-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="a3da7-117">-ThresholdOperator</span></span>
<span data-ttu-id="a3da7-118">O operador limite: GreaterThan, LessThan ou Equal</span><span class="sxs-lookup"><span data-stu-id="a3da7-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="a3da7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3da7-119">CommonParameters</span></span>
<span data-ttu-id="a3da7-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3da7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3da7-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3da7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3da7-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="a3da7-122">INPUTS</span></span>

### <span data-ttu-id="a3da7-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a3da7-123">None</span></span>

## <span data-ttu-id="a3da7-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="a3da7-124">OUTPUTS</span></span>

### <span data-ttu-id="a3da7-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a3da7-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="a3da7-126">Notas</span><span class="sxs-lookup"><span data-stu-id="a3da7-126">NOTES</span></span>

## <span data-ttu-id="a3da7-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3da7-127">RELATED LINKS</span></span>
