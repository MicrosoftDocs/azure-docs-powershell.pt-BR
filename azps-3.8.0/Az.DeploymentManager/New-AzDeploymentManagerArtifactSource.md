---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: dcd8d4164d091564aef3d3802430ab499eac38ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944388"
---
# <span data-ttu-id="17ad8-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="17ad8-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="17ad8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="17ad8-103">Cria uma fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="17ad8-103">Creates an artifact source.</span></span>

## <span data-ttu-id="17ad8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17ad8-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17ad8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="17ad8-106">O cmdlet **New-AzDeploymentManagerArtifactSource** cria uma fonte de artefato.</span><span class="sxs-lookup"><span data-stu-id="17ad8-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="17ad8-107">Especifique o *nome* , *ResourceGroupName* e propriedades necessárias.</span><span class="sxs-lookup"><span data-stu-id="17ad8-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="17ad8-108">Você pode modificar o objeto retornado localmente e, em seguida, aplicar as alterações à fonte de artefatos usando o cmdlet Set-AzDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="17ad8-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="17ad8-109">O cmdlet retorna um objeto artefato que tem um ResourceId que pode ser referenciado no cmdlet New-AzDeploymentManagerServiceTopology para que os artefatos necessários para um recurso de recurso, o modelo e os arquivos de parâmetros, possam ser referenciados neste local.</span><span class="sxs-lookup"><span data-stu-id="17ad8-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="17ad8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17ad8-110">EXAMPLES</span></span>

### <span data-ttu-id="17ad8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17ad8-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="17ad8-112">Cria uma fonte de artefatos no ContosoResourceGroup com o nome ContosoArtifactSource com EUA como o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="17ad8-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="17ad8-113">A propriedade SasUri fornece um URI de SAS de armazenamento do Azure para o contêiner de armazenamento em que os artefatos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="17ad8-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="17ad8-114">OS</span><span class="sxs-lookup"><span data-stu-id="17ad8-114">PARAMETERS</span></span>

### <span data-ttu-id="17ad8-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="17ad8-115">-ArtifactRoot</span></span>
<span data-ttu-id="17ad8-116">O deslocamento de diretório opcional abaixo do contêiner de armazenamento dos artefatos.</span><span class="sxs-lookup"><span data-stu-id="17ad8-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="17ad8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ad8-117">-DefaultProfile</span></span>
<span data-ttu-id="17ad8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17ad8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17ad8-119">-Local</span><span class="sxs-lookup"><span data-stu-id="17ad8-119">-Location</span></span>
<span data-ttu-id="17ad8-120">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="17ad8-120">The location of the resource.</span></span>

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

### <span data-ttu-id="17ad8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="17ad8-121">-Name</span></span>
<span data-ttu-id="17ad8-122">O nome da fonte do artefato.</span><span class="sxs-lookup"><span data-stu-id="17ad8-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="17ad8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ad8-123">-ResourceGroupName</span></span>
<span data-ttu-id="17ad8-124">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17ad8-124">The resource group.</span></span>

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

### <span data-ttu-id="17ad8-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="17ad8-125">-SasUri</span></span>
<span data-ttu-id="17ad8-126">O URI da SAS para o contêiner de armazenamento do Azure em que os artefatos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="17ad8-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="17ad8-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="17ad8-127">-Tag</span></span>
<span data-ttu-id="17ad8-128">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="17ad8-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="17ad8-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17ad8-129">-Confirm</span></span>
<span data-ttu-id="17ad8-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17ad8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17ad8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17ad8-131">-WhatIf</span></span>
<span data-ttu-id="17ad8-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17ad8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17ad8-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17ad8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17ad8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ad8-134">CommonParameters</span></span>
<span data-ttu-id="17ad8-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17ad8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ad8-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17ad8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ad8-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17ad8-137">INPUTS</span></span>

### <span data-ttu-id="17ad8-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="17ad8-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17ad8-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17ad8-139">OUTPUTS</span></span>

### <span data-ttu-id="17ad8-140">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="17ad8-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="17ad8-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17ad8-141">NOTES</span></span>

## <span data-ttu-id="17ad8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17ad8-142">RELATED LINKS</span></span>
