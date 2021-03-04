---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: d01399eeedf3b27bbf74e969876e24180ed571b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886930"
---
# <span data-ttu-id="af526-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="af526-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="af526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af526-102">SYNOPSIS</span></span>
<span data-ttu-id="af526-103">Cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="af526-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="af526-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="af526-104">SYNTAX</span></span>

### <span data-ttu-id="af526-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="af526-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af526-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af526-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af526-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="af526-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af526-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="af526-108">DESCRIPTION</span></span>
<span data-ttu-id="af526-109">O cmdlet **Set-AzActivityLogAlert** cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="af526-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="af526-110">Para marcas, condições e ações, os objetos devem ser criados antecipadamente e passados como parâmetros nesta chamada como uma vírgula separada (consulte o exemplo abaixo).</span><span class="sxs-lookup"><span data-stu-id="af526-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="af526-111">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar/modificar o recurso.</span><span class="sxs-lookup"><span data-stu-id="af526-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="af526-112">**OBSERVAÇÃO**: Este cmdlet e seus relacionados substitui o preterido (novembro de 2017) **Add-AzLogAlertRule**.</span><span class="sxs-lookup"><span data-stu-id="af526-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="af526-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af526-113">EXAMPLES</span></span>

### <span data-ttu-id="af526-114">Exemplo 1: Criar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="af526-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="af526-115">Os quatro primeiros comandos criam a condição de folha e o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="af526-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="af526-116">O comando final cria um Alerta de Log de Atividade usando a condição e o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="af526-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="af526-117">Exemplo 2: Criar um Alerta de Log de Atividades desabilitado</span><span class="sxs-lookup"><span data-stu-id="af526-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="af526-118">Os quatro primeiros comandos criam a condição de folha e o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="af526-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="af526-119">O comando final cria um Alerta de Log de Atividade usando a condição e o grupo de ações, mas cria o alerta desabilitado.</span><span class="sxs-lookup"><span data-stu-id="af526-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="af526-120">Exemplo 3: definir um alerta de log de atividade com base em um valor do pipe ou do parâmetro InputObject</span><span class="sxs-lookup"><span data-stu-id="af526-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="af526-121">O primeiro comando é semelhante a um nop, ele define o alerta com os mesmos valores que ele já continha O restante dos comandos recupera a regra de alerta, altera a descrição e a desabilita e, em seguida, usa o parâmetro InputObject para persistir essas alterações</span><span class="sxs-lookup"><span data-stu-id="af526-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="af526-122">Exemplo 4: definir um alerta de log de atividades com base no valor ResourceId do pipe</span><span class="sxs-lookup"><span data-stu-id="af526-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="af526-123">Se a regra de alerta de log determinada existir, esse comando a desabilitará.</span><span class="sxs-lookup"><span data-stu-id="af526-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="af526-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="af526-124">PARAMETERS</span></span>

### <span data-ttu-id="af526-125">-Action</span><span class="sxs-lookup"><span data-stu-id="af526-125">-Action</span></span>
<span data-ttu-id="af526-126">A lista de grupos de ações do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="af526-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-127">-Condition</span><span class="sxs-lookup"><span data-stu-id="af526-127">-Condition</span></span>
<span data-ttu-id="af526-128">A lista de condições do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="af526-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="af526-129">**OBSERVAÇÃO**: Na lista de condições, deve haver pelo menos uma com Field igual a "Category".</span><span class="sxs-lookup"><span data-stu-id="af526-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="af526-130">O back-end responde com 400 (BadRequest) se essa condição não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="af526-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af526-131">-DefaultProfile</span></span>
<span data-ttu-id="af526-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="af526-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af526-133">-Description</span><span class="sxs-lookup"><span data-stu-id="af526-133">-Description</span></span>
<span data-ttu-id="af526-134">A descrição do recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="af526-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="af526-135">-DisableAlert</span></span>
<span data-ttu-id="af526-136">Permite que o usuário crie um alerta de log de atividades desabilitado.</span><span class="sxs-lookup"><span data-stu-id="af526-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="af526-137">Se não for dado, os alertas serão criados habilitados.</span><span class="sxs-lookup"><span data-stu-id="af526-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af526-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af526-138">-InputObject</span></span>
<span data-ttu-id="af526-139">Define a propriedade InputObject tags da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af526-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-140">-Location</span><span class="sxs-lookup"><span data-stu-id="af526-140">-Location</span></span>
<span data-ttu-id="af526-141">O local onde o alerta de log de atividade existirá.</span><span class="sxs-lookup"><span data-stu-id="af526-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-142">-Name</span><span class="sxs-lookup"><span data-stu-id="af526-142">-Name</span></span>
<span data-ttu-id="af526-143">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="af526-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af526-144">-ResourceGroupName</span></span>
<span data-ttu-id="af526-145">O nome do grupo de recursos onde o recurso de alerta existirá.</span><span class="sxs-lookup"><span data-stu-id="af526-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af526-146">-ResourceId</span></span>
<span data-ttu-id="af526-147">Define a propriedade de marcas ResourceId da chamada para extrair o nome necessário, propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af526-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="af526-148">-Scope</span></span>
<span data-ttu-id="af526-149">A lista de escopos do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="af526-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="af526-150">-Tag</span></span>
<span data-ttu-id="af526-151">Define a propriedade tags do recurso de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="af526-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af526-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af526-152">-Confirm</span></span>
<span data-ttu-id="af526-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af526-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af526-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af526-154">-WhatIf</span></span>
<span data-ttu-id="af526-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af526-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af526-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af526-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af526-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af526-157">CommonParameters</span></span>
<span data-ttu-id="af526-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af526-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af526-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af526-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af526-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af526-160">INPUTS</span></span>

### <span data-ttu-id="af526-161">System.String</span><span class="sxs-lookup"><span data-stu-id="af526-161">System.String</span></span>

### <span data-ttu-id="af526-162">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af526-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af526-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="af526-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="af526-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="af526-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="af526-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af526-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af526-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="af526-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="af526-167">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="af526-167">OUTPUTS</span></span>

### <span data-ttu-id="af526-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="af526-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="af526-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="af526-169">NOTES</span></span>

## <span data-ttu-id="af526-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af526-170">RELATED LINKS</span></span>

[<span data-ttu-id="af526-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="af526-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="af526-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="af526-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="af526-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="af526-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="af526-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="af526-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="af526-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="af526-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="af526-176">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="af526-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
