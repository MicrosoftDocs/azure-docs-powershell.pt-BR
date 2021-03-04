---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: a69297afe49bb7cda0abc95cf97b371e04cac0ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886937"
---
# <span data-ttu-id="921cb-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="921cb-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="921cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="921cb-102">SYNOPSIS</span></span>
<span data-ttu-id="921cb-103">Remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="921cb-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="921cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="921cb-104">SYNTAX</span></span>

### <span data-ttu-id="921cb-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="921cb-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921cb-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="921cb-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921cb-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="921cb-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="921cb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="921cb-108">DESCRIPTION</span></span>
<span data-ttu-id="921cb-109">O cmdlet **Remove-AzActivityLogAlert** remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="921cb-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="921cb-110">Este cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar a confirmação do usuário antes de realmente corrigir o recurso.</span><span class="sxs-lookup"><span data-stu-id="921cb-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="921cb-111">Este cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="921cb-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="921cb-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="921cb-112">EXAMPLES</span></span>

### <span data-ttu-id="921cb-113">Exemplo 1: Remover um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="921cb-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="921cb-114">Remove um alerta de log de atividades usando o nome e o nome do grupo de recursos como entradas.</span><span class="sxs-lookup"><span data-stu-id="921cb-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="921cb-115">Exemplo 2: Remover um alerta de log de atividade usando um PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="921cb-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="921cb-116">Remove um alerta de log de atividades usando um PSActivityLogAlertResource como entrada.</span><span class="sxs-lookup"><span data-stu-id="921cb-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="921cb-117">Exemplo 3: Remover o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="921cb-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="921cb-118">Este comando remove o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="921cb-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="921cb-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="921cb-119">PARAMETERS</span></span>

### <span data-ttu-id="921cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921cb-120">-DefaultProfile</span></span>
<span data-ttu-id="921cb-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="921cb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="921cb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="921cb-122">-InputObject</span></span>
<span data-ttu-id="921cb-123">Define a propriedade InputObject tags da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="921cb-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="921cb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="921cb-124">-Name</span></span>
<span data-ttu-id="921cb-125">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="921cb-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921cb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="921cb-126">-ResourceGroupName</span></span>
<span data-ttu-id="921cb-127">O nome do grupo de recursos onde o recurso de alerta existe.</span><span class="sxs-lookup"><span data-stu-id="921cb-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921cb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="921cb-128">-ResourceId</span></span>
<span data-ttu-id="921cb-129">Define a propriedade de marcas ResourceId da chamada para extrair o nome necessário, propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="921cb-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921cb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="921cb-130">-Confirm</span></span>
<span data-ttu-id="921cb-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="921cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="921cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921cb-132">-WhatIf</span></span>
<span data-ttu-id="921cb-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="921cb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="921cb-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="921cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="921cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921cb-135">CommonParameters</span></span>
<span data-ttu-id="921cb-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="921cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921cb-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="921cb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921cb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="921cb-138">INPUTS</span></span>

### <span data-ttu-id="921cb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="921cb-139">System.String</span></span>

### <span data-ttu-id="921cb-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="921cb-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="921cb-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="921cb-141">OUTPUTS</span></span>

### <span data-ttu-id="921cb-142">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="921cb-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="921cb-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="921cb-143">NOTES</span></span>

## <span data-ttu-id="921cb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="921cb-144">RELATED LINKS</span></span>

[<span data-ttu-id="921cb-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="921cb-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="921cb-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="921cb-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="921cb-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="921cb-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="921cb-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="921cb-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="921cb-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="921cb-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="921cb-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="921cb-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

