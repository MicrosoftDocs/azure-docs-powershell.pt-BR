---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 6e3414efd21b1dd333f91e24333cda05ea650600
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259949"
---
# <span data-ttu-id="1e3d1-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1e3d1-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="1e3d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3d1-103">Habilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="1e3d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e3d1-104">SYNTAX</span></span>

### <span data-ttu-id="1e3d1-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e3d1-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e3d1-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e3d1-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e3d1-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e3d1-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e3d1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e3d1-108">DESCRIPTION</span></span>
<span data-ttu-id="1e3d1-109">O cmdlet **Enable-AzActivityLogAlert** permite habilitar um alerta de log de atividades e definir suas marcas.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="1e3d1-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente aplicar o patch do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="1e3d1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e3d1-111">EXAMPLES</span></span>

### <span data-ttu-id="1e3d1-112">Exemplo 1: habilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="1e3d1-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="1e3d1-113">Esse comando habilita o alerta do log de atividades chamado alert1 no grupo de recursos padrão-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="1e3d1-114">Exemplo 2: habilitar um alerta de log de atividades usando um objeto PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="1e3d1-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="1e3d1-115">Esse comando habilita um alerta de log de atividades chamado alert1.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="1e3d1-116">Para isso, ele usa um objeto PSActivityLogAlertResource como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="1e3d1-117">Exemplo 3: habilitar o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e3d1-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="1e3d1-118">Esse comando habilita o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="1e3d1-119">OS</span><span class="sxs-lookup"><span data-stu-id="1e3d1-119">PARAMETERS</span></span>

### <span data-ttu-id="1e3d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3d1-120">-DefaultProfile</span></span>
<span data-ttu-id="1e3d1-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1e3d1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e3d1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e3d1-122">-InputObject</span></span>
<span data-ttu-id="1e3d1-123">Define a propriedade InputObject da chamada para extrair o nome necessário, o nome do grupo de recursos e as propriedades de marcas opcionais.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="1e3d1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e3d1-124">-Name</span></span>
<span data-ttu-id="1e3d1-125">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="1e3d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e3d1-127">O nome do grupo de recursos no qual o recurso de alerta vai existir.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="1e3d1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e3d1-128">-ResourceId</span></span>
<span data-ttu-id="1e3d1-129">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="1e3d1-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e3d1-130">-Confirm</span></span>
<span data-ttu-id="1e3d1-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e3d1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3d1-132">-WhatIf</span></span>
<span data-ttu-id="1e3d1-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e3d1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e3d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3d1-135">CommonParameters</span></span>
<span data-ttu-id="1e3d1-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e3d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3d1-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e3d1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3d1-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e3d1-138">INPUTS</span></span>

### <span data-ttu-id="1e3d1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3d1-139">System.String</span></span>

### <span data-ttu-id="1e3d1-140">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1e3d1-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1e3d1-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e3d1-141">OUTPUTS</span></span>

### <span data-ttu-id="1e3d1-142">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1e3d1-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1e3d1-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e3d1-143">NOTES</span></span>

## <span data-ttu-id="1e3d1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e3d1-144">RELATED LINKS</span></span>

[<span data-ttu-id="1e3d1-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1e3d1-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="1e3d1-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1e3d1-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="1e3d1-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1e3d1-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="1e3d1-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1e3d1-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="1e3d1-149">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="1e3d1-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="1e3d1-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1e3d1-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
