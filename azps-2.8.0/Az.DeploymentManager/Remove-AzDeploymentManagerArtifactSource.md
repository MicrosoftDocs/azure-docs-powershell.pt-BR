---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 1977fca9843c00d80d398a1dcd0bb967883cb5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596652"
---
# <span data-ttu-id="51f30-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="51f30-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="51f30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51f30-102">SYNOPSIS</span></span>
<span data-ttu-id="51f30-103">Exclui a fonte de artefato especificada.</span><span class="sxs-lookup"><span data-stu-id="51f30-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="51f30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51f30-104">SYNTAX</span></span>

### <span data-ttu-id="51f30-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="51f30-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51f30-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="51f30-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51f30-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="51f30-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f30-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51f30-108">DESCRIPTION</span></span>
<span data-ttu-id="51f30-109">O cmdlet **Remove-AzDeploymentManagerArtifactSource** exclui uma fonte de artefato especifica a origem do artefato por seu nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51f30-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="51f30-110">Como alternativa, você pode fornecer o objeto artefato ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="51f30-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="51f30-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51f30-111">EXAMPLES</span></span>

### <span data-ttu-id="51f30-112">Exemplo 1: excluir uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="51f30-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="51f30-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51f30-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="51f30-114">Esse comando exclui uma fonte de artefato nomeada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="51f30-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="51f30-115">Exemplo 2: excluir uma fonte de artefato usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="51f30-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="51f30-116">Esse comando exclui uma fonte de artefato nomeada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="51f30-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="51f30-117">Exemplo 3: excluir uma fonte de artefato usando um objeto</span><span class="sxs-lookup"><span data-stu-id="51f30-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="51f30-118">Esse comando exclui uma fonte de artefato cujo nome e o meu nome do participante correspondem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="51f30-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="51f30-119">OS</span><span class="sxs-lookup"><span data-stu-id="51f30-119">PARAMETERS</span></span>

### <span data-ttu-id="51f30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f30-120">-DefaultProfile</span></span>
<span data-ttu-id="51f30-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51f30-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51f30-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51f30-122">-InputObject</span></span>
<span data-ttu-id="51f30-123">A origem do artefato a ser removida.</span><span class="sxs-lookup"><span data-stu-id="51f30-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="51f30-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="51f30-124">-Name</span></span>
<span data-ttu-id="51f30-125">O nome da fonte do artefato.</span><span class="sxs-lookup"><span data-stu-id="51f30-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="51f30-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51f30-126">-PassThru</span></span>
<span data-ttu-id="51f30-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="51f30-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="51f30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51f30-128">-ResourceGroupName</span></span>
<span data-ttu-id="51f30-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51f30-129">The resource group.</span></span>

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

### <span data-ttu-id="51f30-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51f30-130">-ResourceId</span></span>
<span data-ttu-id="51f30-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="51f30-131">The resource identifier.</span></span>

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

### <span data-ttu-id="51f30-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51f30-132">-Confirm</span></span>
<span data-ttu-id="51f30-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f30-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51f30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f30-134">-WhatIf</span></span>
<span data-ttu-id="51f30-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51f30-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51f30-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51f30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51f30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f30-137">CommonParameters</span></span>
<span data-ttu-id="51f30-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f30-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f30-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f30-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51f30-140">INPUTS</span></span>

### <span data-ttu-id="51f30-141">System. String</span><span class="sxs-lookup"><span data-stu-id="51f30-141">System.String</span></span>

### <span data-ttu-id="51f30-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="51f30-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="51f30-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51f30-143">OUTPUTS</span></span>

### <span data-ttu-id="51f30-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51f30-144">System.Boolean</span></span>

## <span data-ttu-id="51f30-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51f30-145">NOTES</span></span>

## <span data-ttu-id="51f30-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51f30-146">RELATED LINKS</span></span>
