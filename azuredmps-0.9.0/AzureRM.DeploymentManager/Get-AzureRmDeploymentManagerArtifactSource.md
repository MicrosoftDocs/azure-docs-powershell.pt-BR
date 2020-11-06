---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601782"
---
# <span data-ttu-id="011d9-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="011d9-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="011d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="011d9-102">SYNOPSIS</span></span>
<span data-ttu-id="011d9-103">Obtém uma fonte de artefatos.</span><span class="sxs-lookup"><span data-stu-id="011d9-103">Gets an artifact source.</span></span>

## <span data-ttu-id="011d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="011d9-104">SYNTAX</span></span>

### <span data-ttu-id="011d9-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="011d9-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="011d9-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="011d9-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="011d9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="011d9-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="011d9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="011d9-108">DESCRIPTION</span></span>
<span data-ttu-id="011d9-109">O cmdlet **Get-AzureRmDeploymentManagerArtifactSource** Obtém uma fonte de artefato e retorna um objeto que representa essa fonte de artefatos.</span><span class="sxs-lookup"><span data-stu-id="011d9-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="011d9-110">Especifique a origem do artefato por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="011d9-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="011d9-111">Como alternativa, você pode fornecer o objeto artefato ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="011d9-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="011d9-112">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à fonte de artefatos usando o cmdlet Set-AzureRmDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="011d9-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="011d9-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="011d9-113">EXAMPLES</span></span>

### <span data-ttu-id="011d9-114">Exemplo 1: obter uma fonte de artefato</span><span class="sxs-lookup"><span data-stu-id="011d9-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="011d9-115">Esse comando obtém uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="011d9-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="011d9-116">Exemplo 2: obter uma fonte de artefato usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="011d9-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="011d9-117">Esse comando obtém uma fonte de artefato chamada ContosoArtifactSource em ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="011d9-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="011d9-118">Exemplo 3: obter uma fonte de artefato usando um objeto retornado por New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="011d9-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="011d9-119">Esse comando obtém uma fonte de artefato cujo nome e o nome do participante correspondem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="011d9-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="011d9-120">OS</span><span class="sxs-lookup"><span data-stu-id="011d9-120">PARAMETERS</span></span>

### <span data-ttu-id="011d9-121">-Artefatoname</span><span class="sxs-lookup"><span data-stu-id="011d9-121">-ArtifactSource</span></span>
<span data-ttu-id="011d9-122">Objeto de origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="011d9-122">Artifact Source object.</span></span>

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

### <span data-ttu-id="011d9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011d9-123">-DefaultProfile</span></span>
<span data-ttu-id="011d9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="011d9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="011d9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="011d9-125">-Name</span></span>
<span data-ttu-id="011d9-126">O nome da fonte do artefato.</span><span class="sxs-lookup"><span data-stu-id="011d9-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="011d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="011d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="011d9-128">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="011d9-128">The resource group.</span></span>

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

### <span data-ttu-id="011d9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="011d9-129">-ResourceId</span></span>
<span data-ttu-id="011d9-130">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="011d9-130">The resource identifier.</span></span>

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

### <span data-ttu-id="011d9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011d9-131">CommonParameters</span></span>
<span data-ttu-id="011d9-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="011d9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011d9-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="011d9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011d9-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="011d9-134">INPUTS</span></span>

### <span data-ttu-id="011d9-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="011d9-135">None</span></span>

## <span data-ttu-id="011d9-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="011d9-136">OUTPUTS</span></span>

### <span data-ttu-id="011d9-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="011d9-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="011d9-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="011d9-138">NOTES</span></span>

## <span data-ttu-id="011d9-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="011d9-139">RELATED LINKS</span></span>

[<span data-ttu-id="011d9-140">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="011d9-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="011d9-141">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="011d9-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="011d9-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="011d9-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)