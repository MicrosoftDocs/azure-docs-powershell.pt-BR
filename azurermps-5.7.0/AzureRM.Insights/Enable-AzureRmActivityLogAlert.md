---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/enable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 67d1b91c58793560f619c4d69e2e957d30f37758
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432498"
---
# <span data-ttu-id="f941b-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f941b-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="f941b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f941b-102">SYNOPSIS</span></span>
<span data-ttu-id="f941b-103">Habilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="f941b-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f941b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f941b-104">SYNTAX</span></span>

### <span data-ttu-id="f941b-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f941b-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f941b-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="f941b-106">EnableByInputObject</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f941b-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="f941b-107">EnableByResourceId</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f941b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f941b-108">DESCRIPTION</span></span>
<span data-ttu-id="f941b-109">O cmdlet **Enable-AzureRmActivityLogAlert** permite habilitar um alerta de log de atividades e definir suas marcas.</span><span class="sxs-lookup"><span data-stu-id="f941b-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="f941b-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente aplicar o patch do recurso.</span><span class="sxs-lookup"><span data-stu-id="f941b-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="f941b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f941b-111">EXAMPLES</span></span>

### <span data-ttu-id="f941b-112">Exemplo 1: desabilitar um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="f941b-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="f941b-113">Esse comando habilita o alerta do log de atividades chamado alert1 no grupo de recursos padrão-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="f941b-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="f941b-114">Exemplo 2: habilitar um alerta de log de atividades usando um objeto PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="f941b-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="f941b-115">Esse comando habilita um alerta de log de atividades chamado alert1.</span><span class="sxs-lookup"><span data-stu-id="f941b-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="f941b-116">Para isso, ele usa um objeto PSActivityLogAlertResource como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="f941b-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="f941b-117">Exemplo 3: habilitar o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="f941b-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="f941b-118">Esse comando habilita o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="f941b-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="f941b-119">OS</span><span class="sxs-lookup"><span data-stu-id="f941b-119">PARAMETERS</span></span>

### <span data-ttu-id="f941b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f941b-120">-DefaultProfile</span></span>
<span data-ttu-id="f941b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f941b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f941b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f941b-122">-InputObject</span></span>
<span data-ttu-id="f941b-123">Define a propriedade InputObject da chamada para extrair o nome necessário, o nome do grupo de recursos e as propriedades de marcas opcionais.</span><span class="sxs-lookup"><span data-stu-id="f941b-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f941b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f941b-124">-Name</span></span>
<span data-ttu-id="f941b-125">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="f941b-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: EnableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f941b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f941b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f941b-127">O nome do grupo de recursos no qual o recurso de alerta vai existir.</span><span class="sxs-lookup"><span data-stu-id="f941b-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: String
Parameter Sets: EnableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f941b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f941b-128">-ResourceId</span></span>
<span data-ttu-id="f941b-129">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f941b-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: EnableByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f941b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f941b-130">-Confirm</span></span>
<span data-ttu-id="f941b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f941b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f941b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f941b-132">-WhatIf</span></span>
<span data-ttu-id="f941b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f941b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f941b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f941b-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f941b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f941b-135">CommonParameters</span></span>
<span data-ttu-id="f941b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f941b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f941b-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f941b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f941b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f941b-138">INPUTS</span></span>

### <span data-ttu-id="f941b-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f941b-139">None</span></span>
<span data-ttu-id="f941b-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f941b-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f941b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f941b-141">OUTPUTS</span></span>

### <span data-ttu-id="f941b-142">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="f941b-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="f941b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f941b-143">NOTES</span></span>

## <span data-ttu-id="f941b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f941b-144">RELATED LINKS</span></span>

[<span data-ttu-id="f941b-145">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f941b-145">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f941b-146">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f941b-146">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f941b-147">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f941b-147">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f941b-148">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="f941b-148">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="f941b-149">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="f941b-149">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="f941b-150">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f941b-150">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)