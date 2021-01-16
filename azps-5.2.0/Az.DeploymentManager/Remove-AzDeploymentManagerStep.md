---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259381"
---
# <span data-ttu-id="f55ae-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f55ae-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f55ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f55ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f55ae-103">Exclui a etapa.</span><span class="sxs-lookup"><span data-stu-id="f55ae-103">Deletes the step.</span></span>

## <span data-ttu-id="f55ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f55ae-104">SYNTAX</span></span>

### <span data-ttu-id="f55ae-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="f55ae-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55ae-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="f55ae-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55ae-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f55ae-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55ae-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f55ae-108">DESCRIPTION</span></span>
<span data-ttu-id="f55ae-109">O cmdlet **Remove-AzDeploymentManagerStep** exclui uma etapa.</span><span class="sxs-lookup"><span data-stu-id="f55ae-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="f55ae-110">Especifique a etapa pelo nome e pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f55ae-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="f55ae-111">Como alternativa, você pode fornecer o objeto Step ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f55ae-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="f55ae-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f55ae-112">EXAMPLES</span></span>

### <span data-ttu-id="f55ae-113">Exemplo 1: remover uma etapa</span><span class="sxs-lookup"><span data-stu-id="f55ae-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="f55ae-114">Esse comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f55ae-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f55ae-115">Exemplo 2: remover uma etapa usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="f55ae-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="f55ae-116">Esse comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f55ae-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f55ae-117">Exemplo 3: remover uma etapa usando um objeto retornado por New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f55ae-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="f55ae-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f55ae-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="f55ae-119">Esse comando exclui uma etapa cujo nome e o nome da fonte de renome coincidem com as propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f55ae-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="f55ae-120">OS</span><span class="sxs-lookup"><span data-stu-id="f55ae-120">PARAMETERS</span></span>

### <span data-ttu-id="f55ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55ae-121">-DefaultProfile</span></span>
<span data-ttu-id="f55ae-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f55ae-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f55ae-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f55ae-123">-InputObject</span></span>
<span data-ttu-id="f55ae-124">A etapa a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f55ae-124">The step to be removed.</span></span>

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

### <span data-ttu-id="f55ae-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f55ae-125">-Name</span></span>
<span data-ttu-id="f55ae-126">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="f55ae-126">The name of the step.</span></span>

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

### <span data-ttu-id="f55ae-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f55ae-127">-PassThru</span></span>
<span data-ttu-id="f55ae-128">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="f55ae-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f55ae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55ae-129">-ResourceGroupName</span></span>
<span data-ttu-id="f55ae-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f55ae-130">The resource group.</span></span>

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

### <span data-ttu-id="f55ae-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f55ae-131">-ResourceId</span></span>
<span data-ttu-id="f55ae-132">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="f55ae-132">The resource identifier.</span></span>

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

### <span data-ttu-id="f55ae-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f55ae-133">-Confirm</span></span>
<span data-ttu-id="f55ae-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55ae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55ae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55ae-135">-WhatIf</span></span>
<span data-ttu-id="f55ae-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f55ae-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f55ae-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f55ae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55ae-138">CommonParameters</span></span>
<span data-ttu-id="f55ae-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55ae-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f55ae-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55ae-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f55ae-141">INPUTS</span></span>

### <span data-ttu-id="f55ae-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f55ae-142">System.String</span></span>

### <span data-ttu-id="f55ae-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f55ae-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f55ae-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f55ae-144">OUTPUTS</span></span>

### <span data-ttu-id="f55ae-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f55ae-145">System.Boolean</span></span>

## <span data-ttu-id="f55ae-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f55ae-146">NOTES</span></span>

## <span data-ttu-id="f55ae-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f55ae-147">RELATED LINKS</span></span>
