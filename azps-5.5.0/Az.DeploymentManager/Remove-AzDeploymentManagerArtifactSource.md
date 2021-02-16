---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113238"
---
# <span data-ttu-id="610da-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="610da-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="610da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="610da-102">SYNOPSIS</span></span>
<span data-ttu-id="610da-103">Exclui a fonte de artefato especificada.</span><span class="sxs-lookup"><span data-stu-id="610da-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="610da-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="610da-104">SYNTAX</span></span>

### <span data-ttu-id="610da-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="610da-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610da-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="610da-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610da-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="610da-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="610da-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="610da-108">DESCRIPTION</span></span>
<span data-ttu-id="610da-109">O cmdlet **Remove-AzDeploymentManagerArtifactSource** exclui uma fonte de artefato Especifique a fonte de artefato pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="610da-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="610da-110">Como alternativa, você pode fornecer o objeto ArtifactSource ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="610da-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="610da-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="610da-111">EXAMPLES</span></span>

### <span data-ttu-id="610da-112">Exemplo 1: Excluir uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="610da-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="610da-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="610da-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="610da-114">Esse comando exclui uma fonte de artefato chamada ContosoArtifactSource no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="610da-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="610da-115">Exemplo 2: Excluir uma fonte de artefato usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="610da-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="610da-116">Esse comando exclui uma fonte de artefato chamada ContosoArtifactSource no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="610da-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="610da-117">Exemplo 3: Excluir uma fonte de artefato usando um objeto</span><span class="sxs-lookup"><span data-stu-id="610da-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="610da-118">Esse comando exclui uma fonte de artefato cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos da $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="610da-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="610da-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="610da-119">PARAMETERS</span></span>

### <span data-ttu-id="610da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610da-120">-DefaultProfile</span></span>
<span data-ttu-id="610da-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="610da-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="610da-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="610da-122">-InputObject</span></span>
<span data-ttu-id="610da-123">A origem do artefato a ser removida.</span><span class="sxs-lookup"><span data-stu-id="610da-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="610da-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="610da-124">-Name</span></span>
<span data-ttu-id="610da-125">O nome da origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="610da-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="610da-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="610da-126">-PassThru</span></span>
<span data-ttu-id="610da-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="610da-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="610da-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="610da-128">-ResourceGroupName</span></span>
<span data-ttu-id="610da-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="610da-129">The resource group.</span></span>

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

### <span data-ttu-id="610da-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="610da-130">-ResourceId</span></span>
<span data-ttu-id="610da-131">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="610da-131">The resource identifier.</span></span>

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

### <span data-ttu-id="610da-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="610da-132">-Confirm</span></span>
<span data-ttu-id="610da-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="610da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="610da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="610da-134">-WhatIf</span></span>
<span data-ttu-id="610da-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="610da-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="610da-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="610da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="610da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610da-137">CommonParameters</span></span>
<span data-ttu-id="610da-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="610da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610da-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="610da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610da-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="610da-140">INPUTS</span></span>

### <span data-ttu-id="610da-141">System.String</span><span class="sxs-lookup"><span data-stu-id="610da-141">System.String</span></span>

### <span data-ttu-id="610da-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="610da-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="610da-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="610da-143">OUTPUTS</span></span>

### <span data-ttu-id="610da-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="610da-144">System.Boolean</span></span>

## <span data-ttu-id="610da-145">Notas</span><span class="sxs-lookup"><span data-stu-id="610da-145">NOTES</span></span>

## <span data-ttu-id="610da-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="610da-146">RELATED LINKS</span></span>
