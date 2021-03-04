---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 819fb3427ae59291c6b6d78a9ce93ee4e519ee13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887182"
---
# <span data-ttu-id="3c63a-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3c63a-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="3c63a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c63a-102">SYNOPSIS</span></span>

<span data-ttu-id="3c63a-103">Obtém a origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="3c63a-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="3c63a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3c63a-104">SYNTAX</span></span>

### <span data-ttu-id="3c63a-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3c63a-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c63a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c63a-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c63a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3c63a-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c63a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3c63a-108">DESCRIPTION</span></span>
<span data-ttu-id="3c63a-109">O cmdlet **Get-AzDeploymentManagerArtifactSource** obtém uma fonte de artefato e retorna um objeto que representa essa fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="3c63a-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="3c63a-110">Especifique a origem do artefato pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c63a-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="3c63a-111">Como alternativa, você pode fornecer o objeto ArtifactSource ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3c63a-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="3c63a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c63a-112">EXAMPLES</span></span>

### <span data-ttu-id="3c63a-113">Exemplo 1: Obter uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="3c63a-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="3c63a-114">Este comando obtém uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3c63a-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="3c63a-115">Exemplo 2: Obter uma fonte de artefato usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="3c63a-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="3c63a-116">Este comando obtém uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3c63a-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="3c63a-117">Exemplo 3: Obter uma fonte de artefato usando um objeto retornado por New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3c63a-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="3c63a-118">Este comando obtém uma fonte de artefato cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3c63a-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="3c63a-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3c63a-119">PARAMETERS</span></span>

### <span data-ttu-id="3c63a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c63a-120">-DefaultProfile</span></span>
<span data-ttu-id="3c63a-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c63a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c63a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c63a-122">-InputObject</span></span>
<span data-ttu-id="3c63a-123">Objeto Artifact Source.</span><span class="sxs-lookup"><span data-stu-id="3c63a-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="3c63a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3c63a-124">-Name</span></span>
<span data-ttu-id="3c63a-125">O nome da origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="3c63a-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c63a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c63a-126">-ResourceGroupName</span></span>
<span data-ttu-id="3c63a-127">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c63a-127">The resource group.</span></span>

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

### <span data-ttu-id="3c63a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c63a-128">-ResourceId</span></span>
<span data-ttu-id="3c63a-129">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="3c63a-129">The resource identifier.</span></span>

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

### <span data-ttu-id="3c63a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c63a-130">CommonParameters</span></span>
<span data-ttu-id="3c63a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c63a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c63a-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c63a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c63a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c63a-133">INPUTS</span></span>

### <span data-ttu-id="3c63a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3c63a-134">System.String</span></span>

### <span data-ttu-id="3c63a-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3c63a-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="3c63a-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3c63a-136">OUTPUTS</span></span>

### <span data-ttu-id="3c63a-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="3c63a-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="3c63a-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="3c63a-138">NOTES</span></span>

## <span data-ttu-id="3c63a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c63a-139">RELATED LINKS</span></span>
