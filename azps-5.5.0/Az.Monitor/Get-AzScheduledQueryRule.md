---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 5cee29c5141a9fa5cce1af93f7c3ec1de487ffec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112957"
---
# <span data-ttu-id="97a35-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="97a35-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="97a35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97a35-102">SYNOPSIS</span></span>
<span data-ttu-id="97a35-103">Obtém recursos de consulta agendados</span><span class="sxs-lookup"><span data-stu-id="97a35-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="97a35-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97a35-104">SYNTAX</span></span>

### <span data-ttu-id="97a35-105">BySubscriptionOrResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="97a35-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97a35-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="97a35-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97a35-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97a35-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a35-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="97a35-108">DESCRIPTION</span></span>
<span data-ttu-id="97a35-109">Obtém recursos de consulta agendados</span><span class="sxs-lookup"><span data-stu-id="97a35-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="97a35-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97a35-110">EXAMPLES</span></span>

### <span data-ttu-id="97a35-111">Exemplo 1: Lista por assinatura ou grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="97a35-111">Example 1: List by subscription or resource group</span></span>
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

### <span data-ttu-id="97a35-112">Exemplo 2: Obter por nome de regra</span><span class="sxs-lookup"><span data-stu-id="97a35-112">Example 2: Get by rule name</span></span>
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

### <span data-ttu-id="97a35-113">Exemplo 3: Obter por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="97a35-113">Example 3: Get by resource Id</span></span>
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

## <span data-ttu-id="97a35-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97a35-114">PARAMETERS</span></span>

### <span data-ttu-id="97a35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a35-115">-DefaultProfile</span></span>
<span data-ttu-id="97a35-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97a35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a35-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="97a35-117">-Name</span></span>
<span data-ttu-id="97a35-118">O nome da regra de alerta</span><span class="sxs-lookup"><span data-stu-id="97a35-118">The alert rule name</span></span>

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

### <span data-ttu-id="97a35-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a35-119">-ResourceGroupName</span></span>
<span data-ttu-id="97a35-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="97a35-120">The resource group name</span></span>

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

### <span data-ttu-id="97a35-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a35-121">-ResourceId</span></span>
<span data-ttu-id="97a35-122">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="97a35-122">The resource Id</span></span>

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

### <span data-ttu-id="97a35-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a35-123">CommonParameters</span></span>
<span data-ttu-id="97a35-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a35-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a35-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97a35-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a35-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="97a35-126">INPUTS</span></span>

### <span data-ttu-id="97a35-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="97a35-127">None</span></span>

## <span data-ttu-id="97a35-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="97a35-128">OUTPUTS</span></span>

### <span data-ttu-id="97a35-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="97a35-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="97a35-130">Notas</span><span class="sxs-lookup"><span data-stu-id="97a35-130">NOTES</span></span>

## <span data-ttu-id="97a35-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97a35-131">RELATED LINKS</span></span>
