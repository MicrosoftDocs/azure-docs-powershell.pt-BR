---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 77d8792bf7499f2634ae525396568a9a21432f6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603368"
---
# <span data-ttu-id="3853f-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3853f-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="3853f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3853f-102">SYNOPSIS</span></span>
<span data-ttu-id="3853f-103">Cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="3853f-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3853f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3853f-104">SYNTAX</span></span>

### <span data-ttu-id="3853f-105">Parâmetros padrão para alerta de registro de atividades de definição</span><span class="sxs-lookup"><span data-stu-id="3853f-105">Default parameters for set activity log alert</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3853f-106">Parâmetros para definir um alerta de log de atividades levando o valor de ResourceId do pipe</span><span class="sxs-lookup"><span data-stu-id="3853f-106">Parameters to set an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3853f-107">Parâmetros para definir um valor de alertas do log de atividades a partir do pipe</span><span class="sxs-lookup"><span data-stu-id="3853f-107">Parameters to set an activity log alerts taking value from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3853f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3853f-108">DESCRIPTION</span></span>
<span data-ttu-id="3853f-109">O cmdlet **set-AzureRmActivityLogAlert** cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="3853f-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="3853f-110">Para marcas, condições e ações, os objetos devem ser criados antecipadamente e passados como parâmetros nesta chamada como uma vírgula separada (consulte o exemplo abaixo).</span><span class="sxs-lookup"><span data-stu-id="3853f-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="3853f-111">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar/modificar o recurso.</span><span class="sxs-lookup"><span data-stu-id="3853f-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

## <span data-ttu-id="3853f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3853f-112">EXAMPLES</span></span>

### <span data-ttu-id="3853f-113">Exemplo 1: criar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="3853f-113">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="3853f-114">Os primeiros quatro comandos criam a condição e o grupo de ação folha.</span><span class="sxs-lookup"><span data-stu-id="3853f-114">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="3853f-115">O comando final cria um alerta de log de atividades usando a condição e o grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="3853f-115">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="3853f-116">Exemplo 2: criar um alerta de log de atividades desabilitado</span><span class="sxs-lookup"><span data-stu-id="3853f-116">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="3853f-117">Os primeiros quatro comandos criam a condição e o grupo de ação folha.</span><span class="sxs-lookup"><span data-stu-id="3853f-117">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="3853f-118">O comando final cria um alerta de log de atividades usando a condição e o grupo de ação, mas cria o alerta desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3853f-118">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="3853f-119">Exemplo 3: definir um alerta de log de atividades baseado usando um valor do pipe ou o parâmetro InputObject</span><span class="sxs-lookup"><span data-stu-id="3853f-119">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="3853f-120">O primeiro comando é semelhante a um Nop, ele define o alerta com os mesmos valores que ele já continha o restante dos comandos recuperar a regra de alerta, alterar a descrição e desabilitá-la e usar o parâmetro InputObject para persistir essas alterações</span><span class="sxs-lookup"><span data-stu-id="3853f-120">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="3853f-121">Exemplo 4: definir um alerta de log de atividades baseado usando o valor de ResourceId do pipe</span><span class="sxs-lookup"><span data-stu-id="3853f-121">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="3853f-122">Se a regra de alerta de log fornecida existir, esse comando a desabilitará.</span><span class="sxs-lookup"><span data-stu-id="3853f-122">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="3853f-123">OS</span><span class="sxs-lookup"><span data-stu-id="3853f-123">PARAMETERS</span></span>

### <span data-ttu-id="3853f-124">-Local</span><span class="sxs-lookup"><span data-stu-id="3853f-124">-Location</span></span>
<span data-ttu-id="3853f-125">O local onde o alerta de log de atividades existirá.</span><span class="sxs-lookup"><span data-stu-id="3853f-125">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3853f-126">-Name</span></span>
<span data-ttu-id="3853f-127">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="3853f-127">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3853f-128">-ResourceGroupName</span></span>
<span data-ttu-id="3853f-129">O nome do grupo de recursos no qual o recurso de alerta vai existir.</span><span class="sxs-lookup"><span data-stu-id="3853f-129">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-130">-Escopo</span><span class="sxs-lookup"><span data-stu-id="3853f-130">-Scope</span></span>
<span data-ttu-id="3853f-131">A lista de escopos do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="3853f-131">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-132">-Condition</span><span class="sxs-lookup"><span data-stu-id="3853f-132">-Condition</span></span>
<span data-ttu-id="3853f-133">A lista de condições para o alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="3853f-133">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="3853f-134">**Observação** : na lista de condições, deve haver pelo menos um com o campo igual a "categoria".</span><span class="sxs-lookup"><span data-stu-id="3853f-134">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="3853f-135">O back-end responde com o 400 (BadRequest) se essa condição não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="3853f-135">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-136">-Ação</span><span class="sxs-lookup"><span data-stu-id="3853f-136">-Action</span></span>
<span data-ttu-id="3853f-137">A lista de grupos de ação para o alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="3853f-137">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-138">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="3853f-138">-DisableAlert</span></span>
<span data-ttu-id="3853f-139">Permite que o usuário crie um alerta de log de atividades desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3853f-139">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="3853f-140">Se não for especificado, os alertas serão criados habilitados.</span><span class="sxs-lookup"><span data-stu-id="3853f-140">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-141">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3853f-141">-Description</span></span>
<span data-ttu-id="3853f-142">A descrição do recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="3853f-142">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="3853f-143">-Tag</span></span>
<span data-ttu-id="3853f-144">Define a propriedade Tags do recurso de alerta do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="3853f-144">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3853f-145">-InputObject</span></span>
<span data-ttu-id="3853f-146">Define a propriedade InputObject Tag da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3853f-146">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3853f-147">-ResourceId</span></span>
<span data-ttu-id="3853f-148">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3853f-148">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3853f-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3853f-149">-Confirm</span></span>
<span data-ttu-id="3853f-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3853f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3853f-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3853f-151">-DefaultProfile</span></span>
<span data-ttu-id="3853f-152">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3853f-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3853f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3853f-153">-WhatIf</span></span>
<span data-ttu-id="3853f-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3853f-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3853f-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3853f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3853f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3853f-156">CommonParameters</span></span>
<span data-ttu-id="3853f-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3853f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3853f-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3853f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3853f-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3853f-159">INPUTS</span></span>

## <span data-ttu-id="3853f-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3853f-160">OUTPUTS</span></span>

### <span data-ttu-id="3853f-161">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="3853f-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="3853f-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3853f-162">NOTES</span></span>

## <span data-ttu-id="3853f-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3853f-163">RELATED LINKS</span></span>

[<span data-ttu-id="3853f-164">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3853f-164">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3853f-165">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3853f-165">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3853f-166">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3853f-166">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3853f-167">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3853f-167">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3853f-168">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="3853f-168">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="3853f-169">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="3853f-169">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
