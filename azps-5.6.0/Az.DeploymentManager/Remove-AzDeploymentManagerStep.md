---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 96f5f9e3dd0390d714b0ee7a74b3f585b46dcc1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887174"
---
# <span data-ttu-id="15c38-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="15c38-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="15c38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15c38-102">SYNOPSIS</span></span>
<span data-ttu-id="15c38-103">Exclui a etapa.</span><span class="sxs-lookup"><span data-stu-id="15c38-103">Deletes the step.</span></span>

## <span data-ttu-id="15c38-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="15c38-104">SYNTAX</span></span>

### <span data-ttu-id="15c38-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="15c38-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c38-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="15c38-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c38-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="15c38-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c38-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="15c38-108">DESCRIPTION</span></span>
<span data-ttu-id="15c38-109">O cmdlet **Remove-AzDeploymentManagerStep** exclui uma etapa.</span><span class="sxs-lookup"><span data-stu-id="15c38-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="15c38-110">Especifique a etapa pelo nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15c38-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="15c38-111">Como alternativa, você pode fornecer o objeto Step ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="15c38-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="15c38-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15c38-112">EXAMPLES</span></span>

### <span data-ttu-id="15c38-113">Exemplo 1: Remover uma etapa</span><span class="sxs-lookup"><span data-stu-id="15c38-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="15c38-114">Este comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="15c38-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="15c38-115">Exemplo 2: Remover uma etapa usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="15c38-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="15c38-116">Este comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="15c38-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="15c38-117">Exemplo 3: Remover uma etapa usando um objeto retornado por New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="15c38-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="15c38-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15c38-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="15c38-119">Este comando exclui uma etapa cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="15c38-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="15c38-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="15c38-120">PARAMETERS</span></span>

### <span data-ttu-id="15c38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c38-121">-DefaultProfile</span></span>
<span data-ttu-id="15c38-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15c38-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c38-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15c38-123">-InputObject</span></span>
<span data-ttu-id="15c38-124">A etapa a ser removida.</span><span class="sxs-lookup"><span data-stu-id="15c38-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15c38-125">-Name</span><span class="sxs-lookup"><span data-stu-id="15c38-125">-Name</span></span>
<span data-ttu-id="15c38-126">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="15c38-126">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c38-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15c38-127">-PassThru</span></span>
<span data-ttu-id="15c38-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="15c38-128">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c38-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c38-129">-ResourceGroupName</span></span>
<span data-ttu-id="15c38-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15c38-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c38-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15c38-131">-ResourceId</span></span>
<span data-ttu-id="15c38-132">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="15c38-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15c38-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15c38-133">-Confirm</span></span>
<span data-ttu-id="15c38-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15c38-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c38-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c38-135">-WhatIf</span></span>
<span data-ttu-id="15c38-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15c38-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15c38-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15c38-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c38-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c38-138">CommonParameters</span></span>
<span data-ttu-id="15c38-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c38-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c38-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15c38-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c38-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15c38-141">INPUTS</span></span>

### <span data-ttu-id="15c38-142">System.String</span><span class="sxs-lookup"><span data-stu-id="15c38-142">System.String</span></span>

### <span data-ttu-id="15c38-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="15c38-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="15c38-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="15c38-144">OUTPUTS</span></span>

### <span data-ttu-id="15c38-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15c38-145">System.Boolean</span></span>

## <span data-ttu-id="15c38-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="15c38-146">NOTES</span></span>

## <span data-ttu-id="15c38-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15c38-147">RELATED LINKS</span></span>
