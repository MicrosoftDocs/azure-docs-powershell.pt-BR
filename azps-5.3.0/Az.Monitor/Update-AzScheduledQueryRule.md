---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428610"
---
# <span data-ttu-id="3f153-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3f153-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="3f153-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f153-102">SYNOPSIS</span></span>
<span data-ttu-id="3f153-103">Atualiza uma regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="3f153-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="3f153-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f153-104">SYNTAX</span></span>

### <span data-ttu-id="3f153-105">ByRuleName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f153-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f153-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3f153-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f153-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f153-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f153-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f153-108">DESCRIPTION</span></span>
<span data-ttu-id="3f153-109">Atualiza uma regra de alerta de log, atualizando somente a propriedade "Enabled" é compatível com este comando.</span><span class="sxs-lookup"><span data-stu-id="3f153-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="3f153-110">Para atualizar outras propriedades, consulte comando [set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) .</span><span class="sxs-lookup"><span data-stu-id="3f153-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="3f153-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f153-111">EXAMPLES</span></span>

### <span data-ttu-id="3f153-112">Exemplo 1: atualizar por nome de regra</span><span class="sxs-lookup"><span data-stu-id="3f153-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
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

### <span data-ttu-id="3f153-113">Exemplo 2: atualizar por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="3f153-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
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

### <span data-ttu-id="3f153-114">Exemplo 3: atualizar por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="3f153-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
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

## <span data-ttu-id="3f153-115">OS</span><span class="sxs-lookup"><span data-stu-id="3f153-115">PARAMETERS</span></span>

### <span data-ttu-id="3f153-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f153-116">-DefaultProfile</span></span>
<span data-ttu-id="3f153-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f153-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f153-118">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="3f153-118">-Enabled</span></span>
<span data-ttu-id="3f153-119">O estado do alerta do Azure-valores válidos-$true $false</span><span class="sxs-lookup"><span data-stu-id="3f153-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f153-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f153-120">-InputObject</span></span>
<span data-ttu-id="3f153-121">O recurso de regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="3f153-121">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f153-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f153-122">-Name</span></span>
<span data-ttu-id="3f153-123">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="3f153-123">The alert name</span></span>

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

### <span data-ttu-id="3f153-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f153-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f153-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3f153-125">The resource group name</span></span>

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

### <span data-ttu-id="3f153-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f153-126">-ResourceId</span></span>
<span data-ttu-id="3f153-127">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="3f153-127">The resource Id</span></span>

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

### <span data-ttu-id="3f153-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3f153-128">-Confirm</span></span>
<span data-ttu-id="3f153-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f153-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f153-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f153-130">-WhatIf</span></span>
<span data-ttu-id="3f153-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3f153-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f153-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f153-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f153-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f153-133">CommonParameters</span></span>
<span data-ttu-id="3f153-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f153-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f153-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f153-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f153-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f153-136">INPUTS</span></span>

### <span data-ttu-id="3f153-137">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="3f153-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="3f153-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3f153-138">System.String</span></span>

## <span data-ttu-id="3f153-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f153-139">OUTPUTS</span></span>

### <span data-ttu-id="3f153-140">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="3f153-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="3f153-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f153-141">NOTES</span></span>

## <span data-ttu-id="3f153-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f153-142">RELATED LINKS</span></span>
