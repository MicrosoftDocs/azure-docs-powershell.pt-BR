---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 3421eec7fa723767db0dc896d0c3c40e7c5cbebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893283"
---
# <span data-ttu-id="7ab30-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="7ab30-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="7ab30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ab30-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab30-103">Objeto de distribuição genérica</span><span class="sxs-lookup"><span data-stu-id="7ab30-103">Generic distribution object</span></span>

## <span data-ttu-id="7ab30-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ab30-104">SYNTAX</span></span>

### <span data-ttu-id="7ab30-105">ManagedImageDistributor (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7ab30-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="7ab30-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="7ab30-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="7ab30-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="7ab30-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="7ab30-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ab30-108">DESCRIPTION</span></span>
<span data-ttu-id="7ab30-109">Objeto de distribuição genérica</span><span class="sxs-lookup"><span data-stu-id="7ab30-109">Generic distribution object</span></span>

## <span data-ttu-id="7ab30-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ab30-110">EXAMPLES</span></span>

### <span data-ttu-id="7ab30-111">Exemplo 1: Criar um distribuidor de imagem gerenciado</span><span class="sxs-lookup"><span data-stu-id="7ab30-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="7ab30-112">Este comando cria um distribuidor de imagem gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7ab30-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="7ab30-113">Exemplo 2: Criar um distribuidor VHD</span><span class="sxs-lookup"><span data-stu-id="7ab30-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="7ab30-114">Este comando cria um distribuidor VHD.</span><span class="sxs-lookup"><span data-stu-id="7ab30-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="7ab30-115">Exemplo 3: Criar um distribuidor de imagem compartilhado</span><span class="sxs-lookup"><span data-stu-id="7ab30-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="7ab30-116">Este comando cria um distribuidor de imagem compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7ab30-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="7ab30-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ab30-117">PARAMETERS</span></span>

### <span data-ttu-id="7ab30-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="7ab30-118">-ArtifactTag</span></span>
<span data-ttu-id="7ab30-119">Marcas que serão aplicadas ao artefato depois que ele tiver sido criado/atualizado pelo distribuidor.</span><span class="sxs-lookup"><span data-stu-id="7ab30-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="7ab30-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="7ab30-121">Sinalizador que indica se a versão de imagem criada deve ser excluída da versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="7ab30-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="7ab30-122">Omita usar o padrão (false).</span><span class="sxs-lookup"><span data-stu-id="7ab30-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="7ab30-123">-GalleryImageId</span></span>
<span data-ttu-id="7ab30-124">ID de recurso da imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="7ab30-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="7ab30-125">-ImageId</span></span>
<span data-ttu-id="7ab30-126">ID de recurso da Imagem de Disco Gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7ab30-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-127">-Location</span><span class="sxs-lookup"><span data-stu-id="7ab30-127">-Location</span></span>
<span data-ttu-id="7ab30-128">O local do Azure para a imagem deve corresponder se a imagem já existir.</span><span class="sxs-lookup"><span data-stu-id="7ab30-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="7ab30-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="7ab30-130">Distribuir como uma imagem de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7ab30-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="7ab30-131">-ReplicationRegion</span></span>
<span data-ttu-id="7ab30-132">Uma lista de regiões para as que a imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="7ab30-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="7ab30-133">-RunOutputName</span></span>
<span data-ttu-id="7ab30-134">O nome a ser usado para o RunOutput associado.</span><span class="sxs-lookup"><span data-stu-id="7ab30-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="7ab30-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="7ab30-135">-SharedImageDistributor</span></span>
<span data-ttu-id="7ab30-136">Distribuir por meio da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="7ab30-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7ab30-137">-StorageAccountType</span></span>
<span data-ttu-id="7ab30-138">Tipo de conta de armazenamento a ser usado para armazenar a imagem compartilhada.</span><span class="sxs-lookup"><span data-stu-id="7ab30-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="7ab30-139">Omita usar o padrão (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="7ab30-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="7ab30-140">-VhdDistributor</span></span>
<span data-ttu-id="7ab30-141">Distribuir por VHD em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7ab30-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab30-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab30-142">CommonParameters</span></span>
<span data-ttu-id="7ab30-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab30-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab30-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ab30-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab30-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ab30-145">INPUTS</span></span>

## <span data-ttu-id="7ab30-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ab30-146">OUTPUTS</span></span>

### <span data-ttu-id="7ab30-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="7ab30-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="7ab30-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ab30-148">NOTES</span></span>

<span data-ttu-id="7ab30-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7ab30-149">ALIASES</span></span>

## <span data-ttu-id="7ab30-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ab30-150">RELATED LINKS</span></span>

