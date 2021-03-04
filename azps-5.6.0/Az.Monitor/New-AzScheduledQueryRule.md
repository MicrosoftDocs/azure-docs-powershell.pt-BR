---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 49863fd8102aef7b0175328edc0b4523f13921d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886613"
---
# <span data-ttu-id="a71b5-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a71b5-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="a71b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a71b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a71b5-103">Cria uma regra de alerta de log (tipo de regra de consulta agendada)</span><span class="sxs-lookup"><span data-stu-id="a71b5-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="a71b5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a71b5-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71b5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a71b5-105">DESCRIPTION</span></span>
<span data-ttu-id="a71b5-106">Cria uma regra de alerta de log (tipo de regra de consulta agendada)</span><span class="sxs-lookup"><span data-stu-id="a71b5-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="a71b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a71b5-107">EXAMPLES</span></span>

### <span data-ttu-id="a71b5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a71b5-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="a71b5-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a71b5-109">PARAMETERS</span></span>

### <span data-ttu-id="a71b5-110">-Action</span><span class="sxs-lookup"><span data-stu-id="a71b5-110">-Action</span></span>
<span data-ttu-id="a71b5-111">Ação de alerta da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="a71b5-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a71b5-112">-AsJob</span></span>
<span data-ttu-id="a71b5-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a71b5-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71b5-114">-DefaultProfile</span></span>
<span data-ttu-id="a71b5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a71b5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a71b5-116">-Description</span><span class="sxs-lookup"><span data-stu-id="a71b5-116">-Description</span></span>
<span data-ttu-id="a71b5-117">A descrição desse alerta</span><span class="sxs-lookup"><span data-stu-id="a71b5-117">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="a71b5-118">-Enabled</span></span>
<span data-ttu-id="a71b5-119">O estado de alerta do azure - valores válidos - $true, $false</span><span class="sxs-lookup"><span data-stu-id="a71b5-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a71b5-120">-Location</span></span>
<span data-ttu-id="a71b5-121">O local desse alerta</span><span class="sxs-lookup"><span data-stu-id="a71b5-121">The location for this alert</span></span>

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

### <span data-ttu-id="a71b5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a71b5-122">-Name</span></span>
<span data-ttu-id="a71b5-123">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="a71b5-123">The alert name</span></span>

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

### <span data-ttu-id="a71b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a71b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a71b5-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a71b5-125">The resource group name</span></span>

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

### <span data-ttu-id="a71b5-126">-Schedule</span><span class="sxs-lookup"><span data-stu-id="a71b5-126">-Schedule</span></span>
<span data-ttu-id="a71b5-127">O agendamento da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="a71b5-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-128">-Source</span><span class="sxs-lookup"><span data-stu-id="a71b5-128">-Source</span></span>
<span data-ttu-id="a71b5-129">A origem da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="a71b5-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a71b5-130">-Tag</span></span>
<span data-ttu-id="a71b5-131">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="a71b5-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a71b5-132">-Confirm</span></span>
<span data-ttu-id="a71b5-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71b5-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71b5-134">-WhatIf</span></span>
<span data-ttu-id="a71b5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a71b5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a71b5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a71b5-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71b5-137">CommonParameters</span></span>
<span data-ttu-id="a71b5-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a71b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71b5-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a71b5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71b5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a71b5-140">INPUTS</span></span>

### <span data-ttu-id="a71b5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a71b5-141">System.String</span></span>

## <span data-ttu-id="a71b5-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a71b5-142">OUTPUTS</span></span>

### <span data-ttu-id="a71b5-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="a71b5-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="a71b5-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="a71b5-144">NOTES</span></span>

## <span data-ttu-id="a71b5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a71b5-145">RELATED LINKS</span></span>
