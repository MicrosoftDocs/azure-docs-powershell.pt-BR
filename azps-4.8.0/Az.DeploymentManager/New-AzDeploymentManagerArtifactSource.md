---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: dcd8d4164d091564aef3d3802430ab499eac38ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112809"
---
# <span data-ttu-id="e965c-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e965c-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="e965c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e965c-102">SYNOPSIS</span></span>
<span data-ttu-id="e965c-103">Cria uma fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="e965c-103">Creates an artifact source.</span></span>

## <span data-ttu-id="e965c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e965c-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e965c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e965c-105">DESCRIPTION</span></span>
<span data-ttu-id="e965c-106">O cmdlet **New-AzDeploymentManagerArtifactSource** cria uma fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="e965c-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="e965c-107">Especifique o *nome* , *ResourceGroupName* e propriedades necessárias.</span><span class="sxs-lookup"><span data-stu-id="e965c-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="e965c-108">Você pode modificar o objeto retornado localmente e, em seguida, aplicar as alterações à fonte de artefatos usando o cmdlet Set-AzDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="e965c-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="e965c-109">O cmdlet retorna um objeto artefato que tem um ResourceId que pode ser referenciado no cmdlet New-AzDeploymentManagerServiceTopology para que os artefatos necessários para um recurso de recurso, o modelo e os arquivos de parâmetros, possam ser referenciados neste local.</span><span class="sxs-lookup"><span data-stu-id="e965c-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="e965c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e965c-110">EXAMPLES</span></span>

### <span data-ttu-id="e965c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e965c-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="e965c-112">Cria uma fonte de artefatos no ContosoResourceGroup com o nome ContosoArtifactSource com EUA como o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e965c-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="e965c-113">A propriedade SasUri fornece um URI de SAS de armazenamento do Azure para o contêiner de armazenamento em que os artefatos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="e965c-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="e965c-114">OS</span><span class="sxs-lookup"><span data-stu-id="e965c-114">PARAMETERS</span></span>

### <span data-ttu-id="e965c-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="e965c-115">-ArtifactRoot</span></span>
<span data-ttu-id="e965c-116">O deslocamento de diretório opcional abaixo do contêiner de armazenamento dos artefatos.</span><span class="sxs-lookup"><span data-stu-id="e965c-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="e965c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e965c-117">-DefaultProfile</span></span>
<span data-ttu-id="e965c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e965c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e965c-119">-Local</span><span class="sxs-lookup"><span data-stu-id="e965c-119">-Location</span></span>
<span data-ttu-id="e965c-120">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e965c-120">The location of the resource.</span></span>

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

### <span data-ttu-id="e965c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e965c-121">-Name</span></span>
<span data-ttu-id="e965c-122">O nome da fonte do artefato.</span><span class="sxs-lookup"><span data-stu-id="e965c-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="e965c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e965c-123">-ResourceGroupName</span></span>
<span data-ttu-id="e965c-124">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e965c-124">The resource group.</span></span>

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

### <span data-ttu-id="e965c-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="e965c-125">-SasUri</span></span>
<span data-ttu-id="e965c-126">O URI da SAS para o contêiner de armazenamento do Azure em que os artefatos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="e965c-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="e965c-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="e965c-127">-Tag</span></span>
<span data-ttu-id="e965c-128">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="e965c-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e965c-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e965c-129">-Confirm</span></span>
<span data-ttu-id="e965c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e965c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e965c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e965c-131">-WhatIf</span></span>
<span data-ttu-id="e965c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e965c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e965c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e965c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e965c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e965c-134">CommonParameters</span></span>
<span data-ttu-id="e965c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e965c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e965c-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e965c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e965c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e965c-137">INPUTS</span></span>

### <span data-ttu-id="e965c-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e965c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e965c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e965c-139">OUTPUTS</span></span>

### <span data-ttu-id="e965c-140">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e965c-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="e965c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e965c-141">NOTES</span></span>

## <span data-ttu-id="e965c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e965c-142">RELATED LINKS</span></span>
