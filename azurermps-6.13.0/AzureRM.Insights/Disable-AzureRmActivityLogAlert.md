---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 42107266ba38dff03c77336f14015853ef9b56c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602725"
---
# <span data-ttu-id="30084-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="30084-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="30084-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30084-102">SYNOPSIS</span></span>
<span data-ttu-id="30084-103">Desabilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="30084-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30084-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30084-104">SYNTAX</span></span>

### <span data-ttu-id="30084-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30084-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30084-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="30084-106">DisableByInputObject</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30084-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="30084-107">DisableByResourceId</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30084-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30084-108">DESCRIPTION</span></span>
<span data-ttu-id="30084-109">O cmdlet **Disable-AzureRmActivityLogAlert** desativa o Alert log de atividades e permite definir suas marcas.</span><span class="sxs-lookup"><span data-stu-id="30084-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="30084-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente aplicar o patch do recurso.</span><span class="sxs-lookup"><span data-stu-id="30084-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="30084-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30084-111">EXAMPLES</span></span>

### <span data-ttu-id="30084-112">Exemplo 1: desabilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="30084-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="30084-113">Esse comando desabilita o alerta de log de atividades chamado alert1 no grupo de recursos default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="30084-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="30084-114">Esse comando altera a propriedade Tags do alerta de log de atividades chamado alert1 e desabilita-o.</span><span class="sxs-lookup"><span data-stu-id="30084-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="30084-115">Exemplo 2: desabilitar um alerta de log de atividades usando um objeto PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="30084-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="30084-116">Esse comando desabilita um alerta de log de atividades chamado alert1.</span><span class="sxs-lookup"><span data-stu-id="30084-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="30084-117">Para isso, ele usa um objeto PSActivityLogAlertResource como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="30084-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="30084-118">Exemplo 3: desabilitar o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="30084-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="30084-119">Esse comando desabilita o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="30084-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="30084-120">OS</span><span class="sxs-lookup"><span data-stu-id="30084-120">PARAMETERS</span></span>

### <span data-ttu-id="30084-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30084-121">-DefaultProfile</span></span>
<span data-ttu-id="30084-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="30084-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30084-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30084-123">-InputObject</span></span>
<span data-ttu-id="30084-124">Define a propriedade InputObject da chamada para extrair o nome necessário, o nome do grupo de recursos e as propriedades de marca opcionais.</span><span class="sxs-lookup"><span data-stu-id="30084-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="30084-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="30084-125">-Name</span></span>
<span data-ttu-id="30084-126">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="30084-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="30084-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30084-127">-ResourceGroupName</span></span>
<span data-ttu-id="30084-128">O nome do grupo de recursos no qual o recurso de alerta vai existir.</span><span class="sxs-lookup"><span data-stu-id="30084-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="30084-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30084-129">-ResourceId</span></span>
<span data-ttu-id="30084-130">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="30084-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="30084-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="30084-131">-Confirm</span></span>
<span data-ttu-id="30084-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30084-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30084-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30084-133">-WhatIf</span></span>
<span data-ttu-id="30084-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="30084-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30084-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30084-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30084-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30084-136">CommonParameters</span></span>
<span data-ttu-id="30084-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30084-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30084-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30084-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30084-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30084-139">INPUTS</span></span>

### <span data-ttu-id="30084-140">System. String</span><span class="sxs-lookup"><span data-stu-id="30084-140">System.String</span></span>

### <span data-ttu-id="30084-141">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="30084-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="30084-142">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30084-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="30084-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30084-143">OUTPUTS</span></span>

### <span data-ttu-id="30084-144">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="30084-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="30084-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30084-145">NOTES</span></span>

## <span data-ttu-id="30084-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30084-146">RELATED LINKS</span></span>

[<span data-ttu-id="30084-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="30084-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="30084-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="30084-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="30084-149">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="30084-149">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="30084-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="30084-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="30084-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="30084-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="30084-152">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="30084-152">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
