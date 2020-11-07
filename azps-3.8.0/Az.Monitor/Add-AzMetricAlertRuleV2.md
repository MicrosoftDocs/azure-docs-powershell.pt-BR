---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 25854c3432f0ea28ee5eb267013992fce977b06a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93945019"
---
# <span data-ttu-id="bd032-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bd032-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="bd032-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd032-102">SYNOPSIS</span></span>
<span data-ttu-id="bd032-103">Adiciona ou atualiza uma regra de alerta baseada em métrica v2 (não clássico).</span><span class="sxs-lookup"><span data-stu-id="bd032-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="bd032-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd032-104">SYNTAX</span></span>

### <span data-ttu-id="bd032-105">CreateAlertByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="bd032-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd032-106">CreateAlertByResourceIdAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="bd032-106">CreateAlertByResourceIdAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd032-107">CreateAlertByResourceIdAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="bd032-107">CreateAlertByResourceIdAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd032-108">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="bd032-108">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd032-109">CreateAlertByScopesAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="bd032-109">CreateAlertByScopesAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd032-110">CreateAlertByScopesAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="bd032-110">CreateAlertByScopesAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd032-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd032-111">DESCRIPTION</span></span>
<span data-ttu-id="bd032-112">Adiciona ou atualiza uma **regra de alerta baseada em métrica v2 (não clássico)**.</span><span class="sxs-lookup"><span data-stu-id="bd032-112">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="bd032-113">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="bd032-113">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="bd032-114">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="bd032-114">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="bd032-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd032-115">EXAMPLES</span></span>

### <span data-ttu-id="bd032-116">Exemplo 1: adicionar uma regra de alerta de métrica a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="bd032-116">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="bd032-117">Esse comando cria uma regra de alerta métrica para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd032-117">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="bd032-118">$condition é a saída do cmdlet New-AzMetricAlertRuleV2Criteria e $act é a saída do cmdlet New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="bd032-118">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="bd032-119">Exemplo 2: adicionar uma regra de alerta de métrica para todas as máquinas virtuais em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="bd032-119">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="bd032-120">Este comando cria uma regra de alerta métrica para todas as máquinas virtuais na assinatura do lesteus</span><span class="sxs-lookup"><span data-stu-id="bd032-120">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="bd032-121">Exemplo 3: desabilitar uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="bd032-121">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="bd032-122">Esse comando desabilita uma regra de alerta de métrica.</span><span class="sxs-lookup"><span data-stu-id="bd032-122">This command disables a metric alert rule.</span></span> <span data-ttu-id="bd032-123">Aqui, estamos canalizando a saída de Get-AzMetricAlertRuleV2 para Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bd032-123">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="bd032-124">Exemplo 4: adicionar uma regra de alerta de métrica com dimensões</span><span class="sxs-lookup"><span data-stu-id="bd032-124">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="bd032-125">Para criar uma regra de alerta de métrica mais complexa, como aquelas que envolvem a seleção de valores de dimensão ou ter vários critérios, você pode usar os cmdlets auxiliares New-AzMetricAlertRuleV2DimensionSelection e New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="bd032-125">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="bd032-126">O conjunto de cmdlets acima criará uma regra de alerta métrica com dimensões.</span><span class="sxs-lookup"><span data-stu-id="bd032-126">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="bd032-127">OS</span><span class="sxs-lookup"><span data-stu-id="bd032-127">PARAMETERS</span></span>

### <span data-ttu-id="bd032-128">-Botão de ação</span><span class="sxs-lookup"><span data-stu-id="bd032-128">-ActionGroup</span></span>
<span data-ttu-id="bd032-129">O grupo ação para a regra</span><span class="sxs-lookup"><span data-stu-id="bd032-129">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: CreateAlertByResourceIdAndActionGroup, CreateAlertByScopesAndActionGroup
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd032-130">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="bd032-130">-ActionGroupId</span></span>
<span data-ttu-id="bd032-131">A ID do grupo de ação para a regra</span><span class="sxs-lookup"><span data-stu-id="bd032-131">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByResourceIdAndActionGroupId, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd032-132">-Condition</span><span class="sxs-lookup"><span data-stu-id="bd032-132">-Condition</span></span>
<span data-ttu-id="bd032-133">A condição para a regra</span><span class="sxs-lookup"><span data-stu-id="bd032-133">The condition for rule</span></span>

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

### <span data-ttu-id="bd032-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd032-134">-DefaultProfile</span></span>
<span data-ttu-id="bd032-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd032-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd032-136">-Descrição</span><span class="sxs-lookup"><span data-stu-id="bd032-136">-Description</span></span>
<span data-ttu-id="bd032-137">A descrição da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="bd032-137">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="bd032-138">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="bd032-138">-DisableRule</span></span>
<span data-ttu-id="bd032-139">O sinalizador desabilitar regra (status)</span><span class="sxs-lookup"><span data-stu-id="bd032-139">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="bd032-140">-Frequency</span><span class="sxs-lookup"><span data-stu-id="bd032-140">-Frequency</span></span>
<span data-ttu-id="bd032-141">A frequência de avaliação da regra</span><span class="sxs-lookup"><span data-stu-id="bd032-141">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="bd032-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd032-142">-Name</span></span>
<span data-ttu-id="bd032-143">O nome da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="bd032-143">The name of metric alert rule</span></span>

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

### <span data-ttu-id="bd032-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd032-144">-ResourceGroupName</span></span>
<span data-ttu-id="bd032-145">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bd032-145">The Resource Group Name</span></span>

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

### <span data-ttu-id="bd032-146">-Severidade</span><span class="sxs-lookup"><span data-stu-id="bd032-146">-Severity</span></span>
<span data-ttu-id="bd032-147">A gravidade da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="bd032-147">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="bd032-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bd032-148">-TargetResourceId</span></span>
<span data-ttu-id="bd032-149">A ID do recurso de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="bd032-149">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId, CreateAlertByResourceIdAndActionGroup, CreateAlertByResourceIdAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd032-150">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="bd032-150">-TargetResourceRegion</span></span>
<span data-ttu-id="bd032-151">A região de recursos de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="bd032-151">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd032-152">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="bd032-152">-TargetResourceScope</span></span>
<span data-ttu-id="bd032-153">O escopo de recursos de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="bd032-153">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd032-154">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="bd032-154">-TargetResourceType</span></span>
<span data-ttu-id="bd032-155">O tipo de recurso de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="bd032-155">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd032-156">-WindowS</span><span class="sxs-lookup"><span data-stu-id="bd032-156">-WindowSize</span></span>
<span data-ttu-id="bd032-157">O tamanho da janela para a regra</span><span class="sxs-lookup"><span data-stu-id="bd032-157">The window size for rule</span></span>

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

### <span data-ttu-id="bd032-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd032-158">-Confirm</span></span>
<span data-ttu-id="bd032-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd032-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd032-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd032-160">-WhatIf</span></span>
<span data-ttu-id="bd032-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd032-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd032-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd032-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd032-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd032-163">CommonParameters</span></span>
<span data-ttu-id="bd032-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd032-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd032-165">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd032-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd032-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd032-166">INPUTS</span></span>

### <span data-ttu-id="bd032-167">System. String</span><span class="sxs-lookup"><span data-stu-id="bd032-167">System.String</span></span>

### <span data-ttu-id="bd032-168">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="bd032-168">System.TimeSpan</span></span>

### <span data-ttu-id="bd032-169">System. String []</span><span class="sxs-lookup"><span data-stu-id="bd032-169">System.String[]</span></span>

### <span data-ttu-id="bd032-170">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. insights. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bd032-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bd032-171">Microsoft. Azure. Management. monitor. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="bd032-171">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="bd032-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd032-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bd032-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bd032-173">System.Int32</span></span>

## <span data-ttu-id="bd032-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd032-174">OUTPUTS</span></span>

### <span data-ttu-id="bd032-175">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bd032-175">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="bd032-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd032-176">NOTES</span></span>

## <span data-ttu-id="bd032-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd032-177">RELATED LINKS</span></span>
