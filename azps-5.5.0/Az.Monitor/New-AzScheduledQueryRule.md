---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112952"
---
# <span data-ttu-id="6e1ca-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6e1ca-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="6e1ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1ca-103">Cria uma Regra de Alerta de Log (tipo de Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="6e1ca-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="6e1ca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e1ca-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e1ca-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="6e1ca-106">Cria uma Regra de Alerta de Log (tipo de Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="6e1ca-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="6e1ca-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="6e1ca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e1ca-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="6e1ca-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e1ca-109">PARAMETERS</span></span>

### <span data-ttu-id="6e1ca-110">-Ação</span><span class="sxs-lookup"><span data-stu-id="6e1ca-110">-Action</span></span>
<span data-ttu-id="6e1ca-111">Ação de Alerta da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="6e1ca-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="6e1ca-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e1ca-112">-AsJob</span></span>
<span data-ttu-id="6e1ca-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6e1ca-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e1ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1ca-114">-DefaultProfile</span></span>
<span data-ttu-id="6e1ca-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1ca-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6e1ca-116">-Description</span></span>
<span data-ttu-id="6e1ca-117">A descrição deste alerta</span><span class="sxs-lookup"><span data-stu-id="6e1ca-117">The description for this alert</span></span>

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

### <span data-ttu-id="6e1ca-118">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="6e1ca-118">-Enabled</span></span>
<span data-ttu-id="6e1ca-119">O estado de alerta do Azure - valores válidos - $true, $false</span><span class="sxs-lookup"><span data-stu-id="6e1ca-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="6e1ca-120">-Local</span><span class="sxs-lookup"><span data-stu-id="6e1ca-120">-Location</span></span>
<span data-ttu-id="6e1ca-121">O local para este alerta</span><span class="sxs-lookup"><span data-stu-id="6e1ca-121">The location for this alert</span></span>

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

### <span data-ttu-id="6e1ca-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e1ca-122">-Name</span></span>
<span data-ttu-id="6e1ca-123">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="6e1ca-123">The alert name</span></span>

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

### <span data-ttu-id="6e1ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e1ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e1ca-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6e1ca-125">The resource group name</span></span>

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

### <span data-ttu-id="6e1ca-126">-Agendar</span><span class="sxs-lookup"><span data-stu-id="6e1ca-126">-Schedule</span></span>
<span data-ttu-id="6e1ca-127">O cronograma da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="6e1ca-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="6e1ca-128">-Origem</span><span class="sxs-lookup"><span data-stu-id="6e1ca-128">-Source</span></span>
<span data-ttu-id="6e1ca-129">A fonte da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="6e1ca-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="6e1ca-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e1ca-130">-Tag</span></span>
<span data-ttu-id="6e1ca-131">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="6e1ca-131">Resource tags</span></span>

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

### <span data-ttu-id="6e1ca-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6e1ca-132">-Confirm</span></span>
<span data-ttu-id="6e1ca-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e1ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e1ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e1ca-134">-WhatIf</span></span>
<span data-ttu-id="6e1ca-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6e1ca-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e1ca-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e1ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e1ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1ca-137">CommonParameters</span></span>
<span data-ttu-id="6e1ca-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1ca-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e1ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1ca-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="6e1ca-140">INPUTS</span></span>

### <span data-ttu-id="6e1ca-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6e1ca-141">System.String</span></span>

## <span data-ttu-id="6e1ca-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="6e1ca-142">OUTPUTS</span></span>

### <span data-ttu-id="6e1ca-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="6e1ca-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="6e1ca-144">Notas</span><span class="sxs-lookup"><span data-stu-id="6e1ca-144">NOTES</span></span>

## <span data-ttu-id="6e1ca-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e1ca-145">RELATED LINKS</span></span>
