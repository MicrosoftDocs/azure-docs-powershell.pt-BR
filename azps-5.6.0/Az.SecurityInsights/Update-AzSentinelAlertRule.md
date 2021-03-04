---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 86b6067e13a7b4d1d90e8fcb3d308af797dab354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887621"
---
# <span data-ttu-id="37bd0-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="37bd0-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="37bd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="37bd0-103">Criar uma Análise (Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="37bd0-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="37bd0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37bd0-104">SYNTAX</span></span>

### <span data-ttu-id="37bd0-105">AlertRuleId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="37bd0-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37bd0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="37bd0-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37bd0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="37bd0-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37bd0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37bd0-108">DESCRIPTION</span></span>
<span data-ttu-id="37bd0-109">O cmdlet **Update-AzSentinelAlertRule** atualiza uma Analytic (Regra de Alerta) no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="37bd0-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="37bd0-110">Você pode usar um -InputObject ou -ResourceId ou -AlertId.</span><span class="sxs-lookup"><span data-stu-id="37bd0-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="37bd0-111">Você pode atualizar 1 ou mais parmaters de proprtery.</span><span class="sxs-lookup"><span data-stu-id="37bd0-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="37bd0-112">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="37bd0-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="37bd0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37bd0-113">EXAMPLES</span></span>

### <span data-ttu-id="37bd0-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37bd0-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="37bd0-115">Este exemplo atualiza uma **configuração AlertRule** como *Desabilitada* e renomeia para *Disabled-AlertRuleDisplayName*.</span><span class="sxs-lookup"><span data-stu-id="37bd0-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="37bd0-116">Todas as outras propriedades permanecerão as mesmas.</span><span class="sxs-lookup"><span data-stu-id="37bd0-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="37bd0-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="37bd0-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="37bd0-118">Este exemplo atualiza um **AlertRule** usando uma configuração InputObject como *Disabled*.</span><span class="sxs-lookup"><span data-stu-id="37bd0-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="37bd0-119">Todas as outras propriedades permanecerão as mesmas.</span><span class="sxs-lookup"><span data-stu-id="37bd0-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="37bd0-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37bd0-120">PARAMETERS</span></span>

### <span data-ttu-id="37bd0-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="37bd0-121">-AlertRuleId</span></span>
<span data-ttu-id="37bd0-122">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="37bd0-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="37bd0-124">Modelo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-124">Alert Rule Template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37bd0-125">-DefaultProfile</span></span>
<span data-ttu-id="37bd0-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37bd0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-127">-Description</span><span class="sxs-lookup"><span data-stu-id="37bd0-127">-Description</span></span>
<span data-ttu-id="37bd0-128">Descrição.</span><span class="sxs-lookup"><span data-stu-id="37bd0-128">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="37bd0-129">-Disabled</span></span>
<span data-ttu-id="37bd0-130">Regra de alerta desabilitada.</span><span class="sxs-lookup"><span data-stu-id="37bd0-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="37bd0-131">-DisplayName</span></span>
<span data-ttu-id="37bd0-132">Nome de exibição da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-132">Alert Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="37bd0-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="37bd0-134">Nomes de exibição de regra de alerta excluem filtro.</span><span class="sxs-lookup"><span data-stu-id="37bd0-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="37bd0-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="37bd0-136">Filtro de Nomes de Exibição de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-137">-Enabled</span><span class="sxs-lookup"><span data-stu-id="37bd0-137">-Enabled</span></span>
<span data-ttu-id="37bd0-138">Regra de alerta Habilitada.</span><span class="sxs-lookup"><span data-stu-id="37bd0-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37bd0-139">-InputObject</span></span>
<span data-ttu-id="37bd0-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="37bd0-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="37bd0-141">-ProductFilter</span></span>
<span data-ttu-id="37bd0-142">Alert Rule Product Filter.</span><span class="sxs-lookup"><span data-stu-id="37bd0-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-143">-Query</span><span class="sxs-lookup"><span data-stu-id="37bd0-143">-Query</span></span>
<span data-ttu-id="37bd0-144">Consulta de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-144">Alert Rule Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="37bd0-145">-QueryFrequency</span></span>
<span data-ttu-id="37bd0-146">Alert Rule Query Frequency.</span><span class="sxs-lookup"><span data-stu-id="37bd0-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="37bd0-147">-QueryPeriod</span></span>
<span data-ttu-id="37bd0-148">Período de consulta de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37bd0-149">-ResourceGroupName</span></span>
<span data-ttu-id="37bd0-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37bd0-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37bd0-151">-ResourceId</span></span>
<span data-ttu-id="37bd0-152">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="37bd0-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="37bd0-153">-SeveritiesFilter</span></span>
<span data-ttu-id="37bd0-154">Filtro de Severidades de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-155">-Severity</span><span class="sxs-lookup"><span data-stu-id="37bd0-155">-Severity</span></span>
<span data-ttu-id="37bd0-156">Gravidade do incidente.</span><span class="sxs-lookup"><span data-stu-id="37bd0-156">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="37bd0-157">-SuppressionDisabled</span></span>
<span data-ttu-id="37bd0-158">Supressão de Regra de Alerta Desabilitada.</span><span class="sxs-lookup"><span data-stu-id="37bd0-158">Alert Rule Suppression Disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="37bd0-159">-SuppressionDuration</span></span>
<span data-ttu-id="37bd0-160">Duração da Supressão de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="37bd0-161">-SuppressionEnabled</span></span>
<span data-ttu-id="37bd0-162">Supressão de Regra de Alerta Habilitada.</span><span class="sxs-lookup"><span data-stu-id="37bd0-162">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-163">-Tactics</span><span class="sxs-lookup"><span data-stu-id="37bd0-163">-Tactics</span></span>
<span data-ttu-id="37bd0-164">Alert Rule Tactics.</span><span class="sxs-lookup"><span data-stu-id="37bd0-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="37bd0-165">-TriggerOperator</span></span>
<span data-ttu-id="37bd0-166">Operador de Gatilho de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="37bd0-167">-TriggerThreshold</span></span>
<span data-ttu-id="37bd0-168">Limite de gatilho de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="37bd0-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37bd0-169">-WorkspaceName</span></span>
<span data-ttu-id="37bd0-170">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="37bd0-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37bd0-171">-Confirm</span></span>
<span data-ttu-id="37bd0-172">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37bd0-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37bd0-173">-WhatIf</span></span>
<span data-ttu-id="37bd0-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37bd0-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37bd0-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37bd0-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd0-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37bd0-176">CommonParameters</span></span>
<span data-ttu-id="37bd0-177">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37bd0-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37bd0-178">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37bd0-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37bd0-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37bd0-179">INPUTS</span></span>

### <span data-ttu-id="37bd0-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="37bd0-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="37bd0-181">System.String</span><span class="sxs-lookup"><span data-stu-id="37bd0-181">System.String</span></span>

## <span data-ttu-id="37bd0-182">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37bd0-182">OUTPUTS</span></span>

### <span data-ttu-id="37bd0-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="37bd0-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="37bd0-184">NOTES</span><span class="sxs-lookup"><span data-stu-id="37bd0-184">NOTES</span></span>

## <span data-ttu-id="37bd0-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37bd0-185">RELATED LINKS</span></span>
