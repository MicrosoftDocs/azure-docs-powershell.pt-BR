---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116220"
---
# <span data-ttu-id="fdfc4-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="fdfc4-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="fdfc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdfc4-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfc4-103">Exclui a etapa.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-103">Deletes the step.</span></span>

## <span data-ttu-id="fdfc4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdfc4-104">SYNTAX</span></span>

### <span data-ttu-id="fdfc4-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fdfc4-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfc4-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="fdfc4-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfc4-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="fdfc4-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdfc4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdfc4-108">DESCRIPTION</span></span>
<span data-ttu-id="fdfc4-109">O cmdlet **Remove-AzDeploymentManagerStep** exclui uma etapa.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="fdfc4-110">Especifique a etapa pelo nome e pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="fdfc4-111">Como alternativa, você pode fornecer o objeto Step ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="fdfc4-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fdfc4-112">EXAMPLES</span></span>

### <span data-ttu-id="fdfc4-113">Exemplo 1: Remover uma etapa</span><span class="sxs-lookup"><span data-stu-id="fdfc4-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="fdfc4-114">Esse comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="fdfc4-115">Exemplo 2: Remover uma etapa usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="fdfc4-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="fdfc4-116">Esse comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="fdfc4-117">Exemplo 3: Remover uma etapa usando um objeto retornado por New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="fdfc4-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="fdfc4-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdfc4-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="fdfc4-119">Esse comando exclui uma etapa cujo nome e Grupo de Recursos corresponderem às propriedades Nome e ResourceGroupName da $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="fdfc4-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdfc4-120">PARAMETERS</span></span>

### <span data-ttu-id="fdfc4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfc4-121">-DefaultProfile</span></span>
<span data-ttu-id="fdfc4-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdfc4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdfc4-123">-InputObject</span></span>
<span data-ttu-id="fdfc4-124">A etapa a ser removida.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-124">The step to be removed.</span></span>

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

### <span data-ttu-id="fdfc4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdfc4-125">-Name</span></span>
<span data-ttu-id="fdfc4-126">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-126">The name of the step.</span></span>

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

### <span data-ttu-id="fdfc4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdfc4-127">-PassThru</span></span>
<span data-ttu-id="fdfc4-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fdfc4-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fdfc4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdfc4-129">-ResourceGroupName</span></span>
<span data-ttu-id="fdfc4-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-130">The resource group.</span></span>

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

### <span data-ttu-id="fdfc4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfc4-131">-ResourceId</span></span>
<span data-ttu-id="fdfc4-132">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-132">The resource identifier.</span></span>

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

### <span data-ttu-id="fdfc4-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fdfc4-133">-Confirm</span></span>
<span data-ttu-id="fdfc4-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdfc4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdfc4-135">-WhatIf</span></span>
<span data-ttu-id="fdfc4-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdfc4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdfc4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfc4-138">CommonParameters</span></span>
<span data-ttu-id="fdfc4-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdfc4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfc4-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdfc4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfc4-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="fdfc4-141">INPUTS</span></span>

### <span data-ttu-id="fdfc4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fdfc4-142">System.String</span></span>

### <span data-ttu-id="fdfc4-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="fdfc4-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="fdfc4-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="fdfc4-144">OUTPUTS</span></span>

### <span data-ttu-id="fdfc4-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fdfc4-145">System.Boolean</span></span>

## <span data-ttu-id="fdfc4-146">Notas</span><span class="sxs-lookup"><span data-stu-id="fdfc4-146">NOTES</span></span>

## <span data-ttu-id="fdfc4-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdfc4-147">RELATED LINKS</span></span>
