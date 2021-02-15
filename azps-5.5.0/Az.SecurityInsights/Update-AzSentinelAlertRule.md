---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 56f1878507424c1396130aa91a5fc7b086f101c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114517"
---
# <span data-ttu-id="21bf1-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="21bf1-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="21bf1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="21bf1-103">Criar uma Analytic (Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="21bf1-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="21bf1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21bf1-104">SYNTAX</span></span>

### <span data-ttu-id="21bf1-105">AlertRuleId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="21bf1-105">AlertRuleId (Default)</span></span>
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

### <span data-ttu-id="21bf1-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="21bf1-106">InputObject</span></span>
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

### <span data-ttu-id="21bf1-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="21bf1-107">ResourceId</span></span>
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

## <span data-ttu-id="21bf1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="21bf1-108">DESCRIPTION</span></span>
<span data-ttu-id="21bf1-109">O cmdlet **Update-AzSentinelAlertRule** atualiza uma Analytic (Regra de Alerta) no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="21bf1-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="21bf1-110">Você pode usar um -InputObject ou -ResourceId ou -AlertId.</span><span class="sxs-lookup"><span data-stu-id="21bf1-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="21bf1-111">Você pode atualizar 1 ou mais parmaters de proprtery.</span><span class="sxs-lookup"><span data-stu-id="21bf1-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="21bf1-112">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="21bf1-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="21bf1-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21bf1-113">EXAMPLES</span></span>

### <span data-ttu-id="21bf1-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21bf1-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="21bf1-115">Este exemplo atualiza um **AlertRule** configurando-o como *Desabilitado* e renomeia para *Disabled-AlertRuleDisplayName.*</span><span class="sxs-lookup"><span data-stu-id="21bf1-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="21bf1-116">Todas as outras propriedades permanecerão as mesmas.</span><span class="sxs-lookup"><span data-stu-id="21bf1-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="21bf1-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="21bf1-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="21bf1-118">Este exemplo atualiza um **AlertRule** usando uma configuração InputObject como *Desabilitada.*</span><span class="sxs-lookup"><span data-stu-id="21bf1-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="21bf1-119">Todas as outras propriedades permanecerão as mesmas.</span><span class="sxs-lookup"><span data-stu-id="21bf1-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="21bf1-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21bf1-120">PARAMETERS</span></span>

### <span data-ttu-id="21bf1-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="21bf1-121">-AlertRuleId</span></span>
<span data-ttu-id="21bf1-122">ID da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="21bf1-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="21bf1-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="21bf1-124">Modelo de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="21bf1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21bf1-125">-DefaultProfile</span></span>
<span data-ttu-id="21bf1-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21bf1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21bf1-127">-Descrição</span><span class="sxs-lookup"><span data-stu-id="21bf1-127">-Description</span></span>
<span data-ttu-id="21bf1-128">Descrição.</span><span class="sxs-lookup"><span data-stu-id="21bf1-128">Description.</span></span>

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

### <span data-ttu-id="21bf1-129">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="21bf1-129">-Disabled</span></span>
<span data-ttu-id="21bf1-130">Regra de alerta desabilitada.</span><span class="sxs-lookup"><span data-stu-id="21bf1-130">Alert Rule Disabled.</span></span>

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

### <span data-ttu-id="21bf1-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="21bf1-131">-DisplayName</span></span>
<span data-ttu-id="21bf1-132">Nome de exibição da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="21bf1-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="21bf1-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="21bf1-134">Filtro de Exibição de Nomes de Exibição da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-134">Alert Rule Display Names Exclude Filter.</span></span>

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

### <span data-ttu-id="21bf1-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="21bf1-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="21bf1-136">Filtro de Nomes de Exibição da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-136">Alert Rule Display Names Filter.</span></span>

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

### <span data-ttu-id="21bf1-137">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="21bf1-137">-Enabled</span></span>
<span data-ttu-id="21bf1-138">Regra de Alerta Habilitada.</span><span class="sxs-lookup"><span data-stu-id="21bf1-138">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="21bf1-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21bf1-139">-InputObject</span></span>
<span data-ttu-id="21bf1-140">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="21bf1-140">InputObject.</span></span>

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

### <span data-ttu-id="21bf1-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="21bf1-141">-ProductFilter</span></span>
<span data-ttu-id="21bf1-142">Filtro de Produto da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-142">Alert Rule Product Filter.</span></span>

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

### <span data-ttu-id="21bf1-143">-Consulta</span><span class="sxs-lookup"><span data-stu-id="21bf1-143">-Query</span></span>
<span data-ttu-id="21bf1-144">Consulta de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="21bf1-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="21bf1-145">-QueryFrequency</span></span>
<span data-ttu-id="21bf1-146">Alert Rule Query Frequency.</span><span class="sxs-lookup"><span data-stu-id="21bf1-146">Alert Rule Query Frequency.</span></span>

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

### <span data-ttu-id="21bf1-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="21bf1-147">-QueryPeriod</span></span>
<span data-ttu-id="21bf1-148">Período de Consulta da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-148">Alert Rule Query Period.</span></span>

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

### <span data-ttu-id="21bf1-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21bf1-149">-ResourceGroupName</span></span>
<span data-ttu-id="21bf1-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21bf1-150">Resource group name.</span></span>

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

### <span data-ttu-id="21bf1-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21bf1-151">-ResourceId</span></span>
<span data-ttu-id="21bf1-152">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="21bf1-152">Resource Id.</span></span>

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

### <span data-ttu-id="21bf1-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="21bf1-153">-SeveritiesFilter</span></span>
<span data-ttu-id="21bf1-154">Filtro de Gravidades da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-154">Alert Rule Severities Filter.</span></span>

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

### <span data-ttu-id="21bf1-155">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="21bf1-155">-Severity</span></span>
<span data-ttu-id="21bf1-156">Gravidade do Incidente.</span><span class="sxs-lookup"><span data-stu-id="21bf1-156">Incident Severity.</span></span>

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

### <span data-ttu-id="21bf1-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="21bf1-157">-SuppressionDisabled</span></span>
<span data-ttu-id="21bf1-158">Suprimição de Regra de Alerta Desabilitada.</span><span class="sxs-lookup"><span data-stu-id="21bf1-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="21bf1-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="21bf1-159">-SuppressionDuration</span></span>
<span data-ttu-id="21bf1-160">Duração da Suprimição da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-160">Alert Rule Suppression Duration.</span></span>

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

### <span data-ttu-id="21bf1-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="21bf1-161">-SuppressionEnabled</span></span>
<span data-ttu-id="21bf1-162">Suprimição de Regra de Alerta Habilitada.</span><span class="sxs-lookup"><span data-stu-id="21bf1-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="21bf1-163">-Táticas</span><span class="sxs-lookup"><span data-stu-id="21bf1-163">-Tactics</span></span>
<span data-ttu-id="21bf1-164">Alertar As Táticas das Regras.</span><span class="sxs-lookup"><span data-stu-id="21bf1-164">Alert Rule Tactics.</span></span>

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

### <span data-ttu-id="21bf1-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="21bf1-165">-TriggerOperator</span></span>
<span data-ttu-id="21bf1-166">Operador de Gatilho de Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-166">Alert Rule Trigger Operator.</span></span>

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

### <span data-ttu-id="21bf1-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="21bf1-167">-TriggerThreshold</span></span>
<span data-ttu-id="21bf1-168">Limite do Gatilho da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="21bf1-168">Alert Rule Trigger Threshold.</span></span>

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

### <span data-ttu-id="21bf1-169">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="21bf1-169">-WorkspaceName</span></span>
<span data-ttu-id="21bf1-170">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="21bf1-170">Workspace Name.</span></span>

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

### <span data-ttu-id="21bf1-171">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="21bf1-171">-Confirm</span></span>
<span data-ttu-id="21bf1-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21bf1-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21bf1-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21bf1-173">-WhatIf</span></span>
<span data-ttu-id="21bf1-174">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="21bf1-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21bf1-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21bf1-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21bf1-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21bf1-176">CommonParameters</span></span>
<span data-ttu-id="21bf1-177">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21bf1-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21bf1-178">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21bf1-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21bf1-179">Entradas</span><span class="sxs-lookup"><span data-stu-id="21bf1-179">INPUTS</span></span>

### <span data-ttu-id="21bf1-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="21bf1-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="21bf1-181">System.String</span><span class="sxs-lookup"><span data-stu-id="21bf1-181">System.String</span></span>

## <span data-ttu-id="21bf1-182">Saídas</span><span class="sxs-lookup"><span data-stu-id="21bf1-182">OUTPUTS</span></span>

### <span data-ttu-id="21bf1-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="21bf1-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="21bf1-184">Notas</span><span class="sxs-lookup"><span data-stu-id="21bf1-184">NOTES</span></span>

## <span data-ttu-id="21bf1-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21bf1-185">RELATED LINKS</span></span>
