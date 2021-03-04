---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: 0f8e532e1bda9555c12cdf0770a5c2c986e8eac7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888915"
---
# <span data-ttu-id="e374c-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e374c-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="e374c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e374c-102">SYNOPSIS</span></span>
<span data-ttu-id="e374c-103">Desabilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="e374c-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="e374c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e374c-104">SYNTAX</span></span>

### <span data-ttu-id="e374c-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e374c-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e374c-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="e374c-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e374c-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="e374c-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e374c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e374c-108">DESCRIPTION</span></span>
<span data-ttu-id="e374c-109">O cmdlet **Disable-AzActivityLogAlert** desabilita e o alerta de log de atividades e permite definir suas marcas.</span><span class="sxs-lookup"><span data-stu-id="e374c-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="e374c-110">Este cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar a confirmação do usuário antes de realmente corrigir o recurso.</span><span class="sxs-lookup"><span data-stu-id="e374c-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="e374c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e374c-111">EXAMPLES</span></span>

### <span data-ttu-id="e374c-112">Exemplo 1: Desabilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="e374c-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="e374c-113">Este comando desabilita o alerta de log de atividades chamado alert1 no grupo de recursos Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="e374c-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="e374c-114">Esse comando altera a propriedade tags do alerta de log de atividade chamado alerta1 e o desabilita.</span><span class="sxs-lookup"><span data-stu-id="e374c-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="e374c-115">Exemplo 2: desabilitar um alerta de log de atividade usando um objeto PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="e374c-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="e374c-116">Este comando desabilita um alerta de log de atividades chamado alerta1.</span><span class="sxs-lookup"><span data-stu-id="e374c-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="e374c-117">Para isso, ele usa um objeto PSActivityLogAlertResource como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="e374c-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="e374c-118">Exemplo 3: Desabilitar o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="e374c-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="e374c-119">Este comando desabilita o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="e374c-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="e374c-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e374c-120">PARAMETERS</span></span>

### <span data-ttu-id="e374c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e374c-121">-DefaultProfile</span></span>
<span data-ttu-id="e374c-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e374c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e374c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e374c-123">-InputObject</span></span>
<span data-ttu-id="e374c-124">Define a propriedade InputObject tags da chamada para extrair o nome necessário, o nome do grupo de recursos e as propriedades de marca opcional.</span><span class="sxs-lookup"><span data-stu-id="e374c-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e374c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e374c-125">-Name</span></span>
<span data-ttu-id="e374c-126">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="e374c-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e374c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e374c-127">-ResourceGroupName</span></span>
<span data-ttu-id="e374c-128">O nome do grupo de recursos onde o recurso de alerta existirá.</span><span class="sxs-lookup"><span data-stu-id="e374c-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e374c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e374c-129">-ResourceId</span></span>
<span data-ttu-id="e374c-130">Define a propriedade de marcas ResourceId da chamada para extrair o nome necessário, propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e374c-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e374c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e374c-131">-Confirm</span></span>
<span data-ttu-id="e374c-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e374c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e374c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e374c-133">-WhatIf</span></span>
<span data-ttu-id="e374c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e374c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e374c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e374c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e374c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e374c-136">CommonParameters</span></span>
<span data-ttu-id="e374c-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e374c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e374c-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e374c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e374c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e374c-139">INPUTS</span></span>

### <span data-ttu-id="e374c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e374c-140">System.String</span></span>

### <span data-ttu-id="e374c-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e374c-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="e374c-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e374c-142">OUTPUTS</span></span>

### <span data-ttu-id="e374c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e374c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="e374c-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="e374c-144">NOTES</span></span>

## <span data-ttu-id="e374c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e374c-145">RELATED LINKS</span></span>

[<span data-ttu-id="e374c-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e374c-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e374c-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e374c-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="e374c-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e374c-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="e374c-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e374c-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="e374c-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e374c-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="e374c-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e374c-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
