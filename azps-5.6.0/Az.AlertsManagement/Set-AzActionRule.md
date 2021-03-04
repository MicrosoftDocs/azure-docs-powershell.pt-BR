---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 65d402f06770542265bd9b0a6e9e50cd943114f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901525"
---
# <span data-ttu-id="51104-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="51104-101">Set-AzActionRule</span></span>

## <span data-ttu-id="51104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51104-102">SYNOPSIS</span></span>
<span data-ttu-id="51104-103">Criar ou atualizar uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="51104-103">Create or update an action rule.</span></span>

## <span data-ttu-id="51104-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51104-104">SYNTAX</span></span>

### <span data-ttu-id="51104-105">BySimplifiedFormatDiagnosticsActionRule (Padrão)</span><span class="sxs-lookup"><span data-stu-id="51104-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51104-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="51104-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51104-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="51104-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51104-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="51104-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51104-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51104-109">DESCRIPTION</span></span>
<span data-ttu-id="51104-110">**Set-AzActionRule** cria ou atualiza uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="51104-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="51104-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51104-111">EXAMPLES</span></span>

### <span data-ttu-id="51104-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51104-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="51104-113">Este cmdlet cria uma regra de ação para supressão, com um escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="51104-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="51104-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="51104-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="51104-115">Este cmdlet cria uma regra de ação para o grupo de ações, com uma lista de escopo de grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="51104-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="51104-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="51104-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="51104-117">Este cmdlet cria uma regra de ação para configurações de diagnóstico, com um escopo de recurso.</span><span class="sxs-lookup"><span data-stu-id="51104-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="51104-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51104-118">PARAMETERS</span></span>

### <span data-ttu-id="51104-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="51104-119">-ActionGroupId</span></span>
<span data-ttu-id="51104-120">ID do Grupo de Ações que deve ser notificado.</span><span class="sxs-lookup"><span data-stu-id="51104-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="51104-121">-ActionRuleType</span></span>
<span data-ttu-id="51104-122">Formato Json da regra de ação</span><span class="sxs-lookup"><span data-stu-id="51104-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="51104-123">-AlertContextCondition</span></span>
<span data-ttu-id="51104-124">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="51104-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="51104-125">Contains:smartgroups</span><span class="sxs-lookup"><span data-stu-id="51104-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="51104-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="51104-127">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="51104-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="51104-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="51104-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51104-129">-DefaultProfile</span></span>
<span data-ttu-id="51104-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51104-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51104-131">-Description</span><span class="sxs-lookup"><span data-stu-id="51104-131">-Description</span></span>
<span data-ttu-id="51104-132">Descrição da Regra de Ação</span><span class="sxs-lookup"><span data-stu-id="51104-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="51104-133">-DescriptionCondition</span></span>
<span data-ttu-id="51104-134">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="51104-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="51104-135">Contains:Test Alert</span><span class="sxs-lookup"><span data-stu-id="51104-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51104-136">-InputObject</span></span>
<span data-ttu-id="51104-137">O recurso de regra de ação</span><span class="sxs-lookup"><span data-stu-id="51104-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51104-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="51104-138">-MonitorCondition</span></span>
<span data-ttu-id="51104-139">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="51104-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="51104-140">NotEquals:Resolved</span><span class="sxs-lookup"><span data-stu-id="51104-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="51104-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="51104-142">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="51104-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="51104-143">Equals:Platform,Log Analytics</span><span class="sxs-lookup"><span data-stu-id="51104-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-144">-Name</span><span class="sxs-lookup"><span data-stu-id="51104-144">-Name</span></span>
<span data-ttu-id="51104-145">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="51104-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="51104-146">-ReccurenceType</span></span>
<span data-ttu-id="51104-147">Especifica a duração quando a supressão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="51104-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="51104-148">-ReccurentValue</span></span>
<span data-ttu-id="51104-149">Valores reccurent, se aplicável. No caso de Semanal - \[ 1,2 \] No caso de Mensal - \[ 1,3,5,30\]</span><span class="sxs-lookup"><span data-stu-id="51104-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51104-150">-ResourceGroupName</span></span>
<span data-ttu-id="51104-151">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="51104-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="51104-152">-Scope</span></span>
<span data-ttu-id="51104-153">Lista separada por vírgulas de valores</span><span class="sxs-lookup"><span data-stu-id="51104-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="51104-154">-SeverityCondition</span></span>
<span data-ttu-id="51104-155">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="51104-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="51104-156">Equals:Sev0,Sev1</span><span class="sxs-lookup"><span data-stu-id="51104-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-157">-Status</span><span class="sxs-lookup"><span data-stu-id="51104-157">-Status</span></span>
<span data-ttu-id="51104-158">Status da Regra de Ação.</span><span class="sxs-lookup"><span data-stu-id="51104-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="51104-159">-SuppressionEndTime</span></span>
<span data-ttu-id="51104-160">Hora de término de supressão.</span><span class="sxs-lookup"><span data-stu-id="51104-160">Suppression End Time.</span></span>
<span data-ttu-id="51104-161">Formato 12/09/2018 06:00:00 +Deve ser mencionado no caso de Agendamento de Supressão Reccurent - Uma Vez, Diariamente, Semanal ou Mensal.</span><span class="sxs-lookup"><span data-stu-id="51104-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="51104-162">-SuppressionStartTime</span></span>
<span data-ttu-id="51104-163">Hora de início de supressão.</span><span class="sxs-lookup"><span data-stu-id="51104-163">Suppression Start Time.</span></span>
<span data-ttu-id="51104-164">Formato 12/09/2018 06:00:00 +Deve ser mencionado no caso de Agendamento de Supressão Reccurent - Uma Vez, Diariamente, Semanal ou Mensal.</span><span class="sxs-lookup"><span data-stu-id="51104-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="51104-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="51104-166">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="51104-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="51104-167">Contém:Máquinas Virtuais,Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="51104-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51104-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51104-168">-Confirm</span></span>
<span data-ttu-id="51104-169">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51104-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51104-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51104-170">-WhatIf</span></span>
<span data-ttu-id="51104-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51104-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51104-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51104-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51104-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51104-173">CommonParameters</span></span>
<span data-ttu-id="51104-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51104-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51104-175">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51104-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51104-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51104-176">INPUTS</span></span>

### <span data-ttu-id="51104-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="51104-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="51104-178">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51104-178">OUTPUTS</span></span>

### <span data-ttu-id="51104-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="51104-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="51104-180">NOTES</span><span class="sxs-lookup"><span data-stu-id="51104-180">NOTES</span></span>

## <span data-ttu-id="51104-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51104-181">RELATED LINKS</span></span>
