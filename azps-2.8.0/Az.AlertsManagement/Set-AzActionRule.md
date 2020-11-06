---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 15b847034300d01df354cc7512305ffd3cab8279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598179"
---
# <span data-ttu-id="cc954-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="cc954-101">Set-AzActionRule</span></span>

## <span data-ttu-id="cc954-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc954-102">SYNOPSIS</span></span>
<span data-ttu-id="cc954-103">Criar ou atualizar uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="cc954-103">Create or update an action rule.</span></span>

## <span data-ttu-id="cc954-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc954-104">SYNTAX</span></span>

### <span data-ttu-id="cc954-105">BySimplifiedFormatDiagnosticsActionRule (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc954-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc954-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc954-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc954-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="cc954-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc954-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="cc954-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc954-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc954-109">DESCRIPTION</span></span>
<span data-ttu-id="cc954-110">**Set-AzActionRule** cria ou atualiza uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="cc954-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="cc954-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc954-111">EXAMPLES</span></span>

### <span data-ttu-id="cc954-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc954-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="cc954-113">Esse cmdlet cria uma regra de ação para supressão.</span><span class="sxs-lookup"><span data-stu-id="cc954-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="cc954-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cc954-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="cc954-115">Esse cmdlet cria uma regra de ação para o grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="cc954-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="cc954-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cc954-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="cc954-117">Esse cmdlet cria uma regra de ação para configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="cc954-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="cc954-118">OS</span><span class="sxs-lookup"><span data-stu-id="cc954-118">PARAMETERS</span></span>

### <span data-ttu-id="cc954-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="cc954-119">-ActionGroupId</span></span>
<span data-ttu-id="cc954-120">ID do grupo de ação que será notificado.</span><span class="sxs-lookup"><span data-stu-id="cc954-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="cc954-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="cc954-121">-ActionRuleType</span></span>
<span data-ttu-id="cc954-122">Formato JSON da regra de ação</span><span class="sxs-lookup"><span data-stu-id="cc954-122">Action rule Json format</span></span>

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

### <span data-ttu-id="cc954-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="cc954-123">-AlertContextCondition</span></span>
<span data-ttu-id="cc954-124">Formato esperado-{ \< Operation \> : \< lista de valores separados por vírgula \> } para ex.</span><span class="sxs-lookup"><span data-stu-id="cc954-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cc954-125">Contém: smartgroups</span><span class="sxs-lookup"><span data-stu-id="cc954-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="cc954-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="cc954-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="cc954-127">Formato esperado-{ \< Operation \> : \< lista de valores separados por vírgula \> } para ex.</span><span class="sxs-lookup"><span data-stu-id="cc954-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cc954-128">Equals:/assinaturas/ad825170-845c-47db-8F00-11978947b089/resourceGroups/abvarma/Providers/Microsoft. insights/metricAlerts/Test-mrmc-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="cc954-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="cc954-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc954-129">-DefaultProfile</span></span>
<span data-ttu-id="cc954-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc954-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc954-131">-Descrição</span><span class="sxs-lookup"><span data-stu-id="cc954-131">-Description</span></span>
<span data-ttu-id="cc954-132">Descrição da regra de ação</span><span class="sxs-lookup"><span data-stu-id="cc954-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="cc954-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="cc954-133">-DescriptionCondition</span></span>
<span data-ttu-id="cc954-134">Formato esperado-{ \< Operation \> : \< lista de valores separados por vírgula \> } para ex.</span><span class="sxs-lookup"><span data-stu-id="cc954-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cc954-135">Contém: alerta de teste</span><span class="sxs-lookup"><span data-stu-id="cc954-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="cc954-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc954-136">-InputObject</span></span>
<span data-ttu-id="cc954-137">O recurso regra de ação</span><span class="sxs-lookup"><span data-stu-id="cc954-137">The action rule resource</span></span>

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

### <span data-ttu-id="cc954-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="cc954-138">-MonitorCondition</span></span>
<span data-ttu-id="cc954-139">Formato esperado-{ \< Operation \> : \< lista de valores separados por vírgula \> } para ex.</span><span class="sxs-lookup"><span data-stu-id="cc954-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cc954-140">Não igual a: resolvido</span><span class="sxs-lookup"><span data-stu-id="cc954-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="cc954-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="cc954-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="cc954-142">Formato esperado-{ \< Operation \> : \< lista de valores separados por vírgula \> } para ex.</span><span class="sxs-lookup"><span data-stu-id="cc954-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cc954-143">Igual a: plataforma, análise de logs</span><span class="sxs-lookup"><span data-stu-id="cc954-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="cc954-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc954-144">-Name</span></span>
<span data-ttu-id="cc954-145">Nome da regra da ação</span><span class="sxs-lookup"><span data-stu-id="cc954-145">Action rule Name</span></span>

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

### <span data-ttu-id="cc954-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="cc954-146">-ReccurenceType</span></span>
<span data-ttu-id="cc954-147">Especifica a duração quando a supressão deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="cc954-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="cc954-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="cc954-148">-ReccurentValue</span></span>
<span data-ttu-id="cc954-149">Valores de Reccurent, se aplicável. Em caso de semana- \[ 1, 2 \] em caso de mês- \[ 1, 3, 5, 30\]</span><span class="sxs-lookup"><span data-stu-id="cc954-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="cc954-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc954-150">-ResourceGroupName</span></span>
<span data-ttu-id="cc954-151">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cc954-151">Resource Group Name</span></span>

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

### <span data-ttu-id="cc954-152">-Escopo</span><span class="sxs-lookup"><span data-stu-id="cc954-152">-Scope</span></span>
<span data-ttu-id="cc954-153">Lista de valores separados por vírgula</span><span class="sxs-lookup"><span data-stu-id="cc954-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="cc954-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="cc954-154">-SeverityCondition</span></span>
<span data-ttu-id="cc954-155">Formato esperado-{ \< Operation \> : \< lista de valores separados por vírgula \> } para ex.</span><span class="sxs-lookup"><span data-stu-id="cc954-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cc954-156">É igual a: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="cc954-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="cc954-157">-Status</span><span class="sxs-lookup"><span data-stu-id="cc954-157">-Status</span></span>
<span data-ttu-id="cc954-158">Status da regra da ação.</span><span class="sxs-lookup"><span data-stu-id="cc954-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="cc954-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="cc954-159">-SuppressionEndTime</span></span>
<span data-ttu-id="cc954-160">Hora de término da supressão.</span><span class="sxs-lookup"><span data-stu-id="cc954-160">Suppression End Time.</span></span>
<span data-ttu-id="cc954-161">O formato 12/09/2018 06:00:00 + deve ser mencionado em caso de Reccurent do programa de supressão de uma vez, diariamente, semanalmente ou mensalmente.</span><span class="sxs-lookup"><span data-stu-id="cc954-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="cc954-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="cc954-162">-SuppressionStartTime</span></span>
<span data-ttu-id="cc954-163">Hora de início da supressão.</span><span class="sxs-lookup"><span data-stu-id="cc954-163">Suppression Start Time.</span></span>
<span data-ttu-id="cc954-164">O formato 12/09/2018 06:00:00 + deve ser mencionado em caso de Reccurent do programa de supressão de uma vez, diariamente, semanalmente ou mensalmente.</span><span class="sxs-lookup"><span data-stu-id="cc954-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="cc954-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="cc954-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="cc954-166">Formato esperado-{ \< Operation \> : \< lista de valores separados por vírgula \> } para ex.</span><span class="sxs-lookup"><span data-stu-id="cc954-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="cc954-167">Contém: máquinas virtuais, conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="cc954-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="cc954-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc954-168">-Confirm</span></span>
<span data-ttu-id="cc954-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc954-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc954-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc954-170">-WhatIf</span></span>
<span data-ttu-id="cc954-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc954-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc954-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc954-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc954-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc954-173">CommonParameters</span></span>
<span data-ttu-id="cc954-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc954-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc954-175">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc954-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc954-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc954-176">INPUTS</span></span>

### <span data-ttu-id="cc954-177">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="cc954-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="cc954-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc954-178">OUTPUTS</span></span>

### <span data-ttu-id="cc954-179">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="cc954-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="cc954-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc954-180">NOTES</span></span>

## <span data-ttu-id="cc954-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc954-181">RELATED LINKS</span></span>
