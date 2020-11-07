---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 1dfd435d2797ee7430349546a5d2ba6fa2fe0023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785765"
---
# <span data-ttu-id="f2d07-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2d07-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="f2d07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2d07-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d07-103">Remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="f2d07-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2d07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2d07-104">SYNTAX</span></span>

### <span data-ttu-id="f2d07-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f2d07-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2d07-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2d07-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2d07-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2d07-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2d07-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2d07-108">DESCRIPTION</span></span>
<span data-ttu-id="f2d07-109">O cmdlet **Remove-AzureRmActivityLogAlert** remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="f2d07-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="f2d07-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente aplicar o patch do recurso.</span><span class="sxs-lookup"><span data-stu-id="f2d07-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="f2d07-111">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="f2d07-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f2d07-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2d07-112">EXAMPLES</span></span>

### <span data-ttu-id="f2d07-113">Exemplo 1: remover um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="f2d07-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="f2d07-114">Remove um alerta de log de atividades usando o nome e o nome do grupo de recursos como entradas.</span><span class="sxs-lookup"><span data-stu-id="f2d07-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="f2d07-115">Exemplo 2: remover um alerta de log de atividades usando um PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="f2d07-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="f2d07-116">Remove um alerta de log de atividades usando um PSActivityLogAlertResource como entrada.</span><span class="sxs-lookup"><span data-stu-id="f2d07-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="f2d07-117">Exemplo 3: remover o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2d07-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="f2d07-118">Esse comando Remove o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="f2d07-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="f2d07-119">OS</span><span class="sxs-lookup"><span data-stu-id="f2d07-119">PARAMETERS</span></span>

### <span data-ttu-id="f2d07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d07-120">-DefaultProfile</span></span>
<span data-ttu-id="f2d07-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f2d07-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2d07-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2d07-122">-InputObject</span></span>
<span data-ttu-id="f2d07-123">Define a propriedade InputObject Tag da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2d07-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="f2d07-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2d07-124">-Name</span></span>
<span data-ttu-id="f2d07-125">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="f2d07-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="f2d07-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d07-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2d07-127">O nome do grupo de recursos onde existe o recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="f2d07-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="f2d07-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2d07-128">-ResourceId</span></span>
<span data-ttu-id="f2d07-129">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2d07-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="f2d07-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2d07-130">-Confirm</span></span>
<span data-ttu-id="f2d07-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2d07-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2d07-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2d07-132">-WhatIf</span></span>
<span data-ttu-id="f2d07-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2d07-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2d07-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2d07-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2d07-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d07-135">CommonParameters</span></span>
<span data-ttu-id="f2d07-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d07-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d07-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d07-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d07-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2d07-138">INPUTS</span></span>

### <span data-ttu-id="f2d07-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f2d07-139">System.String</span></span>

### <span data-ttu-id="f2d07-140">Microsoft. Azure. Commands. insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="f2d07-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="f2d07-141">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2d07-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f2d07-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2d07-142">OUTPUTS</span></span>

### <span data-ttu-id="f2d07-143">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f2d07-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="f2d07-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2d07-144">NOTES</span></span>

## <span data-ttu-id="f2d07-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2d07-145">RELATED LINKS</span></span>

[<span data-ttu-id="f2d07-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2d07-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f2d07-147">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2d07-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f2d07-148">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2d07-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f2d07-149">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2d07-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f2d07-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="f2d07-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="f2d07-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="f2d07-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

