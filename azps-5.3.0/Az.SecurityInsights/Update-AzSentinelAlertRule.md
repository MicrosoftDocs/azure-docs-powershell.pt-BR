---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433188"
---
# <span data-ttu-id="670d5-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="670d5-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="670d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="670d5-102">SYNOPSIS</span></span>
<span data-ttu-id="670d5-103">Criar uma análise (regra de alerta).</span><span class="sxs-lookup"><span data-stu-id="670d5-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="670d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="670d5-104">SYNTAX</span></span>

### <span data-ttu-id="670d5-105">AlertRuleId (padrão)</span><span class="sxs-lookup"><span data-stu-id="670d5-105">AlertRuleId (Default)</span></span>
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

### <span data-ttu-id="670d5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="670d5-106">InputObject</span></span>
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

### <span data-ttu-id="670d5-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="670d5-107">ResourceId</span></span>
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

## <span data-ttu-id="670d5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="670d5-108">DESCRIPTION</span></span>
<span data-ttu-id="670d5-109">O cmdlet **Update-AzSentinelAlertRule** atualiza um analítico (regra de alerta) no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="670d5-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="670d5-110">Você pode usar um-InputObject ou-ResourceId ou-Alertid.</span><span class="sxs-lookup"><span data-stu-id="670d5-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="670d5-111">Você pode atualizar uma ou mais proprtery parmaters.</span><span class="sxs-lookup"><span data-stu-id="670d5-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="670d5-112">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="670d5-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="670d5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="670d5-113">EXAMPLES</span></span>

### <span data-ttu-id="670d5-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="670d5-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="670d5-115">Este exemplo atualiza um **AlertRule** definindo-o como *Disabled* e renomeia como *Disabled-AlertRuleDisplayName*.</span><span class="sxs-lookup"><span data-stu-id="670d5-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="670d5-116">Todas as outras propriedades continuarão as mesmas.</span><span class="sxs-lookup"><span data-stu-id="670d5-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="670d5-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="670d5-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="670d5-118">Este exemplo atualiza um **AlertRule** usando um InputObject definindo-o como *Disabled*.</span><span class="sxs-lookup"><span data-stu-id="670d5-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="670d5-119">Todas as outras propriedades continuarão as mesmas.</span><span class="sxs-lookup"><span data-stu-id="670d5-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="670d5-120">OS</span><span class="sxs-lookup"><span data-stu-id="670d5-120">PARAMETERS</span></span>

### <span data-ttu-id="670d5-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="670d5-121">-AlertRuleId</span></span>
<span data-ttu-id="670d5-122">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="670d5-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="670d5-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="670d5-124">Modelo de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="670d5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670d5-125">-DefaultProfile</span></span>
<span data-ttu-id="670d5-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="670d5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="670d5-127">-Descrição</span><span class="sxs-lookup"><span data-stu-id="670d5-127">-Description</span></span>
<span data-ttu-id="670d5-128">Descritivo.</span><span class="sxs-lookup"><span data-stu-id="670d5-128">Description.</span></span>

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

### <span data-ttu-id="670d5-129">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="670d5-129">-Disabled</span></span>
<span data-ttu-id="670d5-130">Regra de alerta desabilitada.</span><span class="sxs-lookup"><span data-stu-id="670d5-130">Alert Rule Disabled.</span></span>

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

### <span data-ttu-id="670d5-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="670d5-131">-DisplayName</span></span>
<span data-ttu-id="670d5-132">Nome de exibição da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="670d5-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="670d5-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="670d5-134">Nomes de exibição de regra de alerta excluir filtro.</span><span class="sxs-lookup"><span data-stu-id="670d5-134">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="670d5-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="670d5-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="670d5-136">Filtro de nomes para exibição de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-136">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="670d5-137">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="670d5-137">-Enabled</span></span>
<span data-ttu-id="670d5-138">Regra de alerta habilitada.</span><span class="sxs-lookup"><span data-stu-id="670d5-138">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="670d5-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="670d5-139">-InputObject</span></span>
<span data-ttu-id="670d5-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="670d5-140">InputObject.</span></span>

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

### <span data-ttu-id="670d5-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="670d5-141">-ProductFilter</span></span>
<span data-ttu-id="670d5-142">Filtro de produto regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="670d5-143">-Consulta</span><span class="sxs-lookup"><span data-stu-id="670d5-143">-Query</span></span>
<span data-ttu-id="670d5-144">Consulta de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="670d5-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="670d5-145">-QueryFrequency</span></span>
<span data-ttu-id="670d5-146">Frequência de consulta de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="670d5-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="670d5-147">-QueryPeriod</span></span>
<span data-ttu-id="670d5-148">Período da consulta regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="670d5-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670d5-149">-ResourceGroupName</span></span>
<span data-ttu-id="670d5-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="670d5-150">Resource group name.</span></span>

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

### <span data-ttu-id="670d5-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="670d5-151">-ResourceId</span></span>
<span data-ttu-id="670d5-152">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="670d5-152">Resource Id.</span></span>

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

### <span data-ttu-id="670d5-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="670d5-153">-SeveritiesFilter</span></span>
<span data-ttu-id="670d5-154">Filtro de severidades de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="670d5-155">-Severidade</span><span class="sxs-lookup"><span data-stu-id="670d5-155">-Severity</span></span>
<span data-ttu-id="670d5-156">Severidade do incidente.</span><span class="sxs-lookup"><span data-stu-id="670d5-156">Incident Severity.</span></span>

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

### <span data-ttu-id="670d5-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="670d5-157">-SuppressionDisabled</span></span>
<span data-ttu-id="670d5-158">Supressão de regra de alerta desabilitada.</span><span class="sxs-lookup"><span data-stu-id="670d5-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="670d5-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="670d5-159">-SuppressionDuration</span></span>
<span data-ttu-id="670d5-160">Duração da supressão da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-160">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="670d5-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="670d5-161">-SuppressionEnabled</span></span>
<span data-ttu-id="670d5-162">Supressão de regra de alerta habilitada.</span><span class="sxs-lookup"><span data-stu-id="670d5-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="670d5-163">-Táticas</span><span class="sxs-lookup"><span data-stu-id="670d5-163">-Tactics</span></span>
<span data-ttu-id="670d5-164">Táticas de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-164">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="670d5-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="670d5-165">-TriggerOperator</span></span>
<span data-ttu-id="670d5-166">Operador de gatilho de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-166">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="670d5-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="670d5-167">-TriggerThreshold</span></span>
<span data-ttu-id="670d5-168">Limite de gatilho de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="670d5-168">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="670d5-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="670d5-169">-WorkspaceName</span></span>
<span data-ttu-id="670d5-170">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="670d5-170">Workspace Name.</span></span>

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

### <span data-ttu-id="670d5-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="670d5-171">-Confirm</span></span>
<span data-ttu-id="670d5-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="670d5-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="670d5-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670d5-173">-WhatIf</span></span>
<span data-ttu-id="670d5-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="670d5-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="670d5-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="670d5-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="670d5-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670d5-176">CommonParameters</span></span>
<span data-ttu-id="670d5-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670d5-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670d5-178">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="670d5-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670d5-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="670d5-179">INPUTS</span></span>

### <span data-ttu-id="670d5-180">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="670d5-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="670d5-181">System. String</span><span class="sxs-lookup"><span data-stu-id="670d5-181">System.String</span></span>

## <span data-ttu-id="670d5-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="670d5-182">OUTPUTS</span></span>

### <span data-ttu-id="670d5-183">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="670d5-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="670d5-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="670d5-184">NOTES</span></span>

## <span data-ttu-id="670d5-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="670d5-185">RELATED LINKS</span></span>
