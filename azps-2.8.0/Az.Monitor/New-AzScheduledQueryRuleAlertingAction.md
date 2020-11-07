---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 382aa35b9967e016ce87da982b32c97148c9f3c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772183"
---
# <span data-ttu-id="42e2e-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="42e2e-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="42e2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="42e2e-103">Cria um objeto do tipo ação de alerta</span><span class="sxs-lookup"><span data-stu-id="42e2e-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="42e2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42e2e-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42e2e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42e2e-105">DESCRIPTION</span></span>
<span data-ttu-id="42e2e-106">Cria um objeto do tipo ação de alerta esse objeto deve ser passado para o comando que cria a regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="42e2e-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="42e2e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42e2e-107">EXAMPLES</span></span>

### <span data-ttu-id="42e2e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42e2e-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="42e2e-109">OS</span><span class="sxs-lookup"><span data-stu-id="42e2e-109">PARAMETERS</span></span>

### <span data-ttu-id="42e2e-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="42e2e-110">-AznsAction</span></span>
<span data-ttu-id="42e2e-111">Os detalhes da ação AzNS</span><span class="sxs-lookup"><span data-stu-id="42e2e-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e2e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e2e-112">-DefaultProfile</span></span>
<span data-ttu-id="42e2e-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42e2e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42e2e-114">-Severidade</span><span class="sxs-lookup"><span data-stu-id="42e2e-114">-Severity</span></span>
<span data-ttu-id="42e2e-115">A gravidade para este alerta</span><span class="sxs-lookup"><span data-stu-id="42e2e-115">The severity for this alert</span></span>

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

### <span data-ttu-id="42e2e-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="42e2e-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="42e2e-117">A duração em minutos para a qual o alerta deve ser limitado</span><span class="sxs-lookup"><span data-stu-id="42e2e-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e2e-118">-Gatilho</span><span class="sxs-lookup"><span data-stu-id="42e2e-118">-Trigger</span></span>
<span data-ttu-id="42e2e-119">A condição de gatilho de alerta</span><span class="sxs-lookup"><span data-stu-id="42e2e-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e2e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e2e-120">CommonParameters</span></span>
<span data-ttu-id="42e2e-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e2e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e2e-122">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42e2e-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e2e-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42e2e-123">INPUTS</span></span>

### <span data-ttu-id="42e2e-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="42e2e-124">None</span></span>

## <span data-ttu-id="42e2e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42e2e-125">OUTPUTS</span></span>

### <span data-ttu-id="42e2e-126">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="42e2e-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="42e2e-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42e2e-127">NOTES</span></span>

## <span data-ttu-id="42e2e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42e2e-128">RELATED LINKS</span></span>