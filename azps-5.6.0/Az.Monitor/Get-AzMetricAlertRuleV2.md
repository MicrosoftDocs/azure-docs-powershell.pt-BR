---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: 135451f5e44d8e92511b84766d5be66be3cd7e9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888879"
---
# <span data-ttu-id="e7d84-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e7d84-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="e7d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d84-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d84-103">Obtém regras de alerta métricaS V2 (não clássicas)</span><span class="sxs-lookup"><span data-stu-id="e7d84-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="e7d84-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7d84-104">SYNTAX</span></span>

### <span data-ttu-id="e7d84-105">ByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e7d84-105">ByResourceGroupName (Default)</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7d84-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="e7d84-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7d84-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="e7d84-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7d84-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7d84-108">DESCRIPTION</span></span>
<span data-ttu-id="e7d84-109">O cmdlet **Get-AzMetricAlertRuleV2** obtém uma regra de alerta métrica por seu nome ou URI, ou todas as regras de alerta métricas de um grupo de recursos ou assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="e7d84-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="e7d84-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7d84-110">EXAMPLES</span></span>

### <span data-ttu-id="e7d84-111">Exemplo 1: Obter todas as regras de alerta métricas na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="e7d84-111">Example 1: Get all metric alert rules in current subscription</span></span>
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

<span data-ttu-id="e7d84-112">Esse comando obtém todas as regras de alerta métricas na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e7d84-112">This command gets all the metric alert rules in the current subscription.</span></span>

### <span data-ttu-id="e7d84-113">Exemplo 2: Obter todas as regras de alerta métricas em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e7d84-113">Example 2: Get all metric alert rules in a resource group</span></span>

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

<span data-ttu-id="e7d84-114">Este comando obtém todas as regras de alerta métricas no grupo de recursos chamado metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="e7d84-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="e7d84-115">Exemplo 3: Obter uma regra de alerta métrica pelo nome</span><span class="sxs-lookup"><span data-stu-id="e7d84-115">Example 3: Get a metric alert rule by name</span></span>

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

<span data-ttu-id="e7d84-116">Este comando obtém a regra de alerta métrica chamada PS3182019 no grupo de recursos chamado metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="e7d84-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="e7d84-117">Exemplo 4: Obter uma regra de alerta métrica por ruleID</span><span class="sxs-lookup"><span data-stu-id="e7d84-117">Example 4: Get a metric alert rule by ruleID</span></span>

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

<span data-ttu-id="e7d84-118">Esse comando obtém a regra de alerta métrica com a ID de recurso determinada.</span><span class="sxs-lookup"><span data-stu-id="e7d84-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="e7d84-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7d84-119">PARAMETERS</span></span>

### <span data-ttu-id="e7d84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d84-120">-DefaultProfile</span></span>
<span data-ttu-id="e7d84-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d84-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7d84-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e7d84-122">-Name</span></span>
<span data-ttu-id="e7d84-123">A regra nome da regra de alerta métrica</span><span class="sxs-lookup"><span data-stu-id="e7d84-123">The Name of metric alert rule</span></span>

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

### <span data-ttu-id="e7d84-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d84-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7d84-125">The ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d84-125">The ResourceGroupName</span></span>

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

### <span data-ttu-id="e7d84-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7d84-126">-ResourceId</span></span>
<span data-ttu-id="e7d84-127">A ID da regra de alerta métrica</span><span class="sxs-lookup"><span data-stu-id="e7d84-127">The Rule Id of metric alert rule</span></span>

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

### <span data-ttu-id="e7d84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d84-128">CommonParameters</span></span>
<span data-ttu-id="e7d84-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d84-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7d84-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d84-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7d84-131">INPUTS</span></span>

### <span data-ttu-id="e7d84-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e7d84-132">System.String</span></span>

## <span data-ttu-id="e7d84-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7d84-133">OUTPUTS</span></span>

### <span data-ttu-id="e7d84-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e7d84-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="e7d84-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7d84-135">NOTES</span></span>

## <span data-ttu-id="e7d84-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7d84-136">RELATED LINKS</span></span>
