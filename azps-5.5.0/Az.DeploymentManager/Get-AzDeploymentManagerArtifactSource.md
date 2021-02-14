---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115847"
---
# <span data-ttu-id="629df-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="629df-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="629df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="629df-102">SYNOPSIS</span></span>

<span data-ttu-id="629df-103">Obtém a origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="629df-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="629df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="629df-104">SYNTAX</span></span>

### <span data-ttu-id="629df-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="629df-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="629df-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="629df-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="629df-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="629df-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="629df-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="629df-108">DESCRIPTION</span></span>
<span data-ttu-id="629df-109">O cmdlet **Get-AzDeploymentManagerArtifactSource** obtém uma fonte de artefato e retorna um objeto que representa essa fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="629df-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="629df-110">Especifique a fonte de artefato pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="629df-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="629df-111">Como alternativa, você pode fornecer o objeto ArtifactSource ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="629df-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="629df-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="629df-112">EXAMPLES</span></span>

### <span data-ttu-id="629df-113">Exemplo 1: Obter uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="629df-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="629df-114">Esse comando obtém uma fonte de artefato chamada ContosoArtifactSource no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="629df-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="629df-115">Exemplo 2: obter uma fonte de artefato usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="629df-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="629df-116">Esse comando obtém uma fonte de artefato chamada ContosoArtifactSource no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="629df-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="629df-117">Exemplo 3: obter uma fonte de artefato usando um objeto retornado por New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="629df-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="629df-118">Esse comando obtém uma fonte de artefato cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="629df-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="629df-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="629df-119">PARAMETERS</span></span>

### <span data-ttu-id="629df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="629df-120">-DefaultProfile</span></span>
<span data-ttu-id="629df-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="629df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="629df-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="629df-122">-InputObject</span></span>
<span data-ttu-id="629df-123">Objeto De origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="629df-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="629df-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="629df-124">-Name</span></span>
<span data-ttu-id="629df-125">O nome da origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="629df-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="629df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="629df-126">-ResourceGroupName</span></span>
<span data-ttu-id="629df-127">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="629df-127">The resource group.</span></span>

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

### <span data-ttu-id="629df-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="629df-128">-ResourceId</span></span>
<span data-ttu-id="629df-129">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="629df-129">The resource identifier.</span></span>

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

### <span data-ttu-id="629df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="629df-130">CommonParameters</span></span>
<span data-ttu-id="629df-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="629df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="629df-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="629df-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="629df-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="629df-133">INPUTS</span></span>

### <span data-ttu-id="629df-134">System.String</span><span class="sxs-lookup"><span data-stu-id="629df-134">System.String</span></span>

### <span data-ttu-id="629df-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="629df-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="629df-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="629df-136">OUTPUTS</span></span>

### <span data-ttu-id="629df-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="629df-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="629df-138">Notas</span><span class="sxs-lookup"><span data-stu-id="629df-138">NOTES</span></span>

## <span data-ttu-id="629df-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="629df-139">RELATED LINKS</span></span>
