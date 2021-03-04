---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: b10d73e118b590a06c2af5a1755a59d219f9f180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886650"
---
# <span data-ttu-id="5336f-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5336f-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="5336f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5336f-102">SYNOPSIS</span></span>
<span data-ttu-id="5336f-103">Exclui a fonte de artefato especificada.</span><span class="sxs-lookup"><span data-stu-id="5336f-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="5336f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5336f-104">SYNTAX</span></span>

### <span data-ttu-id="5336f-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5336f-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5336f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5336f-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5336f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5336f-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5336f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5336f-108">DESCRIPTION</span></span>
<span data-ttu-id="5336f-109">O cmdlet **Remove-AzDeploymentManagerArtifactSource** exclui uma fonte de artefato Especifique a origem do artefato pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5336f-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="5336f-110">Como alternativa, você pode fornecer o objeto ArtifactSource ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5336f-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="5336f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5336f-111">EXAMPLES</span></span>

### <span data-ttu-id="5336f-112">Exemplo 1: Excluir uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="5336f-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="5336f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5336f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="5336f-114">Este comando exclui uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5336f-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5336f-115">Exemplo 2: Excluir uma fonte de artefato usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="5336f-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="5336f-116">Este comando exclui uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5336f-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5336f-117">Exemplo 3: Excluir uma fonte de artefato usando um objeto</span><span class="sxs-lookup"><span data-stu-id="5336f-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="5336f-118">Este comando exclui uma fonte de artefato cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5336f-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="5336f-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5336f-119">PARAMETERS</span></span>

### <span data-ttu-id="5336f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5336f-120">-DefaultProfile</span></span>
<span data-ttu-id="5336f-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5336f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5336f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5336f-122">-InputObject</span></span>
<span data-ttu-id="5336f-123">A origem do artefato a ser removida.</span><span class="sxs-lookup"><span data-stu-id="5336f-123">The artifact source to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5336f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5336f-124">-Name</span></span>
<span data-ttu-id="5336f-125">O nome da origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="5336f-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="5336f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5336f-126">-PassThru</span></span>
<span data-ttu-id="5336f-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5336f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5336f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5336f-128">-ResourceGroupName</span></span>
<span data-ttu-id="5336f-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5336f-129">The resource group.</span></span>

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

### <span data-ttu-id="5336f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5336f-130">-ResourceId</span></span>
<span data-ttu-id="5336f-131">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="5336f-131">The resource identifier.</span></span>

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

### <span data-ttu-id="5336f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5336f-132">-Confirm</span></span>
<span data-ttu-id="5336f-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5336f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5336f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5336f-134">-WhatIf</span></span>
<span data-ttu-id="5336f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5336f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5336f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5336f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5336f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5336f-137">CommonParameters</span></span>
<span data-ttu-id="5336f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5336f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5336f-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5336f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5336f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5336f-140">INPUTS</span></span>

### <span data-ttu-id="5336f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5336f-141">System.String</span></span>

### <span data-ttu-id="5336f-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5336f-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="5336f-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5336f-143">OUTPUTS</span></span>

### <span data-ttu-id="5336f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5336f-144">System.Boolean</span></span>

## <span data-ttu-id="5336f-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="5336f-145">NOTES</span></span>

## <span data-ttu-id="5336f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5336f-146">RELATED LINKS</span></span>
