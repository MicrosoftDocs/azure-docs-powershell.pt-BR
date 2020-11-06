---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425682"
---
# <span data-ttu-id="060a6-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="060a6-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="060a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="060a6-102">SYNOPSIS</span></span>
<span data-ttu-id="060a6-103">Exclui uma fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="060a6-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="060a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="060a6-104">SYNTAX</span></span>

### <span data-ttu-id="060a6-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="060a6-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="060a6-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="060a6-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="060a6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="060a6-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="060a6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="060a6-108">DESCRIPTION</span></span>
<span data-ttu-id="060a6-109">O cmdlet **Remove-AzureRmDeploymentManagerArtifactSource** exclui uma fonte de artefato especifica a origem do artefato por seu nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="060a6-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="060a6-110">Como alternativa, você pode fornecer o objeto artefato ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="060a6-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="060a6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="060a6-111">EXAMPLES</span></span>

### <span data-ttu-id="060a6-112">Exemplo 1: excluir uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="060a6-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="060a6-113">Esse comando exclui uma fonte de artefato nomeada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="060a6-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="060a6-114">Exemplo 2: excluir uma fonte de artefato usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="060a6-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="060a6-115">Esse comando exclui uma fonte de artefato nomeada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="060a6-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="060a6-116">Exemplo 3: excluir uma fonte de artefato usando um objeto</span><span class="sxs-lookup"><span data-stu-id="060a6-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="060a6-117">Esse comando exclui uma fonte de artefato cujo nome e o meu nome do participante correspondem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="060a6-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="060a6-118">OS</span><span class="sxs-lookup"><span data-stu-id="060a6-118">PARAMETERS</span></span>

### <span data-ttu-id="060a6-119">-Artefatoname</span><span class="sxs-lookup"><span data-stu-id="060a6-119">-ArtifactSource</span></span>
<span data-ttu-id="060a6-120">O repositório de artefatos a ser removido.</span><span class="sxs-lookup"><span data-stu-id="060a6-120">The artifact store to be removed.</span></span>

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

### <span data-ttu-id="060a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060a6-121">-DefaultProfile</span></span>
<span data-ttu-id="060a6-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="060a6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="060a6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="060a6-123">-Force</span></span>
<span data-ttu-id="060a6-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="060a6-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="060a6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="060a6-125">-Name</span></span>
<span data-ttu-id="060a6-126">O nome da fonte do artefato.</span><span class="sxs-lookup"><span data-stu-id="060a6-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060a6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="060a6-127">-PassThru</span></span>
<span data-ttu-id="060a6-128">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="060a6-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="060a6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="060a6-129">-ResourceGroupName</span></span>
<span data-ttu-id="060a6-130">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="060a6-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060a6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="060a6-131">-ResourceId</span></span>
<span data-ttu-id="060a6-132">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="060a6-132">The resource identifier.</span></span>

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

### <span data-ttu-id="060a6-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="060a6-133">-Confirm</span></span>
<span data-ttu-id="060a6-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="060a6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="060a6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="060a6-135">-WhatIf</span></span>
<span data-ttu-id="060a6-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="060a6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="060a6-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="060a6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="060a6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060a6-138">CommonParameters</span></span>
<span data-ttu-id="060a6-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="060a6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060a6-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="060a6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060a6-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="060a6-141">INPUTS</span></span>

### <span data-ttu-id="060a6-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="060a6-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="060a6-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="060a6-143">OUTPUTS</span></span>

### <span data-ttu-id="060a6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="060a6-144">System.Boolean</span></span>

## <span data-ttu-id="060a6-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="060a6-145">NOTES</span></span>

## <span data-ttu-id="060a6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="060a6-146">RELATED LINKS</span></span>

[<span data-ttu-id="060a6-147">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="060a6-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="060a6-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="060a6-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="060a6-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="060a6-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)