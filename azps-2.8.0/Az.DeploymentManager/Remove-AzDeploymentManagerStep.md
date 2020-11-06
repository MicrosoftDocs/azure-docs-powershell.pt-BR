---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 6b95c1110368024c267bb56c3cdaa6eb3c9c68af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596642"
---
# <span data-ttu-id="acdf5-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="acdf5-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="acdf5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acdf5-102">SYNOPSIS</span></span>
<span data-ttu-id="acdf5-103">Exclui a etapa.</span><span class="sxs-lookup"><span data-stu-id="acdf5-103">Deletes the step.</span></span>

## <span data-ttu-id="acdf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acdf5-104">SYNTAX</span></span>

### <span data-ttu-id="acdf5-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="acdf5-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acdf5-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="acdf5-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acdf5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="acdf5-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acdf5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acdf5-108">DESCRIPTION</span></span>
<span data-ttu-id="acdf5-109">O cmdlet **Remove-AzDeploymentManagerStep** exclui uma etapa.</span><span class="sxs-lookup"><span data-stu-id="acdf5-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="acdf5-110">Especifique a etapa pelo nome e pelo nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="acdf5-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="acdf5-111">Como alternativa, você pode fornecer o objeto Step ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="acdf5-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="acdf5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acdf5-112">EXAMPLES</span></span>

### <span data-ttu-id="acdf5-113">Exemplo 1: remover uma etapa</span><span class="sxs-lookup"><span data-stu-id="acdf5-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="acdf5-114">Esse comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="acdf5-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="acdf5-115">Exemplo 2: remover uma etapa usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="acdf5-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="acdf5-116">Esse comando exclui uma etapa chamada ContosoService1WaitStep em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="acdf5-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="acdf5-117">Exemplo 3: remover uma etapa usando um objeto retornado por New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="acdf5-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="acdf5-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="acdf5-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="acdf5-119">Esse comando exclui uma etapa cujo nome e o nome da fonte de renome coincidem com as propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="acdf5-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="acdf5-120">OS</span><span class="sxs-lookup"><span data-stu-id="acdf5-120">PARAMETERS</span></span>

### <span data-ttu-id="acdf5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdf5-121">-DefaultProfile</span></span>
<span data-ttu-id="acdf5-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acdf5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acdf5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acdf5-123">-InputObject</span></span>
<span data-ttu-id="acdf5-124">A etapa a ser removida.</span><span class="sxs-lookup"><span data-stu-id="acdf5-124">The step to be removed.</span></span>

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

### <span data-ttu-id="acdf5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="acdf5-125">-Name</span></span>
<span data-ttu-id="acdf5-126">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="acdf5-126">The name of the step.</span></span>

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

### <span data-ttu-id="acdf5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acdf5-127">-PassThru</span></span>
<span data-ttu-id="acdf5-128">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="acdf5-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="acdf5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acdf5-129">-ResourceGroupName</span></span>
<span data-ttu-id="acdf5-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="acdf5-130">The resource group.</span></span>

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

### <span data-ttu-id="acdf5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acdf5-131">-ResourceId</span></span>
<span data-ttu-id="acdf5-132">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="acdf5-132">The resource identifier.</span></span>

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

### <span data-ttu-id="acdf5-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="acdf5-133">-Confirm</span></span>
<span data-ttu-id="acdf5-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acdf5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acdf5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acdf5-135">-WhatIf</span></span>
<span data-ttu-id="acdf5-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="acdf5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acdf5-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="acdf5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acdf5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdf5-138">CommonParameters</span></span>
<span data-ttu-id="acdf5-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acdf5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdf5-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acdf5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdf5-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acdf5-141">INPUTS</span></span>

### <span data-ttu-id="acdf5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="acdf5-142">System.String</span></span>

### <span data-ttu-id="acdf5-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="acdf5-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="acdf5-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acdf5-144">OUTPUTS</span></span>

### <span data-ttu-id="acdf5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="acdf5-145">System.Boolean</span></span>

## <span data-ttu-id="acdf5-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acdf5-146">NOTES</span></span>

## <span data-ttu-id="acdf5-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acdf5-147">RELATED LINKS</span></span>
