---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 6aabb860c070aa458bffd24b56c5b56c63ea3a12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441274"
---
# <span data-ttu-id="22232-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="22232-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="22232-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22232-102">SYNOPSIS</span></span>
<span data-ttu-id="22232-103">Cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="22232-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22232-104">SYNTAX</span></span>

### <span data-ttu-id="22232-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22232-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22232-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="22232-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22232-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="22232-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22232-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22232-108">DESCRIPTION</span></span>
<span data-ttu-id="22232-109">O cmdlet **set-AzureRmActivityLogAlert** cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="22232-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="22232-110">Para marcas, condições e ações, os objetos devem ser criados antecipadamente e passados como parâmetros nesta chamada como uma vírgula separada (consulte o exemplo abaixo).</span><span class="sxs-lookup"><span data-stu-id="22232-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="22232-111">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar/modificar o recurso.</span><span class="sxs-lookup"><span data-stu-id="22232-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="22232-112">**Observação** : Este cmdlet e seus itens relacionados substituem o **Add-AzureRmLogAlertRule** preterido (novembro de 2017).</span><span class="sxs-lookup"><span data-stu-id="22232-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="22232-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22232-113">EXAMPLES</span></span>

### <span data-ttu-id="22232-114">Exemplo 1: criar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="22232-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="22232-115">Os primeiros quatro comandos criam a condição e o grupo de ação folha.</span><span class="sxs-lookup"><span data-stu-id="22232-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="22232-116">O comando final cria um alerta de log de atividades usando a condição e o grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="22232-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="22232-117">Exemplo 2: criar um alerta de log de atividades desabilitado</span><span class="sxs-lookup"><span data-stu-id="22232-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="22232-118">Os primeiros quatro comandos criam a condição e o grupo de ação folha.</span><span class="sxs-lookup"><span data-stu-id="22232-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="22232-119">O comando final cria um alerta de log de atividades usando a condição e o grupo de ação, mas cria o alerta desabilitado.</span><span class="sxs-lookup"><span data-stu-id="22232-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="22232-120">Exemplo 3: definir um alerta de log de atividades baseado usando um valor do pipe ou o parâmetro InputObject</span><span class="sxs-lookup"><span data-stu-id="22232-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="22232-121">O primeiro comando é semelhante a um Nop, ele define o alerta com os mesmos valores que ele já continha o restante dos comandos recuperar a regra de alerta, alterar a descrição e desabilitá-la e usar o parâmetro InputObject para persistir essas alterações</span><span class="sxs-lookup"><span data-stu-id="22232-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="22232-122">Exemplo 4: definir um alerta de log de atividades baseado usando o valor de ResourceId do pipe</span><span class="sxs-lookup"><span data-stu-id="22232-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="22232-123">Se a regra de alerta de log fornecida existir, esse comando a desabilitará.</span><span class="sxs-lookup"><span data-stu-id="22232-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="22232-124">OS</span><span class="sxs-lookup"><span data-stu-id="22232-124">PARAMETERS</span></span>

### <span data-ttu-id="22232-125">-Ação</span><span class="sxs-lookup"><span data-stu-id="22232-125">-Action</span></span>
<span data-ttu-id="22232-126">A lista de grupos de ação para o alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="22232-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="22232-127">-Condition</span><span class="sxs-lookup"><span data-stu-id="22232-127">-Condition</span></span>
<span data-ttu-id="22232-128">A lista de condições para o alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="22232-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="22232-129">**Observação** : na lista de condições, deve haver pelo menos um com o campo igual a "categoria".</span><span class="sxs-lookup"><span data-stu-id="22232-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="22232-130">O back-end responde com o 400 (BadRequest) se essa condição não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="22232-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="22232-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22232-131">-DefaultProfile</span></span>
<span data-ttu-id="22232-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="22232-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22232-133">-Descrição</span><span class="sxs-lookup"><span data-stu-id="22232-133">-Description</span></span>
<span data-ttu-id="22232-134">A descrição do recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="22232-134">The description of the alert resource.</span></span>

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

### <span data-ttu-id="22232-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="22232-135">-DisableAlert</span></span>
<span data-ttu-id="22232-136">Permite que o usuário crie um alerta de log de atividades desabilitado.</span><span class="sxs-lookup"><span data-stu-id="22232-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="22232-137">Se não for especificado, os alertas serão criados habilitados.</span><span class="sxs-lookup"><span data-stu-id="22232-137">If not given, the alerts are created enabled.</span></span>

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

### <span data-ttu-id="22232-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22232-138">-InputObject</span></span>
<span data-ttu-id="22232-139">Define a propriedade InputObject Tag da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22232-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="22232-140">-Local</span><span class="sxs-lookup"><span data-stu-id="22232-140">-Location</span></span>
<span data-ttu-id="22232-141">O local onde o alerta de log de atividades existirá.</span><span class="sxs-lookup"><span data-stu-id="22232-141">The location where the activity log alert will exist.</span></span>

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

### <span data-ttu-id="22232-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="22232-142">-Name</span></span>
<span data-ttu-id="22232-143">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="22232-143">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="22232-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22232-144">-ResourceGroupName</span></span>
<span data-ttu-id="22232-145">O nome do grupo de recursos no qual o recurso de alerta vai existir.</span><span class="sxs-lookup"><span data-stu-id="22232-145">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="22232-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22232-146">-ResourceId</span></span>
<span data-ttu-id="22232-147">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22232-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="22232-148">-Escopo</span><span class="sxs-lookup"><span data-stu-id="22232-148">-Scope</span></span>
<span data-ttu-id="22232-149">A lista de escopos do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="22232-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="22232-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="22232-150">-Tag</span></span>
<span data-ttu-id="22232-151">Define a propriedade Tags do recurso de alerta do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="22232-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="22232-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22232-152">-Confirm</span></span>
<span data-ttu-id="22232-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22232-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22232-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22232-154">-WhatIf</span></span>
<span data-ttu-id="22232-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22232-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22232-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22232-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22232-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22232-157">CommonParameters</span></span>
<span data-ttu-id="22232-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22232-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22232-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22232-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22232-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22232-160">INPUTS</span></span>

### <span data-ttu-id="22232-161">System. String</span><span class="sxs-lookup"><span data-stu-id="22232-161">System.String</span></span>

### <span data-ttu-id="22232-162">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22232-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="22232-163">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertLeafCondition, Microsoft. Azure. Commands. insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22232-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22232-164">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertActionGroup, Microsoft. Azure. Commands. insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22232-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22232-165">System. Collections. Generic. Dictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22232-165">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="22232-166">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="22232-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="22232-167">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22232-167">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="22232-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22232-168">OUTPUTS</span></span>

### <span data-ttu-id="22232-169">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="22232-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="22232-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22232-170">NOTES</span></span>

## <span data-ttu-id="22232-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22232-171">RELATED LINKS</span></span>

[<span data-ttu-id="22232-172">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="22232-172">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="22232-173">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="22232-173">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="22232-174">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="22232-174">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="22232-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="22232-175">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="22232-176">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="22232-176">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="22232-177">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="22232-177">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
