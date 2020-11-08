---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 0317f21231edd2608492d37609ab4f4849ba9c20
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125997"
---
# <span data-ttu-id="afc69-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="afc69-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="afc69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afc69-102">SYNOPSIS</span></span>
<span data-ttu-id="afc69-103">Adiciona ou atualiza uma regra de alerta baseada em métrica v2 (não clássico).</span><span class="sxs-lookup"><span data-stu-id="afc69-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="afc69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afc69-104">SYNTAX</span></span>

### <span data-ttu-id="afc69-105">CreateAlertByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="afc69-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afc69-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="afc69-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afc69-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afc69-107">DESCRIPTION</span></span>
<span data-ttu-id="afc69-108">Adiciona ou atualiza uma **regra de alerta baseada em métrica v2 (não clássico)**.</span><span class="sxs-lookup"><span data-stu-id="afc69-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="afc69-109">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="afc69-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="afc69-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="afc69-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="afc69-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afc69-111">EXAMPLES</span></span>

### <span data-ttu-id="afc69-112">Exemplo 1: adicionar uma regra de alerta de métrica a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="afc69-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="afc69-113">Esse comando cria uma regra de alerta métrica para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="afc69-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="afc69-114">$condition é a saída do cmdlet [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) e $Act é a saída do cmdlet [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup)</span><span class="sxs-lookup"><span data-stu-id="afc69-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="afc69-115">Exemplo 2: adicionar uma regra de alerta de métrica para todas as máquinas virtuais em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="afc69-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="afc69-116">Este comando cria uma regra de alerta métrica para todas as máquinas virtuais na assinatura do lesteus</span><span class="sxs-lookup"><span data-stu-id="afc69-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="afc69-117">Exemplo 3: desabilitar uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="afc69-117">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="afc69-118">Esse comando desabilita uma regra de alerta de métrica.</span><span class="sxs-lookup"><span data-stu-id="afc69-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="afc69-119">Aqui, estamos disparando a saída de [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) para [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="afc69-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="afc69-120">Exemplo 4: adicionar uma regra de alerta de métrica com dimensões</span><span class="sxs-lookup"><span data-stu-id="afc69-120">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="afc69-121">Para criar uma regra de alerta de métrica mais complexa, como aquelas que envolvem a seleção de valores de dimensão ou ter vários critérios, você pode usar os cmdlets auxiliar [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) e [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span><span class="sxs-lookup"><span data-stu-id="afc69-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="afc69-122">O conjunto de cmdlets acima criará uma regra de alerta métrica com dimensões.</span><span class="sxs-lookup"><span data-stu-id="afc69-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="afc69-123">OS</span><span class="sxs-lookup"><span data-stu-id="afc69-123">PARAMETERS</span></span>

### <span data-ttu-id="afc69-124">-Botão de ação</span><span class="sxs-lookup"><span data-stu-id="afc69-124">-ActionGroup</span></span>
<span data-ttu-id="afc69-125">O grupo ação para a regra</span><span class="sxs-lookup"><span data-stu-id="afc69-125">The Action Group for rule</span></span>

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

### <span data-ttu-id="afc69-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="afc69-126">-ActionGroupId</span></span>
<span data-ttu-id="afc69-127">A ID do grupo de ação para a regra</span><span class="sxs-lookup"><span data-stu-id="afc69-127">The Action Group id for rule</span></span>

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

### <span data-ttu-id="afc69-128">-Condition</span><span class="sxs-lookup"><span data-stu-id="afc69-128">-Condition</span></span>
<span data-ttu-id="afc69-129">A condição para a regra</span><span class="sxs-lookup"><span data-stu-id="afc69-129">The condition for rule</span></span>

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

### <span data-ttu-id="afc69-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc69-130">-DefaultProfile</span></span>
<span data-ttu-id="afc69-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afc69-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afc69-132">-Descrição</span><span class="sxs-lookup"><span data-stu-id="afc69-132">-Description</span></span>
<span data-ttu-id="afc69-133">A descrição da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="afc69-133">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="afc69-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="afc69-134">-DisableRule</span></span>
<span data-ttu-id="afc69-135">O sinalizador desabilitar regra (status)</span><span class="sxs-lookup"><span data-stu-id="afc69-135">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="afc69-136">-Frequency</span><span class="sxs-lookup"><span data-stu-id="afc69-136">-Frequency</span></span>
<span data-ttu-id="afc69-137">A frequência de avaliação da regra</span><span class="sxs-lookup"><span data-stu-id="afc69-137">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="afc69-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="afc69-138">-Name</span></span>
<span data-ttu-id="afc69-139">O nome da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="afc69-139">The name of metric alert rule</span></span>

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

### <span data-ttu-id="afc69-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc69-140">-ResourceGroupName</span></span>
<span data-ttu-id="afc69-141">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="afc69-141">The Resource Group Name</span></span>

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

### <span data-ttu-id="afc69-142">-Severidade</span><span class="sxs-lookup"><span data-stu-id="afc69-142">-Severity</span></span>
<span data-ttu-id="afc69-143">A gravidade da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="afc69-143">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="afc69-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="afc69-144">-TargetResourceId</span></span>
<span data-ttu-id="afc69-145">A ID do recurso de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="afc69-145">The target resource id for rule</span></span>

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

### <span data-ttu-id="afc69-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="afc69-146">-TargetResourceRegion</span></span>
<span data-ttu-id="afc69-147">A região de recursos de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="afc69-147">The target resource region for rule</span></span>

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

### <span data-ttu-id="afc69-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="afc69-148">-TargetResourceScope</span></span>
<span data-ttu-id="afc69-149">O escopo de recursos de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="afc69-149">The target resource scope for rule</span></span>

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

### <span data-ttu-id="afc69-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="afc69-150">-TargetResourceType</span></span>
<span data-ttu-id="afc69-151">O tipo de recurso de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="afc69-151">The target resource type for rule</span></span>

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

### <span data-ttu-id="afc69-152">-WindowS</span><span class="sxs-lookup"><span data-stu-id="afc69-152">-WindowSize</span></span>
<span data-ttu-id="afc69-153">O tamanho da janela para a regra</span><span class="sxs-lookup"><span data-stu-id="afc69-153">The window size for rule</span></span>

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

### <span data-ttu-id="afc69-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="afc69-154">-Confirm</span></span>
<span data-ttu-id="afc69-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afc69-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc69-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc69-156">-WhatIf</span></span>
<span data-ttu-id="afc69-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="afc69-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afc69-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afc69-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc69-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc69-159">CommonParameters</span></span>
<span data-ttu-id="afc69-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afc69-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc69-161">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afc69-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc69-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afc69-162">INPUTS</span></span>

### <span data-ttu-id="afc69-163">System. String</span><span class="sxs-lookup"><span data-stu-id="afc69-163">System.String</span></span>

### <span data-ttu-id="afc69-164">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="afc69-164">System.TimeSpan</span></span>

### <span data-ttu-id="afc69-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="afc69-165">System.String[]</span></span>

### <span data-ttu-id="afc69-166">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. insights. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="afc69-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="afc69-167">Microsoft. Azure. Management. monitor. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="afc69-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="afc69-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="afc69-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="afc69-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="afc69-169">System.Int32</span></span>

## <span data-ttu-id="afc69-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afc69-170">OUTPUTS</span></span>

### <span data-ttu-id="afc69-171">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="afc69-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="afc69-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afc69-172">NOTES</span></span>

## <span data-ttu-id="afc69-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afc69-173">RELATED LINKS</span></span>
