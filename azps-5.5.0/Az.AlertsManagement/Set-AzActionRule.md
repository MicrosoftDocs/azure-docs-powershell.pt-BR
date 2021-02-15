---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 75a2071e8f60ed15420b69815eba22d6f82e9f82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114865"
---
# <span data-ttu-id="d34d4-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="d34d4-101">Set-AzActionRule</span></span>

## <span data-ttu-id="d34d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d34d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d34d4-103">Criar ou atualizar uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="d34d4-103">Create or update an action rule.</span></span>

## <span data-ttu-id="d34d4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d34d4-104">SYNTAX</span></span>

### <span data-ttu-id="d34d4-105">BySimplifiedFormatDiagnosticsActionRule (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d34d4-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d34d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d34d4-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d34d4-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="d34d4-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d34d4-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="d34d4-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34d4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d34d4-109">DESCRIPTION</span></span>
<span data-ttu-id="d34d4-110">**O Set-AzActionRule** cria ou atualiza uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="d34d4-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="d34d4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d34d4-111">EXAMPLES</span></span>

### <span data-ttu-id="d34d4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d34d4-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="d34d4-113">Este cmdlet cria uma regra de ação para resserção, com um escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d34d4-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="d34d4-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d34d4-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="d34d4-115">Esse cmdlet cria uma regra de ação para o grupo de ações, com uma lista de escopo de grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="d34d4-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="d34d4-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d34d4-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="d34d4-117">Esse cmdlet cria uma regra de ação para configurações de diagnóstico, com um escopo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d34d4-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="d34d4-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d34d4-118">PARAMETERS</span></span>

### <span data-ttu-id="d34d4-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="d34d4-119">-ActionGroupId</span></span>
<span data-ttu-id="d34d4-120">ID do Grupo de Ações que deve ser notificada.</span><span class="sxs-lookup"><span data-stu-id="d34d4-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="d34d4-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="d34d4-121">-ActionRuleType</span></span>
<span data-ttu-id="d34d4-122">Formatar Json da regra de ação</span><span class="sxs-lookup"><span data-stu-id="d34d4-122">Action rule Json format</span></span>

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

### <span data-ttu-id="d34d4-123">-AlertContextContextCondition</span><span class="sxs-lookup"><span data-stu-id="d34d4-123">-AlertContextCondition</span></span>
<span data-ttu-id="d34d4-124">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="d34d4-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d34d4-125">Contém:grupos inteligentes</span><span class="sxs-lookup"><span data-stu-id="d34d4-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="d34d4-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="d34d4-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="d34d4-127">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="d34d4-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d34d4-128">Igual a:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvaônia/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvalt</span><span class="sxs-lookup"><span data-stu-id="d34d4-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="d34d4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34d4-129">-DefaultProfile</span></span>
<span data-ttu-id="d34d4-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d34d4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d34d4-131">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d34d4-131">-Description</span></span>
<span data-ttu-id="d34d4-132">Descrição da Regra de Ação</span><span class="sxs-lookup"><span data-stu-id="d34d4-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="d34d4-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="d34d4-133">-DescriptionCondition</span></span>
<span data-ttu-id="d34d4-134">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="d34d4-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d34d4-135">Contém:Alerta de Teste</span><span class="sxs-lookup"><span data-stu-id="d34d4-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="d34d4-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d34d4-136">-InputObject</span></span>
<span data-ttu-id="d34d4-137">O recurso de regra de ação</span><span class="sxs-lookup"><span data-stu-id="d34d4-137">The action rule resource</span></span>

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

### <span data-ttu-id="d34d4-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="d34d4-138">-MonitorCondition</span></span>
<span data-ttu-id="d34d4-139">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="d34d4-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d34d4-140">NotEquals:Resolved</span><span class="sxs-lookup"><span data-stu-id="d34d4-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="d34d4-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="d34d4-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="d34d4-142">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="d34d4-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d34d4-143">É igual a:Plataforma, Análise de Log</span><span class="sxs-lookup"><span data-stu-id="d34d4-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="d34d4-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="d34d4-144">-Name</span></span>
<span data-ttu-id="d34d4-145">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="d34d4-145">Action rule Name</span></span>

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

### <span data-ttu-id="d34d4-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="d34d4-146">-ReccurenceType</span></span>
<span data-ttu-id="d34d4-147">Especifica a duração quando a suprimição deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="d34d4-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="d34d4-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="d34d4-148">-ReccurentValue</span></span>
<span data-ttu-id="d34d4-149">Valores recurentes, se aplicável. No caso de Semanal - \[ 1,2 No caso de \] Mensal - \[ 1,3,5,30\]</span><span class="sxs-lookup"><span data-stu-id="d34d4-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="d34d4-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34d4-150">-ResourceGroupName</span></span>
<span data-ttu-id="d34d4-151">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d34d4-151">Resource Group Name</span></span>

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

### <span data-ttu-id="d34d4-152">-Escopo</span><span class="sxs-lookup"><span data-stu-id="d34d4-152">-Scope</span></span>
<span data-ttu-id="d34d4-153">Lista de valores separada por vírgulas</span><span class="sxs-lookup"><span data-stu-id="d34d4-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="d34d4-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="d34d4-154">-SeverityCondition</span></span>
<span data-ttu-id="d34d4-155">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="d34d4-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d34d4-156">É igual a:Sev0,Sev1</span><span class="sxs-lookup"><span data-stu-id="d34d4-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="d34d4-157">-Status</span><span class="sxs-lookup"><span data-stu-id="d34d4-157">-Status</span></span>
<span data-ttu-id="d34d4-158">Status da Regra de Ação.</span><span class="sxs-lookup"><span data-stu-id="d34d4-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="d34d4-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="d34d4-159">-SuppressionEndTime</span></span>
<span data-ttu-id="d34d4-160">Hora de Término da Suprimição.</span><span class="sxs-lookup"><span data-stu-id="d34d4-160">Suppression End Time.</span></span>
<span data-ttu-id="d34d4-161">Formatar 09/12/2018 06:00:00 +Deve ser mencionado no caso de Cronograma de Recorrência – Uma Vez, Diário, Semanal ou Mensal.</span><span class="sxs-lookup"><span data-stu-id="d34d4-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="d34d4-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="d34d4-162">-SuppressionStartTime</span></span>
<span data-ttu-id="d34d4-163">Hora de Início da Suprimição.</span><span class="sxs-lookup"><span data-stu-id="d34d4-163">Suppression Start Time.</span></span>
<span data-ttu-id="d34d4-164">Formatar 09/12/2018 06:00:00 +Deve ser mencionado no caso de Cronograma de Recorrência – Uma Vez, Diário, Semanal ou Mensal.</span><span class="sxs-lookup"><span data-stu-id="d34d4-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="d34d4-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="d34d4-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="d34d4-166">Formato esperado - { \<operation\> : } Para por \<comma separated list of values\> exemplo.</span><span class="sxs-lookup"><span data-stu-id="d34d4-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="d34d4-167">Contém:Máquinas Virtuais, Conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="d34d4-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="d34d4-168">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d34d4-168">-Confirm</span></span>
<span data-ttu-id="d34d4-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d34d4-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34d4-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34d4-170">-WhatIf</span></span>
<span data-ttu-id="d34d4-171">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d34d4-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d34d4-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d34d4-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34d4-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34d4-173">CommonParameters</span></span>
<span data-ttu-id="d34d4-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34d4-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34d4-175">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d34d4-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34d4-176">Entradas</span><span class="sxs-lookup"><span data-stu-id="d34d4-176">INPUTS</span></span>

### <span data-ttu-id="d34d4-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d34d4-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d34d4-178">Saídas</span><span class="sxs-lookup"><span data-stu-id="d34d4-178">OUTPUTS</span></span>

### <span data-ttu-id="d34d4-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d34d4-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d34d4-180">Notas</span><span class="sxs-lookup"><span data-stu-id="d34d4-180">NOTES</span></span>

## <span data-ttu-id="d34d4-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d34d4-181">RELATED LINKS</span></span>
