---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 8aab061d7f61605273bd7147dc5a85ca45bf8ad0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887176"
---
# <span data-ttu-id="9389e-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9389e-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="9389e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9389e-102">SYNOPSIS</span></span>
<span data-ttu-id="9389e-103">Cria uma fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="9389e-103">Creates an artifact source.</span></span>

## <span data-ttu-id="9389e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9389e-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9389e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9389e-105">DESCRIPTION</span></span>
<span data-ttu-id="9389e-106">O cmdlet **New-AzDeploymentManagerArtifactSource** cria uma fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="9389e-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="9389e-107">*Especifique as propriedades Name*, *ResourceGroupName* e required.</span><span class="sxs-lookup"><span data-stu-id="9389e-107">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="9389e-108">Você pode modificar o objeto retornado localmente e aplicar as alterações à origem do artefato usando o cmdlet Set-AzDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="9389e-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="9389e-109">O cmdlet retorna um objeto ArtifactSource que tem um ResourceId que pode ser referenciado no cmdlet New-AzDeploymentManagerServiceTopology para que artefatos necessários para um recurso ServiceUnit, os arquivos Template e Parameters, possam ser referenciados a partir deste local.</span><span class="sxs-lookup"><span data-stu-id="9389e-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="9389e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9389e-110">EXAMPLES</span></span>

### <span data-ttu-id="9389e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9389e-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="9389e-112">Cria uma fonte de artefatos no ContosoResourceGroup com o nome ContosoArtifactSource com a Central US como o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9389e-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="9389e-113">A propriedade SasUri fornece um Uri do Azure Storage SAS para o contêiner de armazenamento onde os artefatos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="9389e-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="9389e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9389e-114">PARAMETERS</span></span>

### <span data-ttu-id="9389e-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="9389e-115">-ArtifactRoot</span></span>
<span data-ttu-id="9389e-116">O deslocamento de diretório opcional no contêiner de armazenamento dos artefatos.</span><span class="sxs-lookup"><span data-stu-id="9389e-116">The optional directory offset under the storage container for the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9389e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9389e-117">-DefaultProfile</span></span>
<span data-ttu-id="9389e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9389e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9389e-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9389e-119">-Location</span></span>
<span data-ttu-id="9389e-120">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9389e-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9389e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9389e-121">-Name</span></span>
<span data-ttu-id="9389e-122">O nome da origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="9389e-122">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9389e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9389e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9389e-124">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9389e-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9389e-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="9389e-125">-SasUri</span></span>
<span data-ttu-id="9389e-126">O Uri do SAS para o contêiner de armazenamento do Azure onde os artefatos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="9389e-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9389e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="9389e-127">-Tag</span></span>
<span data-ttu-id="9389e-128">Uma tabela de hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="9389e-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9389e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9389e-129">-Confirm</span></span>
<span data-ttu-id="9389e-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9389e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9389e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9389e-131">-WhatIf</span></span>
<span data-ttu-id="9389e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9389e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9389e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9389e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9389e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9389e-134">CommonParameters</span></span>
<span data-ttu-id="9389e-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9389e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9389e-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9389e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9389e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9389e-137">INPUTS</span></span>

### <span data-ttu-id="9389e-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9389e-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9389e-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9389e-139">OUTPUTS</span></span>

### <span data-ttu-id="9389e-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9389e-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="9389e-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="9389e-141">NOTES</span></span>

## <span data-ttu-id="9389e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9389e-142">RELATED LINKS</span></span>
