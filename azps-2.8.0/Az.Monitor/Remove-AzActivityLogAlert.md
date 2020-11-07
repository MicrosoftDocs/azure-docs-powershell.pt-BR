---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 1f1e6aa3d90bbb2569f4381b3ea047bce9e483ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772167"
---
# <span data-ttu-id="e5fba-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5fba-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="e5fba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5fba-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fba-103">Remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="e5fba-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="e5fba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5fba-104">SYNTAX</span></span>

### <span data-ttu-id="e5fba-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5fba-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5fba-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5fba-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5fba-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5fba-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5fba-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5fba-108">DESCRIPTION</span></span>
<span data-ttu-id="e5fba-109">O cmdlet **Remove-AzActivityLogAlert** remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="e5fba-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="e5fba-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente aplicar o patch do recurso.</span><span class="sxs-lookup"><span data-stu-id="e5fba-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="e5fba-111">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="e5fba-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e5fba-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5fba-112">EXAMPLES</span></span>

### <span data-ttu-id="e5fba-113">Exemplo 1: remover um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="e5fba-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="e5fba-114">Remove um alerta de log de atividades usando o nome e o nome do grupo de recursos como entradas.</span><span class="sxs-lookup"><span data-stu-id="e5fba-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="e5fba-115">Exemplo 2: remover um alerta de log de atividades usando um PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="e5fba-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="e5fba-116">Remove um alerta de log de atividades usando um PSActivityLogAlertResource como entrada.</span><span class="sxs-lookup"><span data-stu-id="e5fba-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="e5fba-117">Exemplo 3: remover o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5fba-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="e5fba-118">Esse comando Remove o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="e5fba-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="e5fba-119">OS</span><span class="sxs-lookup"><span data-stu-id="e5fba-119">PARAMETERS</span></span>

### <span data-ttu-id="e5fba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fba-120">-DefaultProfile</span></span>
<span data-ttu-id="e5fba-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e5fba-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5fba-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5fba-122">-InputObject</span></span>
<span data-ttu-id="e5fba-123">Define a propriedade InputObject Tag da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5fba-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="e5fba-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5fba-124">-Name</span></span>
<span data-ttu-id="e5fba-125">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="e5fba-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="e5fba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fba-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5fba-127">O nome do grupo de recursos onde existe o recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="e5fba-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="e5fba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5fba-128">-ResourceId</span></span>
<span data-ttu-id="e5fba-129">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5fba-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="e5fba-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e5fba-130">-Confirm</span></span>
<span data-ttu-id="e5fba-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5fba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5fba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fba-132">-WhatIf</span></span>
<span data-ttu-id="e5fba-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5fba-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5fba-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5fba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5fba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fba-135">CommonParameters</span></span>
<span data-ttu-id="e5fba-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fba-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5fba-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fba-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5fba-138">INPUTS</span></span>

### <span data-ttu-id="e5fba-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5fba-139">System.String</span></span>

### <span data-ttu-id="e5fba-140">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e5fba-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="e5fba-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5fba-141">OUTPUTS</span></span>

### <span data-ttu-id="e5fba-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e5fba-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e5fba-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5fba-143">NOTES</span></span>

## <span data-ttu-id="e5fba-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5fba-144">RELATED LINKS</span></span>

[<span data-ttu-id="e5fba-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5fba-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="e5fba-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5fba-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="e5fba-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5fba-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e5fba-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5fba-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="e5fba-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e5fba-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="e5fba-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e5fba-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
