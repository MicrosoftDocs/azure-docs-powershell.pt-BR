---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611116"
---
# <span data-ttu-id="e3054-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e3054-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="e3054-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3054-102">SYNOPSIS</span></span>
<span data-ttu-id="e3054-103">Remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="e3054-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3054-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3054-104">SYNTAX</span></span>

### <span data-ttu-id="e3054-105">Parâmetros padrão para remover um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="e3054-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3054-106">Parâmetros para remover um valor de alertas do log de atividades da conexão</span><span class="sxs-lookup"><span data-stu-id="e3054-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3054-107">Parâmetros para remover os alertas do log de atividades que tomam o valor de ResourceId do pipe</span><span class="sxs-lookup"><span data-stu-id="e3054-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3054-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3054-108">DESCRIPTION</span></span>
<span data-ttu-id="e3054-109">O cmdlet **Remove-AzureRmActivityLogAlert** remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="e3054-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="e3054-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente aplicar o patch do recurso.</span><span class="sxs-lookup"><span data-stu-id="e3054-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="e3054-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3054-111">EXAMPLES</span></span>

### <span data-ttu-id="e3054-112">Exemplo 1: remover um alerta de log de atividades</span><span class="sxs-lookup"><span data-stu-id="e3054-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="e3054-113">Remove um alerta de log de atividades usando o nome e o nome do grupo de recursos como entradas.</span><span class="sxs-lookup"><span data-stu-id="e3054-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="e3054-114">Exemplo 2: remover um alerta de log de atividades usando um PSActivityLogAlertResource como entrada</span><span class="sxs-lookup"><span data-stu-id="e3054-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="e3054-115">Remove um alerta de log de atividades usando um PSActivityLogAlertResource como entrada.</span><span class="sxs-lookup"><span data-stu-id="e3054-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="e3054-116">Exemplo 3: remover o ActivityLogAlert usando o parâmetro ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3054-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="e3054-117">Esse comando Remove o ActivityLogAlert usando o parâmetro ResourceId do pipe.</span><span class="sxs-lookup"><span data-stu-id="e3054-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="e3054-118">OS</span><span class="sxs-lookup"><span data-stu-id="e3054-118">PARAMETERS</span></span>

### <span data-ttu-id="e3054-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3054-119">-Name</span></span>
<span data-ttu-id="e3054-120">O nome do alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="e3054-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3054-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3054-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3054-122">O nome do grupo de recursos onde existe o recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="e3054-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3054-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3054-123">-InputObject</span></span>
<span data-ttu-id="e3054-124">Define a propriedade InputObject Tag da chamada para extrair o nome necessário e as propriedades de nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3054-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3054-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3054-125">-ResourceId</span></span>
<span data-ttu-id="e3054-126">Define a propriedade Tags ResourceId da chamada para extrair o nome necessário, as propriedades do nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3054-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3054-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e3054-127">-Confirm</span></span>
<span data-ttu-id="e3054-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3054-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3054-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3054-129">-DefaultProfile</span></span>
<span data-ttu-id="e3054-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3054-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3054-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3054-131">-WhatIf</span></span>
<span data-ttu-id="e3054-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3054-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3054-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3054-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3054-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3054-134">CommonParameters</span></span>
<span data-ttu-id="e3054-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3054-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3054-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3054-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3054-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3054-137">INPUTS</span></span>

## <span data-ttu-id="e3054-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3054-138">OUTPUTS</span></span>

### <span data-ttu-id="e3054-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e3054-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e3054-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3054-140">NOTES</span></span>

## <span data-ttu-id="e3054-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3054-141">RELATED LINKS</span></span>

[<span data-ttu-id="e3054-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e3054-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e3054-143">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e3054-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e3054-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e3054-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e3054-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e3054-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e3054-146">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e3054-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="e3054-147">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e3054-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

