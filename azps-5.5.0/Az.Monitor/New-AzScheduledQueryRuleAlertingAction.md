---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112950"
---
# <span data-ttu-id="a1141-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a1141-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="a1141-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1141-102">SYNOPSIS</span></span>
<span data-ttu-id="a1141-103">Cria um objeto do tipo Ação de Alerta</span><span class="sxs-lookup"><span data-stu-id="a1141-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="a1141-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1141-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1141-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1141-105">DESCRIPTION</span></span>
<span data-ttu-id="a1141-106">Cria um objeto do tipo Ação de Alerta Este objeto deve ser passado para o comando que cria a Regra de Alerta de Log</span><span class="sxs-lookup"><span data-stu-id="a1141-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="a1141-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1141-107">EXAMPLES</span></span>

### <span data-ttu-id="a1141-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1141-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="a1141-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1141-109">PARAMETERS</span></span>

### <span data-ttu-id="a1141-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="a1141-110">-AznsAction</span></span>
<span data-ttu-id="a1141-111">Os detalhes da ação AzNS</span><span class="sxs-lookup"><span data-stu-id="a1141-111">The AzNS action details</span></span>

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

### <span data-ttu-id="a1141-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1141-112">-DefaultProfile</span></span>
<span data-ttu-id="a1141-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1141-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1141-114">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="a1141-114">-Severity</span></span>
<span data-ttu-id="a1141-115">A gravidade deste alerta</span><span class="sxs-lookup"><span data-stu-id="a1141-115">The severity for this alert</span></span>

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

### <span data-ttu-id="a1141-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="a1141-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="a1141-117">A duração em minutos para o qual o alerta deve ser limitado</span><span class="sxs-lookup"><span data-stu-id="a1141-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="a1141-118">-Gatilho</span><span class="sxs-lookup"><span data-stu-id="a1141-118">-Trigger</span></span>
<span data-ttu-id="a1141-119">A condição de gatilho de alerta</span><span class="sxs-lookup"><span data-stu-id="a1141-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="a1141-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1141-120">CommonParameters</span></span>
<span data-ttu-id="a1141-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1141-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1141-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1141-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1141-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="a1141-123">INPUTS</span></span>

### <span data-ttu-id="a1141-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a1141-124">None</span></span>

## <span data-ttu-id="a1141-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="a1141-125">OUTPUTS</span></span>

### <span data-ttu-id="a1141-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a1141-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="a1141-127">Notas</span><span class="sxs-lookup"><span data-stu-id="a1141-127">NOTES</span></span>

## <span data-ttu-id="a1141-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1141-128">RELATED LINKS</span></span>
