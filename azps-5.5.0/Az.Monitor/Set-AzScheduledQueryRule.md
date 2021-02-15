---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 0351d6920c4af7f781ef27f4dfbc36a13e0c50cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114237"
---
# <span data-ttu-id="a1519-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a1519-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="a1519-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1519-102">SYNOPSIS</span></span>
<span data-ttu-id="a1519-103">Atualiza uma Regra de Alerta de Log</span><span class="sxs-lookup"><span data-stu-id="a1519-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="a1519-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1519-104">SYNTAX</span></span>

### <span data-ttu-id="a1519-105">ByRuleName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a1519-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1519-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1519-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1519-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1519-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1519-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1519-108">DESCRIPTION</span></span>
<span data-ttu-id="a1519-109">Atualiza uma Regra de Alerta de Log por semântica PUT</span><span class="sxs-lookup"><span data-stu-id="a1519-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="a1519-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1519-110">EXAMPLES</span></span>

### <span data-ttu-id="a1519-111">Exemplo 1: Definir por nome de regra</span><span class="sxs-lookup"><span data-stu-id="a1519-111">Example 1: Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="a1519-112">Exemplo 2: Definir por Objeto de Entrada</span><span class="sxs-lookup"><span data-stu-id="a1519-112">Example 2: Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="a1519-113">Exemplo 3: Definir por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="a1519-113">Example 3: Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="a1519-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1519-114">PARAMETERS</span></span>

### <span data-ttu-id="a1519-115">-Ação</span><span class="sxs-lookup"><span data-stu-id="a1519-115">-Action</span></span>
<span data-ttu-id="a1519-116">Ação de Alerta da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="a1519-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1519-117">-AsJob</span></span>
<span data-ttu-id="a1519-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a1519-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1519-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1519-119">-DefaultProfile</span></span>
<span data-ttu-id="a1519-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1519-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1519-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a1519-121">-Description</span></span>
<span data-ttu-id="a1519-122">A descrição deste alerta</span><span class="sxs-lookup"><span data-stu-id="a1519-122">The description for this alert</span></span>

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

### <span data-ttu-id="a1519-123">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="a1519-123">-Enabled</span></span>
<span data-ttu-id="a1519-124">O estado de alerta do Azure - valores válidos - $true, $false</span><span class="sxs-lookup"><span data-stu-id="a1519-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1519-125">-InputObject</span></span>
<span data-ttu-id="a1519-126">O recurso Regra de Consulta Agendada</span><span class="sxs-lookup"><span data-stu-id="a1519-126">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-127">-Local</span><span class="sxs-lookup"><span data-stu-id="a1519-127">-Location</span></span>
<span data-ttu-id="a1519-128">O local para este alerta</span><span class="sxs-lookup"><span data-stu-id="a1519-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1519-129">-Name</span></span>
<span data-ttu-id="a1519-130">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="a1519-130">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1519-131">-ResourceGroupName</span></span>
<span data-ttu-id="a1519-132">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a1519-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1519-133">-ResourceId</span></span>
<span data-ttu-id="a1519-134">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="a1519-134">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-135">-Agendar</span><span class="sxs-lookup"><span data-stu-id="a1519-135">-Schedule</span></span>
<span data-ttu-id="a1519-136">O cronograma da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="a1519-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-137">-Origem</span><span class="sxs-lookup"><span data-stu-id="a1519-137">-Source</span></span>
<span data-ttu-id="a1519-138">A fonte da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="a1519-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1519-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1519-139">-Tag</span></span>
<span data-ttu-id="a1519-140">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="a1519-140">Resource tags</span></span>

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

### <span data-ttu-id="a1519-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a1519-141">-Confirm</span></span>
<span data-ttu-id="a1519-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1519-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1519-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1519-143">-WhatIf</span></span>
<span data-ttu-id="a1519-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a1519-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1519-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1519-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1519-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1519-146">CommonParameters</span></span>
<span data-ttu-id="a1519-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1519-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1519-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1519-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1519-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="a1519-149">INPUTS</span></span>

### <span data-ttu-id="a1519-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="a1519-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="a1519-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a1519-151">System.String</span></span>

### <span data-ttu-id="a1519-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a1519-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="a1519-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a1519-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="a1519-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a1519-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="a1519-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="a1519-155">OUTPUTS</span></span>

### <span data-ttu-id="a1519-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="a1519-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="a1519-157">Notas</span><span class="sxs-lookup"><span data-stu-id="a1519-157">NOTES</span></span>

## <span data-ttu-id="a1519-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1519-158">RELATED LINKS</span></span>
