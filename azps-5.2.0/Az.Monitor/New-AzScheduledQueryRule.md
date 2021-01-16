---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257969"
---
# <span data-ttu-id="44394-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="44394-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="44394-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44394-102">SYNOPSIS</span></span>
<span data-ttu-id="44394-103">Cria uma regra de alerta de log (tipo de regra de consulta agendada)</span><span class="sxs-lookup"><span data-stu-id="44394-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="44394-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44394-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44394-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44394-105">DESCRIPTION</span></span>
<span data-ttu-id="44394-106">Cria uma regra de alerta de log (tipo de regra de consulta agendada)</span><span class="sxs-lookup"><span data-stu-id="44394-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="44394-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44394-107">EXAMPLES</span></span>

### <span data-ttu-id="44394-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44394-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="44394-109">OS</span><span class="sxs-lookup"><span data-stu-id="44394-109">PARAMETERS</span></span>

### <span data-ttu-id="44394-110">-Ação</span><span class="sxs-lookup"><span data-stu-id="44394-110">-Action</span></span>
<span data-ttu-id="44394-111">A ação de alerta de regra de consulta programada</span><span class="sxs-lookup"><span data-stu-id="44394-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="44394-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44394-112">-AsJob</span></span>
<span data-ttu-id="44394-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="44394-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44394-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44394-114">-DefaultProfile</span></span>
<span data-ttu-id="44394-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44394-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44394-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="44394-116">-Description</span></span>
<span data-ttu-id="44394-117">A descrição para este alerta</span><span class="sxs-lookup"><span data-stu-id="44394-117">The description for this alert</span></span>

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

### <span data-ttu-id="44394-118">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="44394-118">-Enabled</span></span>
<span data-ttu-id="44394-119">O estado do alerta do Azure-valores válidos-$true $false</span><span class="sxs-lookup"><span data-stu-id="44394-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="44394-120">-Local</span><span class="sxs-lookup"><span data-stu-id="44394-120">-Location</span></span>
<span data-ttu-id="44394-121">O local para este alerta</span><span class="sxs-lookup"><span data-stu-id="44394-121">The location for this alert</span></span>

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

### <span data-ttu-id="44394-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="44394-122">-Name</span></span>
<span data-ttu-id="44394-123">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="44394-123">The alert name</span></span>

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

### <span data-ttu-id="44394-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44394-124">-ResourceGroupName</span></span>
<span data-ttu-id="44394-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="44394-125">The resource group name</span></span>

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

### <span data-ttu-id="44394-126">-Cronograma</span><span class="sxs-lookup"><span data-stu-id="44394-126">-Schedule</span></span>
<span data-ttu-id="44394-127">A agenda de regras de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="44394-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="44394-128">-Fonte</span><span class="sxs-lookup"><span data-stu-id="44394-128">-Source</span></span>
<span data-ttu-id="44394-129">A origem da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="44394-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="44394-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="44394-130">-Tag</span></span>
<span data-ttu-id="44394-131">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="44394-131">Resource tags</span></span>

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

### <span data-ttu-id="44394-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44394-132">-Confirm</span></span>
<span data-ttu-id="44394-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44394-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44394-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44394-134">-WhatIf</span></span>
<span data-ttu-id="44394-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44394-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44394-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44394-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44394-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44394-137">CommonParameters</span></span>
<span data-ttu-id="44394-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44394-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44394-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44394-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44394-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44394-140">INPUTS</span></span>

### <span data-ttu-id="44394-141">System. String</span><span class="sxs-lookup"><span data-stu-id="44394-141">System.String</span></span>

## <span data-ttu-id="44394-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44394-142">OUTPUTS</span></span>

### <span data-ttu-id="44394-143">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="44394-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="44394-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44394-144">NOTES</span></span>

## <span data-ttu-id="44394-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44394-145">RELATED LINKS</span></span>
