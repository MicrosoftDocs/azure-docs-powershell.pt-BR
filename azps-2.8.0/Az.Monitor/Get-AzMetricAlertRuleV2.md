---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: 5f59de112c99c679b8b9f7187cf4973111f6e931
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771884"
---
# <span data-ttu-id="52a42-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="52a42-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="52a42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52a42-102">SYNOPSIS</span></span>
<span data-ttu-id="52a42-103">Obtém regras de alerta de métrica v2 (não clássicas)</span><span class="sxs-lookup"><span data-stu-id="52a42-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="52a42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52a42-104">SYNTAX</span></span>

### <span data-ttu-id="52a42-105">ByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="52a42-105">ByResourceGroupName (Default)</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52a42-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="52a42-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52a42-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="52a42-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a42-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52a42-108">DESCRIPTION</span></span>
<span data-ttu-id="52a42-109">O cmdlet **Get-AzMetricAlertRuleV2** Obtém uma regra de alerta de métrica por seu nome ou URI, ou todas as regras de alerta de métrica de um grupo de recursos ou assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="52a42-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="52a42-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52a42-110">EXAMPLES</span></span>

### <span data-ttu-id="52a42-111">Exemplo 1: obter todas as regras de alerta de métrica na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="52a42-111">Example 1: Get all metric alert rules in current subscription</span></span>
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

<span data-ttu-id="52a42-112">Este comando obtém todas as regras de alerta de métrica na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="52a42-112">This command gets all the metric alert rules in the current subscription.</span></span>

### <span data-ttu-id="52a42-113">Exemplo 2: obter todas as regras de alerta de métrica em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="52a42-113">Example 2: Get all metric alert rules in a resource group</span></span>

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

<span data-ttu-id="52a42-114">Esse comando obtém todas as regras de alerta de métrica no grupo de recursos chamado metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="52a42-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="52a42-115">Exemplo 3: obter uma regra de alerta de métrica por nome</span><span class="sxs-lookup"><span data-stu-id="52a42-115">Example 3: Get a metric alert rule by name</span></span>

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

<span data-ttu-id="52a42-116">Esse comando obtém a regra de alerta de métrica chamada PS3182019 no grupo de recursos chamado metricAlertsRG.</span><span class="sxs-lookup"><span data-stu-id="52a42-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="52a42-117">Exemplo 4: obter uma regra de alerta de métrica por RuleId</span><span class="sxs-lookup"><span data-stu-id="52a42-117">Example 4: Get a metric alert rule by ruleID</span></span>

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

<span data-ttu-id="52a42-118">Este comando obtém a regra de alerta de métrica com a ID do recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="52a42-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="52a42-119">OS</span><span class="sxs-lookup"><span data-stu-id="52a42-119">PARAMETERS</span></span>

### <span data-ttu-id="52a42-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a42-120">-DefaultProfile</span></span>
<span data-ttu-id="52a42-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52a42-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a42-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="52a42-122">-Name</span></span>
<span data-ttu-id="52a42-123">O nome da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="52a42-123">The Name of metric alert rule</span></span>

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

### <span data-ttu-id="52a42-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a42-124">-ResourceGroupName</span></span>
<span data-ttu-id="52a42-125">O ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a42-125">The ResourceGroupName</span></span>

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

### <span data-ttu-id="52a42-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52a42-126">-ResourceId</span></span>
<span data-ttu-id="52a42-127">A ID da regra da regra de alerta métrico</span><span class="sxs-lookup"><span data-stu-id="52a42-127">The Rule Id of metric alert rule</span></span>

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

### <span data-ttu-id="52a42-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a42-128">CommonParameters</span></span>
<span data-ttu-id="52a42-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a42-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a42-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52a42-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a42-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52a42-131">INPUTS</span></span>

### <span data-ttu-id="52a42-132">System. String</span><span class="sxs-lookup"><span data-stu-id="52a42-132">System.String</span></span>

## <span data-ttu-id="52a42-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52a42-133">OUTPUTS</span></span>

### <span data-ttu-id="52a42-134">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="52a42-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="52a42-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52a42-135">NOTES</span></span>

## <span data-ttu-id="52a42-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52a42-136">RELATED LINKS</span></span>
