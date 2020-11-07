---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 2ce25f0881fff9ee684bcf234d13d847b7f28850
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948183"
---
# <span data-ttu-id="56b5b-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="56b5b-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="56b5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="56b5b-103">Cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="56b5b-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="56b5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56b5b-104">SYNTAX</span></span>

### <span data-ttu-id="56b5b-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56b5b-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56b5b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="56b5b-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56b5b-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="56b5b-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56b5b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56b5b-108">DESCRIPTION</span></span>
<span data-ttu-id="56b5b-109">O cmdlet **set-AzActivityLogAlert** cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="56b5b-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="56b5b-110">Para marcas, condições e ações, os objetos devem ser criados antecipadamente e passados como parâmetros nesta chamada como uma vírgula separada (consulte o exemplo abaixo).</span><span class="sxs-lookup"><span data-stu-id="56b5b-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="56b5b-111">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar/modificar o recurso.</span><span class="sxs-lookup"><span data-stu-id="56b5b-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="56b5b-112">**Observação** : Este cmdlet e seus itens relacionados substituem o **Add-AzLogAlertRule** preterido (novembro de 2017).</span><span class="sxs-lookup"><span data-stu-id="56b5b-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="56b5b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56b5b-113">EXAMPLES</span></span>

### <span data-ttu-id="56b5b-114">Exemplo 1: criar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="56b5b-114">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="56b5b-115">Os primeiros quatro comandos criam a condição e o grupo de ação folha.</span><span class="sxs-lookup"><span data-stu-id="56b5b-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="56b5b-116">O comando final cria um alerta de log de atividades usando a condição e o grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="56b5b-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="56b5b-117">Exemplo 2: criar um alerta de log de atividades desabilitado</span><span class="sxs-lookup"><span data-stu-id="56b5b-117">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="56b5b-118">Os primeiros quatro comandos criam a condição e o grupo de ação folha.</span><span class="sxs-lookup"><span data-stu-id="56b5b-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="56b5b-119">O comando final cria um alerta de log de atividades usando a condição e o grupo de ação, mas cria o alerta desabilitado.</span><span class="sxs-lookup"><span data-stu-id="56b5b-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="56b5b-120">Exemplo 3: definir um alerta de log de atividades baseado usando um valor do pipe ou o parâmetro InputObject</span><span class="sxs-lookup"><span data-stu-id="56b5b-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="56b5b-121">O primeiro comando é semelhante a um Nop, ele define o alerta com os mesmos valores que ele já continha o restante dos comandos recuperar a regra de alerta, alterar a descrição e desabilitá-la e usar o parâmetro InputObject para persistir essas alterações</span><span class="sxs-lookup"><span data-stu-id="56b5b-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="56b5b-122">Exemplo 4: definir um alerta de log de atividades baseado usando o valor de ResourceId do pipe</span><span class="sxs-lookup"><span data-stu-id="56b5b-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="56b5b-123">Se a regra de alerta de log fornecida existir, esse comando a desabilitará.</span><span class="sxs-lookup"><span data-stu-id="56b5b-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="56b5b-124">OS</span><span class="sxs-lookup"><span data-stu-id="56b5b-124">PARAMETERS</span></span>

### <span data-ttu-id="56b5b-125">-Ação</span><span class="sxs-lookup"><span data-stu-id="56b5b-125">-Action</span></span>
<span data-ttu-id="56b5b-126">A lista de grupos de ação para o alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="56b5b-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="56b5b-127">-Condition</span><span class="sxs-lookup"><span data-stu-id="56b5b-127">-Condition</span></span>
<span data-ttu-id="56b5b-128">A lista de condições para o alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="56b5b-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="56b5b-129">**Observação** : na lista de condições, deve haver pelo menos um com o campo igual a "categoria".</span><span class="sxs-lookup"><span data-stu-id="56b5b-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="56b5b-130">O back-end responde com o 400 (BadRequest) se essa condição não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="56b5b-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="56b5b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b5b-131">-DefaultProfile</span></span>
<span data-ttu-id="56b5b-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="56b5b-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56b5b-133">-Descrição</span><span class="sxs-lookup"><span data-stu-id="56b5b-133">-Description</span></span>
<span data-ttu-id="56b5b-134">A descrição do recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="56b5b-134">The description of the alert resource.</span></span>

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

### <span data-ttu-id="56b5b-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="56b5b-135">-DisableAlert</span></span>
<span data-ttu-id="56b5b-136">Permite que o usuário crie um alerta de log de atividades desabilitado.</span><span class="sxs-lookup"><span data-stu-id="56b5b-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="56b5b-137">Se não for especificado, os alertas serão criados habilitados.</span><span class="sxs-lookup"><span data-stu-id="56b5b-137">If not given, the alerts are created enabled.</span></span>

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

### <span data-ttu-id="56b5b-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56b5b-138">-InputObject</span></span>
<span data-ttu-id="56b5b-139">Define a propriedade InputObject Tag da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56b5b-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="56b5b-140">-Local</span><span class="sxs-lookup"><span data-stu-id="56b5b-140">-Location</span></span>
<span data-ttu-id="56b5b-141">O local onde o alerta de log de atividades existirá.</span><span class="sxs-lookup"><span data-stu-id="56b5b-141">The location where the activity log alert will exist.</span></span>

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

### <span data-ttu-id="56b5b-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="56b5b-142">-Name</span></span>
<span data-ttu-id="56b5b-143">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="56b5b-143">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="56b5b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b5b-144">-ResourceGroupName</span></span>
<span data-ttu-id="56b5b-145">O nome do grupo de recursos no qual o recurso de alerta vai existir.</span><span class="sxs-lookup"><span data-stu-id="56b5b-145">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="56b5b-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56b5b-146">-ResourceId</span></span>
<span data-ttu-id="56b5b-147">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56b5b-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="56b5b-148">-Escopo</span><span class="sxs-lookup"><span data-stu-id="56b5b-148">-Scope</span></span>
<span data-ttu-id="56b5b-149">A lista de escopos do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="56b5b-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="56b5b-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="56b5b-150">-Tag</span></span>
<span data-ttu-id="56b5b-151">Define a propriedade Tags do recurso de alerta do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="56b5b-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="56b5b-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="56b5b-152">-Confirm</span></span>
<span data-ttu-id="56b5b-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b5b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56b5b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56b5b-154">-WhatIf</span></span>
<span data-ttu-id="56b5b-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56b5b-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56b5b-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56b5b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56b5b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b5b-157">CommonParameters</span></span>
<span data-ttu-id="56b5b-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b5b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b5b-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56b5b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b5b-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56b5b-160">INPUTS</span></span>

### <span data-ttu-id="56b5b-161">System. String</span><span class="sxs-lookup"><span data-stu-id="56b5b-161">System.String</span></span>

### <span data-ttu-id="56b5b-162">System. Collections. Generic. List ' 1 [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="56b5b-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="56b5b-163">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="56b5b-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="56b5b-164">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertActionGroup, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="56b5b-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="56b5b-165">System. Collections. Generic. Dictionary ' 2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="56b5b-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="56b5b-166">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="56b5b-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="56b5b-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56b5b-167">OUTPUTS</span></span>

### <span data-ttu-id="56b5b-168">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="56b5b-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="56b5b-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56b5b-169">NOTES</span></span>

## <span data-ttu-id="56b5b-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56b5b-170">RELATED LINKS</span></span>

[<span data-ttu-id="56b5b-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="56b5b-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="56b5b-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="56b5b-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="56b5b-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="56b5b-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="56b5b-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="56b5b-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="56b5b-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="56b5b-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="56b5b-176">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="56b5b-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
