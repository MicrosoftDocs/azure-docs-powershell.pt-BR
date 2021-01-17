---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433210"
---
# <span data-ttu-id="d090a-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="d090a-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="d090a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d090a-102">SYNOPSIS</span></span>
<span data-ttu-id="d090a-103">Criar uma análise (regra de alerta).</span><span class="sxs-lookup"><span data-stu-id="d090a-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="d090a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d090a-104">SYNTAX</span></span>

### <span data-ttu-id="d090a-105">ScheduledAlertRule (padrão)</span><span class="sxs-lookup"><span data-stu-id="d090a-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d090a-106">FusionAlertRule</span><span class="sxs-lookup"><span data-stu-id="d090a-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d090a-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="d090a-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d090a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d090a-108">DESCRIPTION</span></span>
<span data-ttu-id="d090a-109">O cmdlet **New-AzSentinelAlertRule** cria uma análise (regra de alerta) no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="d090a-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="d090a-110">Você deve especificar um dos três parâmetros, *Fusion*, *Scheduled* ou *MicrosoftSecurityIncidentCreation* para especificar o tipo de regra de alerta a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d090a-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="d090a-111">Cada tipo tem parâmetros obrigatórios diferentes.</span><span class="sxs-lookup"><span data-stu-id="d090a-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="d090a-112">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="d090a-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d090a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d090a-113">EXAMPLES</span></span>

### <span data-ttu-id="d090a-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d090a-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="d090a-115">Este exemplo cria uma **AlertRule** do tipo *Fusion* com base no modelo para *detecção avançada de ataques de multiestágio* e, em seguida, armazena-o na variável $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="d090a-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="d090a-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d090a-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="d090a-117">Este exemplo cria uma **AlertRule** do tipo *MicrosoftSecurityIncidentCreation* com base no modelo para *criar incidentes com base na central de segurança do Azure para alertas IOT* e, em seguida, armazena-o no varaible de $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="d090a-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="d090a-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d090a-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="d090a-119">Este exemplo cria um **Dataconnecter** do tipo *agendado* e, em seguida, o armazena no $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="d090a-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="d090a-120">OS</span><span class="sxs-lookup"><span data-stu-id="d090a-120">PARAMETERS</span></span>

### <span data-ttu-id="d090a-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="d090a-121">-AlertRuleId</span></span>
<span data-ttu-id="d090a-122">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="d090a-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="d090a-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="d090a-124">Modelo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="d090a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d090a-125">-DefaultProfile</span></span>
<span data-ttu-id="d090a-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d090a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d090a-127">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d090a-127">-Description</span></span>
<span data-ttu-id="d090a-128">Descritivo.</span><span class="sxs-lookup"><span data-stu-id="d090a-128">Description.</span></span>

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

### <span data-ttu-id="d090a-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d090a-129">-DisplayName</span></span>
<span data-ttu-id="d090a-130">Nome de exibição da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-130">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="d090a-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="d090a-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="d090a-132">Nomes de exibição de regra de alerta excluir filtro.</span><span class="sxs-lookup"><span data-stu-id="d090a-132">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="d090a-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="d090a-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="d090a-134">Filtro de nomes para exibição de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-134">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="d090a-135">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="d090a-135">-Enabled</span></span>
<span data-ttu-id="d090a-136">Regra de alerta habilitada.</span><span class="sxs-lookup"><span data-stu-id="d090a-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="d090a-137">-Fusion</span><span class="sxs-lookup"><span data-stu-id="d090a-137">-Fusion</span></span>
<span data-ttu-id="d090a-138">Tipo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-138">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="d090a-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="d090a-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="d090a-140">Tipo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-140">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="d090a-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="d090a-141">-ProductFilter</span></span>
<span data-ttu-id="d090a-142">Filtro de produto regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="d090a-143">-Consulta</span><span class="sxs-lookup"><span data-stu-id="d090a-143">-Query</span></span>
<span data-ttu-id="d090a-144">Consulta de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="d090a-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="d090a-145">-QueryFrequency</span></span>
<span data-ttu-id="d090a-146">Frequência de consulta de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="d090a-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="d090a-147">-QueryPeriod</span></span>
<span data-ttu-id="d090a-148">Período da consulta regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="d090a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d090a-149">-ResourceGroupName</span></span>
<span data-ttu-id="d090a-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d090a-150">Resource group name.</span></span>

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

### <span data-ttu-id="d090a-151">-Programado</span><span class="sxs-lookup"><span data-stu-id="d090a-151">-Scheduled</span></span>
<span data-ttu-id="d090a-152">Tipo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-152">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="d090a-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="d090a-153">-SeveritiesFilter</span></span>
<span data-ttu-id="d090a-154">Filtro de severidades de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="d090a-155">-Severidade</span><span class="sxs-lookup"><span data-stu-id="d090a-155">-Severity</span></span>
<span data-ttu-id="d090a-156">Severidade do incidente.</span><span class="sxs-lookup"><span data-stu-id="d090a-156">Incident Severity.</span></span>

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

### <span data-ttu-id="d090a-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="d090a-157">-SuppressionDuration</span></span>
<span data-ttu-id="d090a-158">Duração da supressão da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-158">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="d090a-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="d090a-159">-SuppressionEnabled</span></span>
<span data-ttu-id="d090a-160">Supressão de regra de alerta habilitada.</span><span class="sxs-lookup"><span data-stu-id="d090a-160">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="d090a-161">-Táticas</span><span class="sxs-lookup"><span data-stu-id="d090a-161">-Tactics</span></span>
<span data-ttu-id="d090a-162">Táticas de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-162">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="d090a-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="d090a-163">-TriggerOperator</span></span>
<span data-ttu-id="d090a-164">Operador de gatilho de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-164">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="d090a-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="d090a-165">-TriggerThreshold</span></span>
<span data-ttu-id="d090a-166">Limite de gatilho de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="d090a-166">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="d090a-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d090a-167">-WorkspaceName</span></span>
<span data-ttu-id="d090a-168">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d090a-168">Workspace Name.</span></span>

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

### <span data-ttu-id="d090a-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d090a-169">-Confirm</span></span>
<span data-ttu-id="d090a-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d090a-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d090a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d090a-171">-WhatIf</span></span>
<span data-ttu-id="d090a-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d090a-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d090a-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d090a-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d090a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d090a-174">CommonParameters</span></span>
<span data-ttu-id="d090a-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d090a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d090a-176">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d090a-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d090a-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d090a-177">INPUTS</span></span>

### <span data-ttu-id="d090a-178">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d090a-178">None</span></span>
## <span data-ttu-id="d090a-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d090a-179">OUTPUTS</span></span>

### <span data-ttu-id="d090a-180">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="d090a-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="d090a-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d090a-181">NOTES</span></span>

## <span data-ttu-id="d090a-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d090a-182">RELATED LINKS</span></span>
