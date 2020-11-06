---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92607537fb80132627e1f26f240a10b8f7150fb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441054"
---
# <span data-ttu-id="4de42-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4de42-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="4de42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4de42-102">SYNOPSIS</span></span>
<span data-ttu-id="4de42-103">Habilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="4de42-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4de42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4de42-104">SYNTAX</span></span>

### <span data-ttu-id="4de42-105">Parâmetros padrão para habilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="4de42-105">Default parameters for enable an activity log alert</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4de42-106">Parâmetros para habilitar um valor de alertas do log de atividades da conexão</span><span class="sxs-lookup"><span data-stu-id="4de42-106">Parameters to enable an activity log alerts taking value from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4de42-107">Parâmetros para habilitar um alerta de log de atividades levando o valor de ResourceId do pipe</span><span class="sxs-lookup"><span data-stu-id="4de42-107">Parameters to enable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de42-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4de42-108">DESCRIPTION</span></span>
<span data-ttu-id="4de42-109">O cmdlet **Enable-AzureRmActivityLogAlert** permite habilitar um alerta de log de atividades e definir suas marcas.</span><span class="sxs-lookup"><span data-stu-id="4de42-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="4de42-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente aplicar o patch do recurso.</span><span class="sxs-lookup"><span data-stu-id="4de42-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="4de42-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4de42-111">EXAMPLES</span></span>

### <span data-ttu-id="4de42-112">Exemplo 1: desabilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="4de42-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="4de42-113">Esse comando habilita o alerta do log de atividades chamado alert1 no grupo de recursos padrão-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="4de42-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="4de42-114">Exemplo 2: habilitar um alerta de log de atividades usando um objeto PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="4de42-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="4de42-115">Esse comando habilita um alerta de log de atividades chamado alert1.</span><span class="sxs-lookup"><span data-stu-id="4de42-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="4de42-116">Para isso, ele usa um objeto PSActivityLogAlertResource como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="4de42-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="4de42-117">Exemplo 3: habilitar o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="4de42-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="4de42-118">Esse comando habilita o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="4de42-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="4de42-119">OS</span><span class="sxs-lookup"><span data-stu-id="4de42-119">PARAMETERS</span></span>

### <span data-ttu-id="4de42-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4de42-120">-Name</span></span>
<span data-ttu-id="4de42-121">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="4de42-121">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de42-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4de42-122">-ResourceGroupName</span></span>
<span data-ttu-id="4de42-123">O nome do grupo de recursos no qual o recurso de alerta vai existir.</span><span class="sxs-lookup"><span data-stu-id="4de42-123">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de42-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4de42-124">-InputObject</span></span>
<span data-ttu-id="4de42-125">Define a propriedade InputObject da chamada para extrair o nome necessário, o nome do grupo de recursos e as propriedades de marcas opcionais.</span><span class="sxs-lookup"><span data-stu-id="4de42-125">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to enable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4de42-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4de42-126">-ResourceId</span></span>
<span data-ttu-id="4de42-127">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4de42-127">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to enable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4de42-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4de42-128">-Confirm</span></span>
<span data-ttu-id="4de42-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4de42-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de42-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de42-130">-DefaultProfile</span></span>
<span data-ttu-id="4de42-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4de42-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4de42-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de42-132">-WhatIf</span></span>
<span data-ttu-id="4de42-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4de42-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4de42-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4de42-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de42-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de42-135">CommonParameters</span></span>
<span data-ttu-id="4de42-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de42-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de42-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de42-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de42-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4de42-138">INPUTS</span></span>

## <span data-ttu-id="4de42-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4de42-139">OUTPUTS</span></span>

### <span data-ttu-id="4de42-140">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="4de42-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="4de42-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4de42-141">NOTES</span></span>

## <span data-ttu-id="4de42-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4de42-142">RELATED LINKS</span></span>

[<span data-ttu-id="4de42-143">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4de42-143">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4de42-144">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4de42-144">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4de42-145">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4de42-145">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4de42-146">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4de42-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="4de42-147">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4de42-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="4de42-148">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4de42-148">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)