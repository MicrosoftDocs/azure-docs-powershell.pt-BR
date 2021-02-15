---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: d809a7d01e6b4d477a72d26df11d73e87678d7e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112960"
---
# <span data-ttu-id="0ac6d-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0ac6d-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="0ac6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ac6d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac6d-103">Obtém regras de alerta métrica V2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="0ac6d-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="0ac6d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ac6d-104">SYNTAX</span></span>

### <span data-ttu-id="0ac6d-105">ByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0ac6d-105">ByResourceGroupName (Default)</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ac6d-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="0ac6d-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ac6d-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="0ac6d-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ac6d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ac6d-108">DESCRIPTION</span></span>
<span data-ttu-id="0ac6d-109">O cmdlet **Get-AzMetricAlertRuleV2** obtém uma regra de alerta métrica por seu nome ou URI, ou todas as regras de alerta métrica de um grupo de recursos ou assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="0ac6d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ac6d-110">EXAMPLES</span></span>

### <span data-ttu-id="0ac6d-111">Exemplo 1: Obter todas as regras de alerta métrico na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="0ac6d-111">Example 1: Get all metric alert rules in current subscription</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : metricResourceGroup
Description          : fdafda
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/microsoft.insights/metricAlerts/Rule1
Name                 : Rule1
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : SampleResourceGroup
Description          : Testing 1 minute granuarity
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/Microsoft.Compute/virtualMachines/SCCMDemo4}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:01:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/Rule2
Name                 : Rule2
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="0ac6d-112">Esse comando obtém todas as regras de alerta métrica na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-112">This command gets all the metric alert rules in the current subscription.</span></span>

### <span data-ttu-id="0ac6d-113">Exemplo 2: Obter todas as regras de alerta métrico em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0ac6d-113">Example 2: Get all metric alert rules in a resource group</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/pr
                       oviders/microsoft.insights/actiongroups/emails}
ResourceGroup        : metricAlertsRG
Description          : Test Classic VM alert - CPU Usage
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Micr
                       osoft.ClassicCompute/virtualMachines/VM1}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.ClassicCompute/virtualMachines
TargetResourceRegion : southcentralus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/micro
                       soft.insights/metricAlerts/Test%20Classic%20VM%20alert%20-%20CPU%20Usage
Name                 : Test Classic VM alert - CPU Usage
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="0ac6d-114">Esse comando obtém todas as regras de alerta métrica no grupo de recursos chamado metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="0ac6d-115">Exemplo 3: Obter uma regra de alerta métrica por nome</span><span class="sxs-lookup"><span data-stu-id="0ac6d-115">Example 3: Get a metric alert rule by name</span></span>

```powershell
PS C:\> Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG -Name PS3182019

Criteria             : {metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
ResourceGroup        : metricAlertsRG
Description          : This is description 
Severity             : 1
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="0ac6d-116">Esse comando obtém a regra de alerta métrica chamada PS3182019 no grupo de recursos chamado metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="0ac6d-117">Exemplo 4: Obter uma regra de alerta métrica por IDda Regra</span><span class="sxs-lookup"><span data-stu-id="0ac6d-117">Example 4: Get a metric alert rule by ruleID</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/emails}
ResourceGroup        : SampleResourceGroup
Description          : Test Description
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : 
TargetResourceRegion : 
AutoMitigate         : 
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
Name                 : MyMetricAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="0ac6d-118">Esse comando obtém a regra de alerta métrico com a ID de recurso determinada.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="0ac6d-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ac6d-119">PARAMETERS</span></span>

### <span data-ttu-id="0ac6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac6d-120">-DefaultProfile</span></span>
<span data-ttu-id="0ac6d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ac6d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ac6d-122">-Name</span></span>
<span data-ttu-id="0ac6d-123">O Nome da regra de alerta métrico</span><span class="sxs-lookup"><span data-stu-id="0ac6d-123">The Name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ac6d-125">O ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac6d-125">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ac6d-126">-ResourceId</span></span>
<span data-ttu-id="0ac6d-127">A ID da Regra da regra de alerta métrico</span><span class="sxs-lookup"><span data-stu-id="0ac6d-127">The Rule Id of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac6d-128">CommonParameters</span></span>
<span data-ttu-id="0ac6d-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac6d-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ac6d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac6d-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ac6d-131">INPUTS</span></span>

### <span data-ttu-id="0ac6d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0ac6d-132">System.String</span></span>

## <span data-ttu-id="0ac6d-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ac6d-133">OUTPUTS</span></span>

### <span data-ttu-id="0ac6d-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0ac6d-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="0ac6d-135">Notas</span><span class="sxs-lookup"><span data-stu-id="0ac6d-135">NOTES</span></span>

## <span data-ttu-id="0ac6d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ac6d-136">RELATED LINKS</span></span>
