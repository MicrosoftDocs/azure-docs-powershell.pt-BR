---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114757"
---
# <span data-ttu-id="81538-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="81538-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="81538-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81538-102">SYNOPSIS</span></span>
<span data-ttu-id="81538-103">Atualiza uma regra de Alerta de Log</span><span class="sxs-lookup"><span data-stu-id="81538-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="81538-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81538-104">SYNTAX</span></span>

### <span data-ttu-id="81538-105">ByRuleName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="81538-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81538-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="81538-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81538-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81538-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81538-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="81538-108">DESCRIPTION</span></span>
<span data-ttu-id="81538-109">Atualiza uma regra de Alerta de Log, atualizando apenas a propriedade "Habilitado" é suportado por esse comando.</span><span class="sxs-lookup"><span data-stu-id="81538-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="81538-110">Para atualizar outras propriedades, consulte [o comando Set-AzScheduledQueryRule.](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule)</span><span class="sxs-lookup"><span data-stu-id="81538-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="81538-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="81538-111">EXAMPLES</span></span>

### <span data-ttu-id="81538-112">Exemplo 1: Atualizar por nome da regra</span><span class="sxs-lookup"><span data-stu-id="81538-112">Example 1: Update by rule name</span></span>
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

### <span data-ttu-id="81538-113">Exemplo 2: Atualizar por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="81538-113">Example 2: Update by input object</span></span>
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

### <span data-ttu-id="81538-114">Exemplo 3: Atualizar por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="81538-114">Example 3: Update by resource Id</span></span>
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

## <span data-ttu-id="81538-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81538-115">PARAMETERS</span></span>

### <span data-ttu-id="81538-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81538-116">-DefaultProfile</span></span>
<span data-ttu-id="81538-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81538-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81538-118">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="81538-118">-Enabled</span></span>
<span data-ttu-id="81538-119">O estado de alerta do Azure - valores válidos - $true, $false</span><span class="sxs-lookup"><span data-stu-id="81538-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="81538-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81538-120">-InputObject</span></span>
<span data-ttu-id="81538-121">O recurso Regra de Consulta Agendada</span><span class="sxs-lookup"><span data-stu-id="81538-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="81538-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="81538-122">-Name</span></span>
<span data-ttu-id="81538-123">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="81538-123">The alert name</span></span>

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

### <span data-ttu-id="81538-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81538-124">-ResourceGroupName</span></span>
<span data-ttu-id="81538-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="81538-125">The resource group name</span></span>

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

### <span data-ttu-id="81538-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81538-126">-ResourceId</span></span>
<span data-ttu-id="81538-127">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="81538-127">The resource Id</span></span>

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

### <span data-ttu-id="81538-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="81538-128">-Confirm</span></span>
<span data-ttu-id="81538-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81538-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81538-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81538-130">-WhatIf</span></span>
<span data-ttu-id="81538-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="81538-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81538-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81538-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81538-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81538-133">CommonParameters</span></span>
<span data-ttu-id="81538-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81538-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81538-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81538-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81538-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="81538-136">INPUTS</span></span>

### <span data-ttu-id="81538-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="81538-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="81538-138">System.String</span><span class="sxs-lookup"><span data-stu-id="81538-138">System.String</span></span>

## <span data-ttu-id="81538-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="81538-139">OUTPUTS</span></span>

### <span data-ttu-id="81538-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="81538-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="81538-141">Notas</span><span class="sxs-lookup"><span data-stu-id="81538-141">NOTES</span></span>

## <span data-ttu-id="81538-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81538-142">RELATED LINKS</span></span>
