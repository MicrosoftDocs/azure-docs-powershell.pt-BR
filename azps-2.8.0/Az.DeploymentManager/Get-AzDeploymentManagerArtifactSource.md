---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 54cccbedc45977505b10526d4806b64c8118380e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596674"
---
# <span data-ttu-id="6ca02-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6ca02-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="6ca02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ca02-102">SYNOPSIS</span></span>

<span data-ttu-id="6ca02-103">Obtém a origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="6ca02-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="6ca02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ca02-104">SYNTAX</span></span>

### <span data-ttu-id="6ca02-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ca02-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ca02-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="6ca02-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ca02-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6ca02-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ca02-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ca02-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca02-109">O cmdlet **Get-AzDeploymentManagerArtifactSource** Obtém uma fonte de artefato e retorna um objeto que representa essa fonte de artefatos.</span><span class="sxs-lookup"><span data-stu-id="6ca02-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="6ca02-110">Especifique a origem do artefato por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ca02-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="6ca02-111">Como alternativa, você pode fornecer o objeto artefato ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6ca02-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="6ca02-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ca02-112">EXAMPLES</span></span>

### <span data-ttu-id="6ca02-113">Exemplo 1: obter uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="6ca02-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="6ca02-114">Esse comando obtém uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6ca02-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6ca02-115">Exemplo 2: obter uma fonte de artefato usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="6ca02-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="6ca02-116">Esse comando obtém uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6ca02-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6ca02-117">Exemplo 3: obter uma fonte de artefato usando um objeto retornado por New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6ca02-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="6ca02-118">Esse comando obtém uma fonte de artefato cujo nome e o nome do participante correspondem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6ca02-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="6ca02-119">OS</span><span class="sxs-lookup"><span data-stu-id="6ca02-119">PARAMETERS</span></span>

### <span data-ttu-id="6ca02-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca02-120">-DefaultProfile</span></span>
<span data-ttu-id="6ca02-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca02-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca02-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ca02-122">-InputObject</span></span>
<span data-ttu-id="6ca02-123">Objeto de origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="6ca02-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="6ca02-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ca02-124">-Name</span></span>
<span data-ttu-id="6ca02-125">O nome da fonte do artefato.</span><span class="sxs-lookup"><span data-stu-id="6ca02-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="6ca02-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca02-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ca02-127">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ca02-127">The resource group.</span></span>

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

### <span data-ttu-id="6ca02-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca02-128">-ResourceId</span></span>
<span data-ttu-id="6ca02-129">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="6ca02-129">The resource identifier.</span></span>

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

### <span data-ttu-id="6ca02-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca02-130">CommonParameters</span></span>
<span data-ttu-id="6ca02-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca02-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca02-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca02-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca02-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ca02-133">INPUTS</span></span>

### <span data-ttu-id="6ca02-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6ca02-134">System.String</span></span>

### <span data-ttu-id="6ca02-135">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6ca02-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="6ca02-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ca02-136">OUTPUTS</span></span>

### <span data-ttu-id="6ca02-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="6ca02-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="6ca02-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ca02-138">NOTES</span></span>

## <span data-ttu-id="6ca02-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ca02-139">RELATED LINKS</span></span>
