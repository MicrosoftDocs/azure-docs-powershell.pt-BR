---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 6c7b867add359edec8379f20e630c9aca5fed00e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402874"
---
# <span data-ttu-id="8b848-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8b848-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="8b848-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b848-102">SYNOPSIS</span></span>
<span data-ttu-id="8b848-103">Cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="8b848-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="8b848-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b848-104">SYNTAX</span></span>

### <span data-ttu-id="8b848-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b848-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b848-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b848-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b848-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b848-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b848-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b848-108">DESCRIPTION</span></span>
<span data-ttu-id="8b848-109">O cmdlet **Set-AzActivityLogAlert** cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="8b848-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="8b848-110">Para marcas, condições e ações, os objetos devem ser criados com antecedência e passados como parâmetros nesta chamada como uma vírgula separada (veja o exemplo abaixo).</span><span class="sxs-lookup"><span data-stu-id="8b848-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="8b848-111">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar/modificar o recurso.</span><span class="sxs-lookup"><span data-stu-id="8b848-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="8b848-112">**OBSERVAÇÃO:** este cmdlet e seus relacionados substituem o **add-AzLogAlertRule** preterido (novembro de 2017).</span><span class="sxs-lookup"><span data-stu-id="8b848-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="8b848-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b848-113">EXAMPLES</span></span>

### <span data-ttu-id="8b848-114">Exemplo 1: Criar um Alerta de Log de Atividades</span><span class="sxs-lookup"><span data-stu-id="8b848-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="8b848-115">Os quatro primeiros comandos criam a condição de folha e o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="8b848-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="8b848-116">O comando final cria um Alerta de Log de Atividades usando a condição e o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="8b848-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="8b848-117">Exemplo 2: Criar um Alerta de Log de Atividades desabilitado</span><span class="sxs-lookup"><span data-stu-id="8b848-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="8b848-118">Os quatro primeiros comandos criam a condição de folha e o grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="8b848-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="8b848-119">O comando final cria um Alerta de Log de Atividades usando a condição e o grupo de ações, mas ele cria o alerta desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8b848-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="8b848-120">Exemplo 3: Definir um alerta de log de atividades com base em um valor do cano ou do parâmetro InputObject</span><span class="sxs-lookup"><span data-stu-id="8b848-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="8b848-121">O primeiro comando é semelhante a um nop, ele define o alerta com os mesmos valores que ele já continha O restante dos comandos recupera a regra de alerta, altera a descrição e a desabilita e, em seguida, usa o parâmetro InputObject para persistir essas alterações</span><span class="sxs-lookup"><span data-stu-id="8b848-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="8b848-122">Exemplo 4: Definir um alerta de log de atividades com base no valor ResourceId do cano</span><span class="sxs-lookup"><span data-stu-id="8b848-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="8b848-123">Se houver uma determinada regra de alerta de log, esse comando a desabilitará.</span><span class="sxs-lookup"><span data-stu-id="8b848-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="8b848-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b848-124">PARAMETERS</span></span>

### <span data-ttu-id="8b848-125">-Ação</span><span class="sxs-lookup"><span data-stu-id="8b848-125">-Action</span></span>
<span data-ttu-id="8b848-126">A lista de grupos de ações para o alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="8b848-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="8b848-127">-Condição</span><span class="sxs-lookup"><span data-stu-id="8b848-127">-Condition</span></span>
<span data-ttu-id="8b848-128">A lista de condições para o alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="8b848-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="8b848-129">**OBSERVAÇÃO:** na lista de condições, deve haver pelo menos uma com o Campo igual a "Categoria".</span><span class="sxs-lookup"><span data-stu-id="8b848-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="8b848-130">O back-end responderá com 400 (BadRequest) se essa condição não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="8b848-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="8b848-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b848-131">-DefaultProfile</span></span>
<span data-ttu-id="8b848-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8b848-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b848-133">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8b848-133">-Description</span></span>
<span data-ttu-id="8b848-134">A descrição do recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="8b848-134">The description of the alert resource.</span></span>

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

### <span data-ttu-id="8b848-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="8b848-135">-DisableAlert</span></span>
<span data-ttu-id="8b848-136">Permite que o usuário crie um alerta de log de atividades desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8b848-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="8b848-137">Se não for dado, os alertas serão criados habilitados.</span><span class="sxs-lookup"><span data-stu-id="8b848-137">If not given, the alerts are created enabled.</span></span>

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

### <span data-ttu-id="8b848-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b848-138">-InputObject</span></span>
<span data-ttu-id="8b848-139">Define a propriedade de marcas InputObject da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b848-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="8b848-140">-Local</span><span class="sxs-lookup"><span data-stu-id="8b848-140">-Location</span></span>
<span data-ttu-id="8b848-141">O local onde o alerta do log de atividades existirá.</span><span class="sxs-lookup"><span data-stu-id="8b848-141">The location where the activity log alert will exist.</span></span>

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

### <span data-ttu-id="8b848-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b848-142">-Name</span></span>
<span data-ttu-id="8b848-143">O nome do alerta do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="8b848-143">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="8b848-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b848-144">-ResourceGroupName</span></span>
<span data-ttu-id="8b848-145">O nome do grupo de recursos onde o recurso de alerta existirá.</span><span class="sxs-lookup"><span data-stu-id="8b848-145">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="8b848-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b848-146">-ResourceId</span></span>
<span data-ttu-id="8b848-147">Define a propriedade de marcas ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b848-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="8b848-148">-Escopo</span><span class="sxs-lookup"><span data-stu-id="8b848-148">-Scope</span></span>
<span data-ttu-id="8b848-149">A lista de escopos do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="8b848-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="8b848-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b848-150">-Tag</span></span>
<span data-ttu-id="8b848-151">Define a propriedade de marcas do recurso de alerta do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="8b848-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="8b848-152">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8b848-152">-Confirm</span></span>
<span data-ttu-id="8b848-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b848-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b848-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b848-154">-WhatIf</span></span>
<span data-ttu-id="8b848-155">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8b848-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b848-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b848-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b848-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b848-157">CommonParameters</span></span>
<span data-ttu-id="8b848-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b848-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b848-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b848-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b848-160">Entradas</span><span class="sxs-lookup"><span data-stu-id="8b848-160">INPUTS</span></span>

### <span data-ttu-id="8b848-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8b848-161">System.String</span></span>

### <span data-ttu-id="8b848-162">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b848-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8b848-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlert PhishCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8b848-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8b848-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8b848-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8b848-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b848-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8b848-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8b848-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8b848-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="8b848-167">OUTPUTS</span></span>

### <span data-ttu-id="8b848-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="8b848-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="8b848-169">Notas</span><span class="sxs-lookup"><span data-stu-id="8b848-169">NOTES</span></span>

## <span data-ttu-id="8b848-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b848-170">RELATED LINKS</span></span>

[<span data-ttu-id="8b848-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8b848-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="8b848-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8b848-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="8b848-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8b848-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="8b848-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8b848-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="8b848-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8b848-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
