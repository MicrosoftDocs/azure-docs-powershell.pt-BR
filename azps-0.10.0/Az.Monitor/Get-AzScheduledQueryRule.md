---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 1cb05a83ccbe1786392867f4714553413fe635c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775730"
---
# <span data-ttu-id="0119a-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0119a-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="0119a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0119a-102">SYNOPSIS</span></span>
<span data-ttu-id="0119a-103">Obtém recursos de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="0119a-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="0119a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0119a-104">SYNTAX</span></span>

### <span data-ttu-id="0119a-105">BySubscriptionOrResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="0119a-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0119a-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="0119a-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0119a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0119a-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0119a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0119a-108">DESCRIPTION</span></span>
<span data-ttu-id="0119a-109">Obtém recursos de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="0119a-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="0119a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0119a-110">EXAMPLES</span></span>

### <span data-ttu-id="0119a-111">Exemplo 1-listar por assinatura ou grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0119a-111">Example 1 - List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="0119a-112">Exemplo 2-obter por nome da regra</span><span class="sxs-lookup"><span data-stu-id="0119a-112">Example 2 - Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="0119a-113">Exemplo 3-obter por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="0119a-113">Example 3 - Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="0119a-114">OS</span><span class="sxs-lookup"><span data-stu-id="0119a-114">PARAMETERS</span></span>

### <span data-ttu-id="0119a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0119a-115">-DefaultProfile</span></span>
<span data-ttu-id="0119a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0119a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0119a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0119a-117">-Name</span></span>
<span data-ttu-id="0119a-118">O nome da regra de alerta</span><span class="sxs-lookup"><span data-stu-id="0119a-118">The alert rule name</span></span>

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

### <span data-ttu-id="0119a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0119a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0119a-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0119a-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="0119a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0119a-121">-ResourceId</span></span>
<span data-ttu-id="0119a-122">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="0119a-122">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0119a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0119a-123">CommonParameters</span></span>
<span data-ttu-id="0119a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0119a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0119a-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0119a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0119a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0119a-126">INPUTS</span></span>

### <span data-ttu-id="0119a-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0119a-127">None</span></span>

## <span data-ttu-id="0119a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0119a-128">OUTPUTS</span></span>

### <span data-ttu-id="0119a-129">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="0119a-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="0119a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0119a-130">NOTES</span></span>

## <span data-ttu-id="0119a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0119a-131">RELATED LINKS</span></span>
