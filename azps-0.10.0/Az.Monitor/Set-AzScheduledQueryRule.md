---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 5a1ae00f13494c73c6e27aa6aeeeda391d17a512
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775670"
---
# <span data-ttu-id="83bfe-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="83bfe-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="83bfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="83bfe-103">Atualiza uma regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="83bfe-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="83bfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83bfe-104">SYNTAX</span></span>

### <span data-ttu-id="83bfe-105">ByRuleName (padrão)</span><span class="sxs-lookup"><span data-stu-id="83bfe-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83bfe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83bfe-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83bfe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83bfe-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83bfe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83bfe-108">DESCRIPTION</span></span>
<span data-ttu-id="83bfe-109">Atualiza uma regra de alerta de log por colocar semântica</span><span class="sxs-lookup"><span data-stu-id="83bfe-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="83bfe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83bfe-110">EXAMPLES</span></span>

### <span data-ttu-id="83bfe-111">Exemplo 1-definir pelo nome da regra</span><span class="sxs-lookup"><span data-stu-id="83bfe-111">Example 1 - Set by rule name</span></span>
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

### <span data-ttu-id="83bfe-112">Exemplo 2-definido por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="83bfe-112">Example 2 - Set by Input Object</span></span>
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

### <span data-ttu-id="83bfe-113">Exemplo 3 – definido por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="83bfe-113">Example 3 - Set by resource Id</span></span>
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

## <span data-ttu-id="83bfe-114">OS</span><span class="sxs-lookup"><span data-stu-id="83bfe-114">PARAMETERS</span></span>

### <span data-ttu-id="83bfe-115">-Ação</span><span class="sxs-lookup"><span data-stu-id="83bfe-115">-Action</span></span>
<span data-ttu-id="83bfe-116">A ação de alerta de regra de consulta programada</span><span class="sxs-lookup"><span data-stu-id="83bfe-116">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="83bfe-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83bfe-117">-AsJob</span></span>
<span data-ttu-id="83bfe-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="83bfe-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83bfe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83bfe-119">-DefaultProfile</span></span>
<span data-ttu-id="83bfe-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83bfe-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83bfe-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="83bfe-121">-Description</span></span>
<span data-ttu-id="83bfe-122">A descrição para este alerta</span><span class="sxs-lookup"><span data-stu-id="83bfe-122">The description for this alert</span></span>

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

### <span data-ttu-id="83bfe-123">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="83bfe-123">-Enabled</span></span>
<span data-ttu-id="83bfe-124">O estado do alerta do Azure-valores válidos-$true $false</span><span class="sxs-lookup"><span data-stu-id="83bfe-124">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="83bfe-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83bfe-125">-InputObject</span></span>
<span data-ttu-id="83bfe-126">O recurso de regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="83bfe-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="83bfe-127">-Local</span><span class="sxs-lookup"><span data-stu-id="83bfe-127">-Location</span></span>
<span data-ttu-id="83bfe-128">O local para este alerta</span><span class="sxs-lookup"><span data-stu-id="83bfe-128">The location for this alert</span></span>

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

### <span data-ttu-id="83bfe-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="83bfe-129">-Name</span></span>
<span data-ttu-id="83bfe-130">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="83bfe-130">The alert name</span></span>

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

### <span data-ttu-id="83bfe-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83bfe-131">-ResourceGroupName</span></span>
<span data-ttu-id="83bfe-132">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="83bfe-132">The resource group name</span></span>

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

### <span data-ttu-id="83bfe-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83bfe-133">-ResourceId</span></span>
<span data-ttu-id="83bfe-134">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="83bfe-134">The resource Id</span></span>

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

### <span data-ttu-id="83bfe-135">-Cronograma</span><span class="sxs-lookup"><span data-stu-id="83bfe-135">-Schedule</span></span>
<span data-ttu-id="83bfe-136">A agenda de regras de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="83bfe-136">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="83bfe-137">-Fonte</span><span class="sxs-lookup"><span data-stu-id="83bfe-137">-Source</span></span>
<span data-ttu-id="83bfe-138">A origem da regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="83bfe-138">The scheduled query rule source</span></span>

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

### <span data-ttu-id="83bfe-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="83bfe-139">-Tag</span></span>
<span data-ttu-id="83bfe-140">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="83bfe-140">Resource tags</span></span>

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

### <span data-ttu-id="83bfe-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="83bfe-141">-Confirm</span></span>
<span data-ttu-id="83bfe-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83bfe-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83bfe-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83bfe-143">-WhatIf</span></span>
<span data-ttu-id="83bfe-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="83bfe-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83bfe-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="83bfe-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83bfe-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83bfe-146">CommonParameters</span></span>
<span data-ttu-id="83bfe-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83bfe-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83bfe-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83bfe-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83bfe-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83bfe-149">INPUTS</span></span>

### <span data-ttu-id="83bfe-150">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="83bfe-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="83bfe-151">System. String</span><span class="sxs-lookup"><span data-stu-id="83bfe-151">System.String</span></span>

### <span data-ttu-id="83bfe-152">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="83bfe-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="83bfe-153">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="83bfe-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="83bfe-154">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="83bfe-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="83bfe-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83bfe-155">OUTPUTS</span></span>

### <span data-ttu-id="83bfe-156">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="83bfe-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="83bfe-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83bfe-157">NOTES</span></span>

## <span data-ttu-id="83bfe-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83bfe-158">RELATED LINKS</span></span>
