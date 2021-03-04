---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 0efb30f9c740362ac6e8c432179599c7d4aef88d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888432"
---
# <span data-ttu-id="52936-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="52936-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="52936-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52936-102">SYNOPSIS</span></span>
<span data-ttu-id="52936-103">Criar uma Análise (Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="52936-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="52936-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52936-104">SYNTAX</span></span>

### <span data-ttu-id="52936-105">ScheduledAlertRule (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52936-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52936-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="52936-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52936-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="52936-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52936-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52936-108">DESCRIPTION</span></span>
<span data-ttu-id="52936-109">O cmdlet **New-AzSentinelAlertRule** cria uma Analytic (Regra de Alerta) no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="52936-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="52936-110">Você deve especificar um dos três parâmetros, *Fusion*, *Scheduled* ou *MicrosoftSecurityIncidentCreation*, para especificar o tipo de regra de Alerta a ser criado.</span><span class="sxs-lookup"><span data-stu-id="52936-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="52936-111">Cada Tipo tem diferentes paramaters obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="52936-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="52936-112">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="52936-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="52936-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52936-113">EXAMPLES</span></span>

### <span data-ttu-id="52936-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52936-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="52936-115">Este exemplo cria um **AlertRule** do tipo *Fusion* com base no Modelo para Detecção Avançada de Ataques de *Vários* Estágios e o armazena na variável $AlertRule avançada.</span><span class="sxs-lookup"><span data-stu-id="52936-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="52936-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52936-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="52936-117">Este exemplo cria um **AlertRule** do tipo *MicrosoftSecurityIncidentCreation* com base no modelo para Criar incidentes com base no Centro de Segurança do *Azure para alertas de IoT* e o armazena no $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="52936-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="52936-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52936-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="52936-119">Este exemplo cria um **DataConnector** do tipo *Scheduled* e o armazena no $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="52936-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="52936-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52936-120">PARAMETERS</span></span>

### <span data-ttu-id="52936-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="52936-121">-AlertRuleId</span></span>
<span data-ttu-id="52936-122">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="52936-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="52936-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="52936-124">Modelo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52936-125">-DefaultProfile</span></span>
<span data-ttu-id="52936-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52936-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52936-127">-Description</span><span class="sxs-lookup"><span data-stu-id="52936-127">-Description</span></span>
<span data-ttu-id="52936-128">Descrição.</span><span class="sxs-lookup"><span data-stu-id="52936-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52936-129">-DisplayName</span></span>
<span data-ttu-id="52936-130">Nome de exibição da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="52936-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="52936-132">Nomes de exibição de regra de alerta excluem filtro.</span><span class="sxs-lookup"><span data-stu-id="52936-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="52936-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="52936-134">Filtro de Nomes de Exibição de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-135">-Enabled</span><span class="sxs-lookup"><span data-stu-id="52936-135">-Enabled</span></span>
<span data-ttu-id="52936-136">Regra de alerta Habilitada.</span><span class="sxs-lookup"><span data-stu-id="52936-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="52936-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="52936-137">-Fusion</span></span>
<span data-ttu-id="52936-138">Tipo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="52936-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="52936-140">Tipo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="52936-141">-ProductFilter</span></span>
<span data-ttu-id="52936-142">Alert Rule Product Filter.</span><span class="sxs-lookup"><span data-stu-id="52936-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-143">-Query</span><span class="sxs-lookup"><span data-stu-id="52936-143">-Query</span></span>
<span data-ttu-id="52936-144">Consulta de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="52936-145">-QueryFrequency</span></span>
<span data-ttu-id="52936-146">Alert Rule Query Frequency.</span><span class="sxs-lookup"><span data-stu-id="52936-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="52936-147">-QueryPeriod</span></span>
<span data-ttu-id="52936-148">Período de consulta de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52936-149">-ResourceGroupName</span></span>
<span data-ttu-id="52936-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52936-150">Resource group name.</span></span>

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

### <span data-ttu-id="52936-151">-Scheduled</span><span class="sxs-lookup"><span data-stu-id="52936-151">-Scheduled</span></span>
<span data-ttu-id="52936-152">Tipo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="52936-153">-SeveritiesFilter</span></span>
<span data-ttu-id="52936-154">Filtro de Severidades de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-155">-Severity</span><span class="sxs-lookup"><span data-stu-id="52936-155">-Severity</span></span>
<span data-ttu-id="52936-156">Gravidade do incidente.</span><span class="sxs-lookup"><span data-stu-id="52936-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="52936-157">-SuppressionDuration</span></span>
<span data-ttu-id="52936-158">Duração da Supressão de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="52936-159">-SuppressionEnabled</span></span>
<span data-ttu-id="52936-160">Supressão de Regra de Alerta Habilitada.</span><span class="sxs-lookup"><span data-stu-id="52936-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-161">-Tactics</span><span class="sxs-lookup"><span data-stu-id="52936-161">-Tactics</span></span>
<span data-ttu-id="52936-162">Alert Rule Tactics.</span><span class="sxs-lookup"><span data-stu-id="52936-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="52936-163">-TriggerOperator</span></span>
<span data-ttu-id="52936-164">Operador de Gatilho de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="52936-165">-TriggerThreshold</span></span>
<span data-ttu-id="52936-166">Limite de gatilho de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="52936-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52936-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52936-167">-WorkspaceName</span></span>
<span data-ttu-id="52936-168">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="52936-168">Workspace Name.</span></span>

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

### <span data-ttu-id="52936-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52936-169">-Confirm</span></span>
<span data-ttu-id="52936-170">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52936-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52936-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52936-171">-WhatIf</span></span>
<span data-ttu-id="52936-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52936-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52936-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52936-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52936-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52936-174">CommonParameters</span></span>
<span data-ttu-id="52936-175">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52936-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52936-176">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52936-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52936-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52936-177">INPUTS</span></span>

### <span data-ttu-id="52936-178">Nenhum</span><span class="sxs-lookup"><span data-stu-id="52936-178">None</span></span>
## <span data-ttu-id="52936-179">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52936-179">OUTPUTS</span></span>

### <span data-ttu-id="52936-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="52936-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="52936-181">NOTES</span><span class="sxs-lookup"><span data-stu-id="52936-181">NOTES</span></span>

## <span data-ttu-id="52936-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52936-182">RELATED LINKS</span></span>
