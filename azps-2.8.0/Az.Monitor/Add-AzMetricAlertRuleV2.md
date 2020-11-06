---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: ffa4ffef702d637291d092792309f20bb082888a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595875"
---
# <span data-ttu-id="33a3e-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="33a3e-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="33a3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="33a3e-103">Adiciona ou atualiza uma regra de alerta baseada em métrica v2 (não clássico).</span><span class="sxs-lookup"><span data-stu-id="33a3e-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="33a3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33a3e-104">SYNTAX</span></span>

### <span data-ttu-id="33a3e-105">CreateAlertByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="33a3e-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a3e-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="33a3e-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33a3e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33a3e-107">DESCRIPTION</span></span>
<span data-ttu-id="33a3e-108">Adiciona ou atualiza uma **regra de alerta baseada em métrica v2 (não clássico)**.</span><span class="sxs-lookup"><span data-stu-id="33a3e-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="33a3e-109">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="33a3e-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="33a3e-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="33a3e-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="33a3e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33a3e-111">EXAMPLES</span></span>

### <span data-ttu-id="33a3e-112">Exemplo 1: adicionar uma regra de alerta de métrica a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="33a3e-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="33a3e-113">Esse comando cria uma regra de alerta métrica para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="33a3e-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="33a3e-114">$condition é a saída do cmdlet New-AzMetricAlertRuleV2Criteria e $act é a saída do cmdlet New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="33a3e-114">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="33a3e-115">Exemplo 2: adicionar uma regra de alerta de métrica para todas as máquinas virtuais em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="33a3e-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="33a3e-116">Este comando cria uma regra de alerta métrica para todas as máquinas virtuais na assinatura do lesteus</span><span class="sxs-lookup"><span data-stu-id="33a3e-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="33a3e-117">Exemplo 3: desabilitar uma regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="33a3e-117">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="33a3e-118">Esse comando desabilita uma regra de alerta de métrica.</span><span class="sxs-lookup"><span data-stu-id="33a3e-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="33a3e-119">Aqui, estamos canalizando a saída de Get-AzMetricAlertRuleV2 para Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="33a3e-119">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="33a3e-120">Exemplo 4: adicionar uma regra de alerta de métrica com dimensões</span><span class="sxs-lookup"><span data-stu-id="33a3e-120">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="33a3e-121">Para criar uma regra de alerta de métrica mais complexa, como aquelas que envolvem a seleção de valores de dimensão ou ter vários critérios, você pode usar os cmdlets auxiliares New-AzMetricAlertRuleV2DimensionSelection e New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="33a3e-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="33a3e-122">O conjunto de cmdlets acima criará uma regra de alerta métrica com dimensões.</span><span class="sxs-lookup"><span data-stu-id="33a3e-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="33a3e-123">OS</span><span class="sxs-lookup"><span data-stu-id="33a3e-123">PARAMETERS</span></span>

### <span data-ttu-id="33a3e-124">-Botão de ação</span><span class="sxs-lookup"><span data-stu-id="33a3e-124">-ActionGroup</span></span>
<span data-ttu-id="33a3e-125">O grupo ação para a regra</span><span class="sxs-lookup"><span data-stu-id="33a3e-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33a3e-126">-Condition</span><span class="sxs-lookup"><span data-stu-id="33a3e-126">-Condition</span></span>
<span data-ttu-id="33a3e-127">A condição para a regra</span><span class="sxs-lookup"><span data-stu-id="33a3e-127">The condition for rule</span></span>

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

### <span data-ttu-id="33a3e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a3e-128">-DefaultProfile</span></span>
<span data-ttu-id="33a3e-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33a3e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a3e-130">-Descrição</span><span class="sxs-lookup"><span data-stu-id="33a3e-130">-Description</span></span>
<span data-ttu-id="33a3e-131">A descrição da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="33a3e-131">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="33a3e-132">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="33a3e-132">-DisableRule</span></span>
<span data-ttu-id="33a3e-133">O sinalizador desabilitar regra (status)</span><span class="sxs-lookup"><span data-stu-id="33a3e-133">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="33a3e-134">-Frequency</span><span class="sxs-lookup"><span data-stu-id="33a3e-134">-Frequency</span></span>
<span data-ttu-id="33a3e-135">A frequência de avaliação da regra</span><span class="sxs-lookup"><span data-stu-id="33a3e-135">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="33a3e-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="33a3e-136">-Name</span></span>
<span data-ttu-id="33a3e-137">O nome da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="33a3e-137">The name of metric alert rule</span></span>

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

### <span data-ttu-id="33a3e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a3e-138">-ResourceGroupName</span></span>
<span data-ttu-id="33a3e-139">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="33a3e-139">The Resource Group Name</span></span>

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

### <span data-ttu-id="33a3e-140">-Severidade</span><span class="sxs-lookup"><span data-stu-id="33a3e-140">-Severity</span></span>
<span data-ttu-id="33a3e-141">A gravidade da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="33a3e-141">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="33a3e-142">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="33a3e-142">-TargetResourceId</span></span>
<span data-ttu-id="33a3e-143">A ID do recurso de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="33a3e-143">The target resource id for rule</span></span>

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

### <span data-ttu-id="33a3e-144">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="33a3e-144">-TargetResourceRegion</span></span>
<span data-ttu-id="33a3e-145">A região de recursos de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="33a3e-145">The target resource region for rule</span></span>

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

### <span data-ttu-id="33a3e-146">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="33a3e-146">-TargetResourceScope</span></span>
<span data-ttu-id="33a3e-147">O escopo de recursos de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="33a3e-147">The target resource scope for rule</span></span>

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

### <span data-ttu-id="33a3e-148">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="33a3e-148">-TargetResourceType</span></span>
<span data-ttu-id="33a3e-149">O tipo de recurso de destino para a regra</span><span class="sxs-lookup"><span data-stu-id="33a3e-149">The target resource type for rule</span></span>

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

### <span data-ttu-id="33a3e-150">-WindowS</span><span class="sxs-lookup"><span data-stu-id="33a3e-150">-WindowSize</span></span>
<span data-ttu-id="33a3e-151">O tamanho da janela para a regra</span><span class="sxs-lookup"><span data-stu-id="33a3e-151">The window size for rule</span></span>

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

### <span data-ttu-id="33a3e-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33a3e-152">-Confirm</span></span>
<span data-ttu-id="33a3e-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a3e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a3e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a3e-154">-WhatIf</span></span>
<span data-ttu-id="33a3e-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33a3e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33a3e-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33a3e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a3e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a3e-157">CommonParameters</span></span>
<span data-ttu-id="33a3e-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a3e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a3e-159">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33a3e-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a3e-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33a3e-160">INPUTS</span></span>

### <span data-ttu-id="33a3e-161">System. String</span><span class="sxs-lookup"><span data-stu-id="33a3e-161">System.String</span></span>

### <span data-ttu-id="33a3e-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="33a3e-162">System.TimeSpan</span></span>

### <span data-ttu-id="33a3e-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="33a3e-163">System.String[]</span></span>

### <span data-ttu-id="33a3e-164">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. insights. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="33a3e-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="33a3e-165">Microsoft. Azure. Management. monitor. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="33a3e-165">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="33a3e-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="33a3e-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="33a3e-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="33a3e-167">System.Int32</span></span>

## <span data-ttu-id="33a3e-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33a3e-168">OUTPUTS</span></span>

### <span data-ttu-id="33a3e-169">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="33a3e-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="33a3e-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33a3e-170">NOTES</span></span>

## <span data-ttu-id="33a3e-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33a3e-171">RELATED LINKS</span></span>
