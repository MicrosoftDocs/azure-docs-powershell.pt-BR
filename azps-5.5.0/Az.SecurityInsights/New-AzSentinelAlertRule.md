---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117157"
---
# <span data-ttu-id="f2152-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="f2152-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="f2152-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2152-102">SYNOPSIS</span></span>
<span data-ttu-id="f2152-103">Criar uma Analytic (Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="f2152-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="f2152-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2152-104">SYNTAX</span></span>

### <span data-ttu-id="f2152-105">ScheduledAlertRule (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2152-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2152-106">NeuralAlertRule</span><span class="sxs-lookup"><span data-stu-id="f2152-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2152-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="f2152-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2152-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2152-108">DESCRIPTION</span></span>
<span data-ttu-id="f2152-109">O cmdlet **New-AzSentinelAlertRule** cria uma Analytic (Regra de Alerta) no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="f2152-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="f2152-110">Você deve especificar um dos três  parâmetros, Seja qual deles, *Seja Qual* é o padrão, Agendado ou *MicrosoftSecurityIncidentCreation,* para especificar o tipo de regra de Alerta a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f2152-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="f2152-111">Cada Tipo tem diferentes paramaters necessários.</span><span class="sxs-lookup"><span data-stu-id="f2152-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="f2152-112">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="f2152-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f2152-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2152-113">EXAMPLES</span></span>

### <span data-ttu-id="f2152-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2152-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="f2152-115">Este exemplo cria um **AlertRule** do tipo *Denúm* com base no Modelo para Detecção Avançada de Ataque *Multiestocado* e, em seguida, o armazena na variável $AlertRule dados.</span><span class="sxs-lookup"><span data-stu-id="f2152-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="f2152-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f2152-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="f2152-117">Este exemplo cria um **AlertRule** do tipo *MicrosoftSecurityIncidentCreation* com base no modelo para Criar incidentes com base no Centro de Segurança do *Azure para alertas de IoT* e, em seguida, armazena-o no $AlertRule varaible.</span><span class="sxs-lookup"><span data-stu-id="f2152-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="f2152-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f2152-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="f2152-119">Este exemplo cria um **DataConnector** do tipo Agendado e o armazena no $AlertRule varaible. </span><span class="sxs-lookup"><span data-stu-id="f2152-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="f2152-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2152-120">PARAMETERS</span></span>

### <span data-ttu-id="f2152-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="f2152-121">-AlertRuleId</span></span>
<span data-ttu-id="f2152-122">ID da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="f2152-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="f2152-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="f2152-124">Modelo de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="f2152-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2152-125">-DefaultProfile</span></span>
<span data-ttu-id="f2152-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2152-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2152-127">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f2152-127">-Description</span></span>
<span data-ttu-id="f2152-128">Descrição.</span><span class="sxs-lookup"><span data-stu-id="f2152-128">Description.</span></span>

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

### <span data-ttu-id="f2152-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f2152-129">-DisplayName</span></span>
<span data-ttu-id="f2152-130">Nome de exibição da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-130">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="f2152-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="f2152-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="f2152-132">Filtro de Exibição de Nomes de Exibição da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-132">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="f2152-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="f2152-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="f2152-134">Filtro de Nomes de Exibição da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-134">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="f2152-135">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="f2152-135">-Enabled</span></span>
<span data-ttu-id="f2152-136">Regra de Alerta Habilitada.</span><span class="sxs-lookup"><span data-stu-id="f2152-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="f2152-137">-Ltda</span><span class="sxs-lookup"><span data-stu-id="f2152-137">-Fusion</span></span>
<span data-ttu-id="f2152-138">Tipo de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-138">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="f2152-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="f2152-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="f2152-140">Tipo de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-140">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="f2152-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="f2152-141">-ProductFilter</span></span>
<span data-ttu-id="f2152-142">Filtro de Produto da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="f2152-143">-Consulta</span><span class="sxs-lookup"><span data-stu-id="f2152-143">-Query</span></span>
<span data-ttu-id="f2152-144">Consulta de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="f2152-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="f2152-145">-QueryFrequency</span></span>
<span data-ttu-id="f2152-146">Alert Rule Query Frequency.</span><span class="sxs-lookup"><span data-stu-id="f2152-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="f2152-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="f2152-147">-QueryPeriod</span></span>
<span data-ttu-id="f2152-148">Período de Consulta da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="f2152-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2152-149">-ResourceGroupName</span></span>
<span data-ttu-id="f2152-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2152-150">Resource group name.</span></span>

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

### <span data-ttu-id="f2152-151">-Agendado</span><span class="sxs-lookup"><span data-stu-id="f2152-151">-Scheduled</span></span>
<span data-ttu-id="f2152-152">Tipo de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-152">Alert Rule Kind.</span></span>

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

### <span data-ttu-id="f2152-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="f2152-153">-SeveritiesFilter</span></span>
<span data-ttu-id="f2152-154">Filtro de Gravidades da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="f2152-155">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="f2152-155">-Severity</span></span>
<span data-ttu-id="f2152-156">Gravidade do Incidente.</span><span class="sxs-lookup"><span data-stu-id="f2152-156">Incident Severity.</span></span>

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

### <span data-ttu-id="f2152-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="f2152-157">-SuppressionDuration</span></span>
<span data-ttu-id="f2152-158">Duração da Suprimição da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-158">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="f2152-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="f2152-159">-SuppressionEnabled</span></span>
<span data-ttu-id="f2152-160">Suprimição de Regra de Alerta Habilitada.</span><span class="sxs-lookup"><span data-stu-id="f2152-160">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="f2152-161">-Táticas</span><span class="sxs-lookup"><span data-stu-id="f2152-161">-Tactics</span></span>
<span data-ttu-id="f2152-162">Alertar As Táticas das Regras.</span><span class="sxs-lookup"><span data-stu-id="f2152-162">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="f2152-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="f2152-163">-TriggerOperator</span></span>
<span data-ttu-id="f2152-164">Operador de Gatilho de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-164">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="f2152-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="f2152-165">-TriggerThreshold</span></span>
<span data-ttu-id="f2152-166">Limite do Gatilho da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="f2152-166">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="f2152-167">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="f2152-167">-WorkspaceName</span></span>
<span data-ttu-id="f2152-168">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f2152-168">Workspace Name.</span></span>

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

### <span data-ttu-id="f2152-169">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f2152-169">-Confirm</span></span>
<span data-ttu-id="f2152-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2152-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2152-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2152-171">-WhatIf</span></span>
<span data-ttu-id="f2152-172">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f2152-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2152-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2152-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2152-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2152-174">CommonParameters</span></span>
<span data-ttu-id="f2152-175">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2152-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2152-176">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2152-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2152-177">Entradas</span><span class="sxs-lookup"><span data-stu-id="f2152-177">INPUTS</span></span>

### <span data-ttu-id="f2152-178">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f2152-178">None</span></span>
## <span data-ttu-id="f2152-179">Saídas</span><span class="sxs-lookup"><span data-stu-id="f2152-179">OUTPUTS</span></span>

### <span data-ttu-id="f2152-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="f2152-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="f2152-181">Notas</span><span class="sxs-lookup"><span data-stu-id="f2152-181">NOTES</span></span>

## <span data-ttu-id="f2152-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2152-182">RELATED LINKS</span></span>
