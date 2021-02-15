---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 0317f21231edd2608492d37609ab4f4849ba9c20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117544"
---
# <span data-ttu-id="11710-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11710-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="11710-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11710-102">SYNOPSIS</span></span>
<span data-ttu-id="11710-103">Adiciona ou atualiza uma regra de alerta baseada em métrica V2 (não clássica).</span><span class="sxs-lookup"><span data-stu-id="11710-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="11710-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11710-104">SYNTAX</span></span>

### <span data-ttu-id="11710-105">CreateAlertByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11710-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11710-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="11710-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11710-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="11710-107">DESCRIPTION</span></span>
<span data-ttu-id="11710-108">Adiciona ou atualiza uma regra de alerta baseada em **métrica V2 (não** clássica).</span><span class="sxs-lookup"><span data-stu-id="11710-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="11710-109">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="11710-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="11710-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="11710-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="11710-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11710-111">EXAMPLES</span></span>

### <span data-ttu-id="11710-112">Exemplo 1: Adicionar uma regra de alerta métrica a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="11710-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="11710-113">Esse comando cria uma regra de alerta métrico para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11710-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="11710-114">$condition é a saída do cmdlet [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) e $act é a saída do cmdlet [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup)</span><span class="sxs-lookup"><span data-stu-id="11710-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="11710-115">Exemplo 2: Adicionar uma regra de alerta métrica para todas as máquinas virtuais em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="11710-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="11710-116">Esse comando cria uma regra de alerta métrico para todas as máquinas virtuais na assinatura que estão em eastus</span><span class="sxs-lookup"><span data-stu-id="11710-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="11710-117">Exemplo 3: Desabilitar uma regra de alerta métrico</span><span class="sxs-lookup"><span data-stu-id="11710-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="11710-118">Esse comando desabilita uma regra de alerta métrico.</span><span class="sxs-lookup"><span data-stu-id="11710-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="11710-119">Aqui, estamos fazendo a saída de [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) para [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="11710-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="11710-120">Exemplo 4: Adicionar uma regra de alerta métrica com dimensões</span><span class="sxs-lookup"><span data-stu-id="11710-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="11710-121">Para criar uma regra de alerta métrica mais complexa, como aquelas que envolvem a seleção de valores de dimensão ou que têm vários critérios, você pode usar os cmdlets auxiliares [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) [e New-AzMetricAlertRuleV2Criteria.](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="11710-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="11710-122">O conjunto acima de cmdlets criará uma regra de alerta métrica com dimensões.</span><span class="sxs-lookup"><span data-stu-id="11710-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="11710-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11710-123">PARAMETERS</span></span>

### <span data-ttu-id="11710-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="11710-124">-ActionGroup</span></span>
<span data-ttu-id="11710-125">O Grupo de Ações para regra</span><span class="sxs-lookup"><span data-stu-id="11710-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="11710-126">-ActionGroupId</span></span>
<span data-ttu-id="11710-127">A ID do Grupo de Ações para regra</span><span class="sxs-lookup"><span data-stu-id="11710-127">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-128">-Condição</span><span class="sxs-lookup"><span data-stu-id="11710-128">-Condition</span></span>
<span data-ttu-id="11710-129">A condição para a regra</span><span class="sxs-lookup"><span data-stu-id="11710-129">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11710-130">-DefaultProfile</span></span>
<span data-ttu-id="11710-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11710-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11710-132">-Descrição</span><span class="sxs-lookup"><span data-stu-id="11710-132">-Description</span></span>
<span data-ttu-id="11710-133">A descrição da regra de alerta métrico</span><span class="sxs-lookup"><span data-stu-id="11710-133">The description of the metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="11710-134">-DisableRule</span></span>
<span data-ttu-id="11710-135">O sinalizador desabilitar regra (status)</span><span class="sxs-lookup"><span data-stu-id="11710-135">The disable rule (status) flag</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-136">-Frequência</span><span class="sxs-lookup"><span data-stu-id="11710-136">-Frequency</span></span>
<span data-ttu-id="11710-137">A frequência de avaliação da regra</span><span class="sxs-lookup"><span data-stu-id="11710-137">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="11710-138">-Name</span></span>
<span data-ttu-id="11710-139">O nome da regra de alerta métrico</span><span class="sxs-lookup"><span data-stu-id="11710-139">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11710-140">-ResourceGroupName</span></span>
<span data-ttu-id="11710-141">O Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="11710-141">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-142">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="11710-142">-Severity</span></span>
<span data-ttu-id="11710-143">A gravidade da regra de alerta métrico</span><span class="sxs-lookup"><span data-stu-id="11710-143">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="11710-144">-TargetResourceId</span></span>
<span data-ttu-id="11710-145">A ID do recurso de destino para regra</span><span class="sxs-lookup"><span data-stu-id="11710-145">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="11710-146">-TargetResourceRegion</span></span>
<span data-ttu-id="11710-147">A região de recurso de destino da regra</span><span class="sxs-lookup"><span data-stu-id="11710-147">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="11710-148">-TargetResourceScope</span></span>
<span data-ttu-id="11710-149">O escopo do recurso de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="11710-149">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="11710-150">-TargetResourceType</span></span>
<span data-ttu-id="11710-151">O tipo de recurso de destino para regra</span><span class="sxs-lookup"><span data-stu-id="11710-151">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="11710-152">-WindowSize</span></span>
<span data-ttu-id="11710-153">O tamanho da janela da regra</span><span class="sxs-lookup"><span data-stu-id="11710-153">The window size for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11710-154">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="11710-154">-Confirm</span></span>
<span data-ttu-id="11710-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11710-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11710-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11710-156">-WhatIf</span></span>
<span data-ttu-id="11710-157">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="11710-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11710-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11710-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11710-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11710-159">CommonParameters</span></span>
<span data-ttu-id="11710-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11710-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11710-161">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11710-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11710-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="11710-162">INPUTS</span></span>

### <span data-ttu-id="11710-163">System.String</span><span class="sxs-lookup"><span data-stu-id="11710-163">System.String</span></span>

### <span data-ttu-id="11710-164">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="11710-164">System.TimeSpan</span></span>

### <span data-ttu-id="11710-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="11710-165">System.String[]</span></span>

### <span data-ttu-id="11710-166">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="11710-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="11710-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span><span class="sxs-lookup"><span data-stu-id="11710-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="11710-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="11710-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="11710-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="11710-169">System.Int32</span></span>

## <span data-ttu-id="11710-170">Saídas</span><span class="sxs-lookup"><span data-stu-id="11710-170">OUTPUTS</span></span>

### <span data-ttu-id="11710-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11710-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="11710-172">Notas</span><span class="sxs-lookup"><span data-stu-id="11710-172">NOTES</span></span>

## <span data-ttu-id="11710-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11710-173">RELATED LINKS</span></span>
