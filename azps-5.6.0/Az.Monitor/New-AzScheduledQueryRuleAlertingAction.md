---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 0394aa7c2db880bbb10c8d68c9d502560c1035bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886612"
---
# <span data-ttu-id="bd00a-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bd00a-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="bd00a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd00a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd00a-103">Cria um objeto do tipo Ação de Alerta</span><span class="sxs-lookup"><span data-stu-id="bd00a-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="bd00a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bd00a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd00a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bd00a-105">DESCRIPTION</span></span>
<span data-ttu-id="bd00a-106">Cria um objeto do tipo Ação de Alerta Este objeto deve ser passado para o comando que cria a Regra de Alerta de Log</span><span class="sxs-lookup"><span data-stu-id="bd00a-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="bd00a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd00a-107">EXAMPLES</span></span>

### <span data-ttu-id="bd00a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bd00a-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="bd00a-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bd00a-109">PARAMETERS</span></span>

### <span data-ttu-id="bd00a-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="bd00a-110">-AznsAction</span></span>
<span data-ttu-id="bd00a-111">Os detalhes da ação do AzNS</span><span class="sxs-lookup"><span data-stu-id="bd00a-111">The AzNS action details</span></span>

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

### <span data-ttu-id="bd00a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd00a-112">-DefaultProfile</span></span>
<span data-ttu-id="bd00a-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd00a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd00a-114">-Severity</span><span class="sxs-lookup"><span data-stu-id="bd00a-114">-Severity</span></span>
<span data-ttu-id="bd00a-115">A gravidade desse alerta</span><span class="sxs-lookup"><span data-stu-id="bd00a-115">The severity for this alert</span></span>

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

### <span data-ttu-id="bd00a-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="bd00a-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="bd00a-117">A duração em minutos para a qual o alerta deve ser limitado</span><span class="sxs-lookup"><span data-stu-id="bd00a-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="bd00a-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="bd00a-118">-Trigger</span></span>
<span data-ttu-id="bd00a-119">A condição de gatilho de alerta</span><span class="sxs-lookup"><span data-stu-id="bd00a-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="bd00a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd00a-120">CommonParameters</span></span>
<span data-ttu-id="bd00a-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd00a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd00a-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd00a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd00a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd00a-123">INPUTS</span></span>

### <span data-ttu-id="bd00a-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bd00a-124">None</span></span>

## <span data-ttu-id="bd00a-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bd00a-125">OUTPUTS</span></span>

### <span data-ttu-id="bd00a-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bd00a-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="bd00a-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="bd00a-127">NOTES</span></span>

## <span data-ttu-id="bd00a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd00a-128">RELATED LINKS</span></span>
