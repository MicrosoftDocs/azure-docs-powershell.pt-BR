---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: bdd854d3f9cc17071e17fea232b1d872b0a5fe8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117539"
---
# <span data-ttu-id="83575-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83575-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="83575-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83575-102">SYNOPSIS</span></span>
<span data-ttu-id="83575-103">Desabilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="83575-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="83575-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83575-104">SYNTAX</span></span>

### <span data-ttu-id="83575-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="83575-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83575-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="83575-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83575-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="83575-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83575-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="83575-108">DESCRIPTION</span></span>
<span data-ttu-id="83575-109">O cmdlet **Disable-AzActivityLogAlert** desabilita e alerta de log de atividades e permite definir suas marcas.</span><span class="sxs-lookup"><span data-stu-id="83575-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="83575-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente corrigir o recurso.</span><span class="sxs-lookup"><span data-stu-id="83575-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="83575-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="83575-111">EXAMPLES</span></span>

### <span data-ttu-id="83575-112">Exemplo 1: Desabilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="83575-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="83575-113">Esse comando desabilita o alerta de log de atividades chamado alerta1 no grupo de recursos Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="83575-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="83575-114">Esse comando altera a propriedade de marcas do alerta de log de atividades chamado alerta1 e o desabilita.</span><span class="sxs-lookup"><span data-stu-id="83575-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="83575-115">Exemplo 2: Desabilitar um alerta de log de atividades usando um objeto PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="83575-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="83575-116">Esse comando desabilita um alerta de log de atividades chamado alerta1.</span><span class="sxs-lookup"><span data-stu-id="83575-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="83575-117">Para isso, ele usa um objeto PSActivityLogAlertResource como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="83575-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="83575-118">Exemplo 3: Desabilitar o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="83575-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="83575-119">Esse comando desabilita o ActivityLogAlert usando o parâmetro ResourceId do cano.</span><span class="sxs-lookup"><span data-stu-id="83575-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="83575-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83575-120">PARAMETERS</span></span>

### <span data-ttu-id="83575-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83575-121">-DefaultProfile</span></span>
<span data-ttu-id="83575-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="83575-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83575-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83575-123">-InputObject</span></span>
<span data-ttu-id="83575-124">Define a propriedade de marcas InputObject da chamada para extrair o nome necessário, o nome do grupo de recursos e as propriedades de marca opcionais.</span><span class="sxs-lookup"><span data-stu-id="83575-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="83575-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="83575-125">-Name</span></span>
<span data-ttu-id="83575-126">O nome do alerta do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="83575-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="83575-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83575-127">-ResourceGroupName</span></span>
<span data-ttu-id="83575-128">O nome do grupo de recursos onde o recurso de alerta existirá.</span><span class="sxs-lookup"><span data-stu-id="83575-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="83575-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83575-129">-ResourceId</span></span>
<span data-ttu-id="83575-130">Define a propriedade de marcas ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="83575-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="83575-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="83575-131">-Confirm</span></span>
<span data-ttu-id="83575-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83575-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83575-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83575-133">-WhatIf</span></span>
<span data-ttu-id="83575-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="83575-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83575-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="83575-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83575-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83575-136">CommonParameters</span></span>
<span data-ttu-id="83575-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83575-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83575-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83575-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83575-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="83575-139">INPUTS</span></span>

### <span data-ttu-id="83575-140">System.String</span><span class="sxs-lookup"><span data-stu-id="83575-140">System.String</span></span>

### <span data-ttu-id="83575-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="83575-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="83575-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="83575-142">OUTPUTS</span></span>

### <span data-ttu-id="83575-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="83575-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="83575-144">Notas</span><span class="sxs-lookup"><span data-stu-id="83575-144">NOTES</span></span>

## <span data-ttu-id="83575-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83575-145">RELATED LINKS</span></span>

[<span data-ttu-id="83575-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83575-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="83575-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83575-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="83575-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83575-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="83575-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="83575-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="83575-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="83575-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="83575-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="83575-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
