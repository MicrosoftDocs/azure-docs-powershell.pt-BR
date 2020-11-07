---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 4e628affbae7b5356b1cfaacb8970b5315be746d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770336"
---
# <span data-ttu-id="48bdb-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="48bdb-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="48bdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="48bdb-103">Habilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="48bdb-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="48bdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48bdb-104">SYNTAX</span></span>

### <span data-ttu-id="48bdb-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="48bdb-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48bdb-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="48bdb-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48bdb-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="48bdb-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48bdb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48bdb-108">DESCRIPTION</span></span>
<span data-ttu-id="48bdb-109">O cmdlet **Enable-AzActivityLogAlert** permite habilitar um alerta de log de atividades e definir suas marcas.</span><span class="sxs-lookup"><span data-stu-id="48bdb-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="48bdb-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente aplicar o patch do recurso.</span><span class="sxs-lookup"><span data-stu-id="48bdb-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="48bdb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48bdb-111">EXAMPLES</span></span>

### <span data-ttu-id="48bdb-112">Exemplo 1: habilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="48bdb-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="48bdb-113">Esse comando habilita o alerta do log de atividades chamado alert1 no grupo de recursos padrão-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="48bdb-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="48bdb-114">Exemplo 2: habilitar um alerta de log de atividades usando um objeto PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="48bdb-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="48bdb-115">Esse comando habilita um alerta de log de atividades chamado alert1.</span><span class="sxs-lookup"><span data-stu-id="48bdb-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="48bdb-116">Para isso, ele usa um objeto PSActivityLogAlertResource como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="48bdb-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="48bdb-117">Exemplo 3: habilitar o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="48bdb-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="48bdb-118">Esse comando habilita o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="48bdb-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="48bdb-119">OS</span><span class="sxs-lookup"><span data-stu-id="48bdb-119">PARAMETERS</span></span>

### <span data-ttu-id="48bdb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48bdb-120">-DefaultProfile</span></span>
<span data-ttu-id="48bdb-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="48bdb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48bdb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48bdb-122">-InputObject</span></span>
<span data-ttu-id="48bdb-123">Define a propriedade InputObject da chamada para extrair o nome necessário, o nome do grupo de recursos e as propriedades de marcas opcionais.</span><span class="sxs-lookup"><span data-stu-id="48bdb-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="48bdb-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="48bdb-124">-Name</span></span>
<span data-ttu-id="48bdb-125">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="48bdb-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="48bdb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48bdb-126">-ResourceGroupName</span></span>
<span data-ttu-id="48bdb-127">O nome do grupo de recursos no qual o recurso de alerta vai existir.</span><span class="sxs-lookup"><span data-stu-id="48bdb-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="48bdb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48bdb-128">-ResourceId</span></span>
<span data-ttu-id="48bdb-129">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48bdb-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="48bdb-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48bdb-130">-Confirm</span></span>
<span data-ttu-id="48bdb-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48bdb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48bdb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48bdb-132">-WhatIf</span></span>
<span data-ttu-id="48bdb-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48bdb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48bdb-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48bdb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48bdb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48bdb-135">CommonParameters</span></span>
<span data-ttu-id="48bdb-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48bdb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48bdb-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48bdb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48bdb-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48bdb-138">INPUTS</span></span>

### <span data-ttu-id="48bdb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="48bdb-139">System.String</span></span>

### <span data-ttu-id="48bdb-140">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="48bdb-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="48bdb-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48bdb-141">OUTPUTS</span></span>

### <span data-ttu-id="48bdb-142">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="48bdb-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="48bdb-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48bdb-143">NOTES</span></span>

## <span data-ttu-id="48bdb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48bdb-144">RELATED LINKS</span></span>

[<span data-ttu-id="48bdb-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="48bdb-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="48bdb-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="48bdb-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="48bdb-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="48bdb-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="48bdb-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="48bdb-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="48bdb-149">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="48bdb-149">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="48bdb-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="48bdb-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
