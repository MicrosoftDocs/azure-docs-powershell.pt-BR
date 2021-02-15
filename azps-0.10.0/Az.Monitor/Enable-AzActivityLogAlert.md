---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 89a2d96b79fa771b18e085978c85c7a98da4e9b5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398760"
---
# <span data-ttu-id="d58be-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d58be-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="d58be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d58be-102">SYNOPSIS</span></span>
<span data-ttu-id="d58be-103">Habilita um alerta de log de atividades e define suas Marcas.</span><span class="sxs-lookup"><span data-stu-id="d58be-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="d58be-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d58be-104">SYNTAX</span></span>

### <span data-ttu-id="d58be-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d58be-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58be-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="d58be-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58be-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="d58be-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d58be-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d58be-108">DESCRIPTION</span></span>
<span data-ttu-id="d58be-109">O cmdlet **Enable-AzActivityLogAlert** permite habilitar um alerta de log de atividades e definir suas marcas.</span><span class="sxs-lookup"><span data-stu-id="d58be-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="d58be-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente corrigir o recurso.</span><span class="sxs-lookup"><span data-stu-id="d58be-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="d58be-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d58be-111">EXAMPLES</span></span>

### <span data-ttu-id="d58be-112">Exemplo 1: Habilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="d58be-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="d58be-113">Esse comando habilita o alerta de log de atividades chamado alerta1 no grupo de recursos Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="d58be-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="d58be-114">Exemplo 2: Habilitar um alerta de log de atividades usando um objeto PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="d58be-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="d58be-115">Esse comando habilita um alerta de log de atividades chamado alerta1.</span><span class="sxs-lookup"><span data-stu-id="d58be-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="d58be-116">Para isso, ele usa um objeto PSActivityLogAlertResource como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="d58be-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="d58be-117">Exemplo 3: Habilitar o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="d58be-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="d58be-118">Esse comando habilita o ActivityLogAlert usando o parâmetro ResourceId do cano.</span><span class="sxs-lookup"><span data-stu-id="d58be-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="d58be-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d58be-119">PARAMETERS</span></span>

### <span data-ttu-id="d58be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58be-120">-DefaultProfile</span></span>
<span data-ttu-id="d58be-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d58be-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d58be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d58be-122">-InputObject</span></span>
<span data-ttu-id="d58be-123">Define a propriedade de marcas InputObject da chamada para extrair o nome necessário, o nome do grupo de recursos e as propriedades de marcas opcionais.</span><span class="sxs-lookup"><span data-stu-id="d58be-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d58be-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d58be-124">-Name</span></span>
<span data-ttu-id="d58be-125">O nome do alerta do log de atividades.</span><span class="sxs-lookup"><span data-stu-id="d58be-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58be-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d58be-126">-ResourceGroupName</span></span>
<span data-ttu-id="d58be-127">O nome do grupo de recursos onde o recurso de alerta existirá.</span><span class="sxs-lookup"><span data-stu-id="d58be-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58be-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d58be-128">-ResourceId</span></span>
<span data-ttu-id="d58be-129">Define a propriedade de marcas ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d58be-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58be-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d58be-130">-Confirm</span></span>
<span data-ttu-id="d58be-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58be-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d58be-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58be-132">-WhatIf</span></span>
<span data-ttu-id="d58be-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d58be-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d58be-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d58be-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d58be-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58be-135">CommonParameters</span></span>
<span data-ttu-id="d58be-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58be-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58be-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d58be-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58be-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="d58be-138">INPUTS</span></span>

### <span data-ttu-id="d58be-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d58be-139">System.String</span></span>

### <span data-ttu-id="d58be-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="d58be-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="d58be-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="d58be-141">OUTPUTS</span></span>

### <span data-ttu-id="d58be-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="d58be-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="d58be-143">Notas</span><span class="sxs-lookup"><span data-stu-id="d58be-143">NOTES</span></span>

## <span data-ttu-id="d58be-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d58be-144">RELATED LINKS</span></span>

[<span data-ttu-id="d58be-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d58be-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="d58be-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d58be-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="d58be-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d58be-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="d58be-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="d58be-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="d58be-149">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d58be-149">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
