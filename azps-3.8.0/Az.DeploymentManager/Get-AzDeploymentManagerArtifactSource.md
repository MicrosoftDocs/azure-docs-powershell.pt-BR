---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944406"
---
# <span data-ttu-id="74c18-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="74c18-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="74c18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74c18-102">SYNOPSIS</span></span>

<span data-ttu-id="74c18-103">Obtém a origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="74c18-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="74c18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74c18-104">SYNTAX</span></span>

### <span data-ttu-id="74c18-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="74c18-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74c18-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="74c18-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74c18-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="74c18-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74c18-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74c18-108">DESCRIPTION</span></span>
<span data-ttu-id="74c18-109">O cmdlet **Get-AzDeploymentManagerArtifactSource** Obtém uma fonte de artefato e retorna um objeto que representa essa fonte de artefatos.</span><span class="sxs-lookup"><span data-stu-id="74c18-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="74c18-110">Especifique a origem do artefato por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74c18-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="74c18-111">Como alternativa, você pode fornecer o objeto artefato ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="74c18-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="74c18-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74c18-112">EXAMPLES</span></span>

### <span data-ttu-id="74c18-113">Exemplo 1: obter uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="74c18-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="74c18-114">Esse comando obtém uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="74c18-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="74c18-115">Exemplo 2: obter uma fonte de artefato usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="74c18-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="74c18-116">Esse comando obtém uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="74c18-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="74c18-117">Exemplo 3: obter uma fonte de artefato usando um objeto retornado por New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="74c18-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="74c18-118">Esse comando obtém uma fonte de artefato cujo nome e o nome do participante correspondem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="74c18-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="74c18-119">OS</span><span class="sxs-lookup"><span data-stu-id="74c18-119">PARAMETERS</span></span>

### <span data-ttu-id="74c18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c18-120">-DefaultProfile</span></span>
<span data-ttu-id="74c18-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74c18-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c18-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74c18-122">-InputObject</span></span>
<span data-ttu-id="74c18-123">Objeto de origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="74c18-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="74c18-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="74c18-124">-Name</span></span>
<span data-ttu-id="74c18-125">O nome da fonte do artefato.</span><span class="sxs-lookup"><span data-stu-id="74c18-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="74c18-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c18-126">-ResourceGroupName</span></span>
<span data-ttu-id="74c18-127">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74c18-127">The resource group.</span></span>

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

### <span data-ttu-id="74c18-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74c18-128">-ResourceId</span></span>
<span data-ttu-id="74c18-129">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="74c18-129">The resource identifier.</span></span>

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

### <span data-ttu-id="74c18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c18-130">CommonParameters</span></span>
<span data-ttu-id="74c18-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c18-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74c18-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c18-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74c18-133">INPUTS</span></span>

### <span data-ttu-id="74c18-134">System. String</span><span class="sxs-lookup"><span data-stu-id="74c18-134">System.String</span></span>

### <span data-ttu-id="74c18-135">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="74c18-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="74c18-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74c18-136">OUTPUTS</span></span>

### <span data-ttu-id="74c18-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="74c18-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="74c18-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74c18-138">NOTES</span></span>

## <span data-ttu-id="74c18-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74c18-139">RELATED LINKS</span></span>
