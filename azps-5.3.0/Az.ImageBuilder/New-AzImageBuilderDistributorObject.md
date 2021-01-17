---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429259"
---
# <span data-ttu-id="81532-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="81532-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="81532-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81532-102">SYNOPSIS</span></span>
<span data-ttu-id="81532-103">Objeto de distribuição genérico</span><span class="sxs-lookup"><span data-stu-id="81532-103">Generic distribution object</span></span>

## <span data-ttu-id="81532-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81532-104">SYNTAX</span></span>

### <span data-ttu-id="81532-105">ManagedImageDistributor (padrão)</span><span class="sxs-lookup"><span data-stu-id="81532-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="81532-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="81532-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="81532-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="81532-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="81532-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81532-108">DESCRIPTION</span></span>
<span data-ttu-id="81532-109">Objeto de distribuição genérico</span><span class="sxs-lookup"><span data-stu-id="81532-109">Generic distribution object</span></span>

## <span data-ttu-id="81532-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81532-110">EXAMPLES</span></span>

### <span data-ttu-id="81532-111">Exemplo 1: criar um distribuidor de imagens gerenciadas</span><span class="sxs-lookup"><span data-stu-id="81532-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="81532-112">Esse comando cria um distribuidor de imagens gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="81532-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="81532-113">Exemplo 2: criar um distribuidor VHD</span><span class="sxs-lookup"><span data-stu-id="81532-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="81532-114">Esse comando cria um distribuidor VHD.</span><span class="sxs-lookup"><span data-stu-id="81532-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="81532-115">Exemplo 3: criar um distribuidor de imagens compartilhadas</span><span class="sxs-lookup"><span data-stu-id="81532-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="81532-116">Esse comando cria um distribuidor de imagens compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="81532-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="81532-117">OS</span><span class="sxs-lookup"><span data-stu-id="81532-117">PARAMETERS</span></span>

### <span data-ttu-id="81532-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="81532-118">-ArtifactTag</span></span>
<span data-ttu-id="81532-119">Marcas que serão aplicadas ao artefato após a criação/atualização do distribuidor.</span><span class="sxs-lookup"><span data-stu-id="81532-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="81532-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="81532-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="81532-121">Sinalizador que indica se a versão da imagem criada deve ser excluída do mais recente.</span><span class="sxs-lookup"><span data-stu-id="81532-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="81532-122">Omita para usar o padrão (falso).</span><span class="sxs-lookup"><span data-stu-id="81532-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="81532-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="81532-123">-GalleryImageId</span></span>
<span data-ttu-id="81532-124">ID do recurso da imagem da Galeria de imagens compartilhada.</span><span class="sxs-lookup"><span data-stu-id="81532-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="81532-125">-Imageid</span><span class="sxs-lookup"><span data-stu-id="81532-125">-ImageId</span></span>
<span data-ttu-id="81532-126">ID do recurso da imagem de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="81532-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="81532-127">-Local</span><span class="sxs-lookup"><span data-stu-id="81532-127">-Location</span></span>
<span data-ttu-id="81532-128">O Azure Location para a imagem deve corresponder se a imagem já existe.</span><span class="sxs-lookup"><span data-stu-id="81532-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="81532-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="81532-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="81532-130">Distribuir como uma imagem de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="81532-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="81532-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="81532-131">-ReplicationRegion</span></span>
<span data-ttu-id="81532-132">Uma lista de regiões para as quais a imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="81532-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="81532-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="81532-133">-RunOutputName</span></span>
<span data-ttu-id="81532-134">O nome a ser usado para o RunOutput associado.</span><span class="sxs-lookup"><span data-stu-id="81532-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="81532-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="81532-135">-SharedImageDistributor</span></span>
<span data-ttu-id="81532-136">Distribuir via Galeria de imagens compartilhada.</span><span class="sxs-lookup"><span data-stu-id="81532-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="81532-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="81532-137">-StorageAccountType</span></span>
<span data-ttu-id="81532-138">Tipo de conta de armazenamento a ser usado para armazenar a imagem compartilhada.</span><span class="sxs-lookup"><span data-stu-id="81532-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="81532-139">Omita para usar o padrão (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="81532-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="81532-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="81532-140">-VhdDistributor</span></span>
<span data-ttu-id="81532-141">Distribuir via VHD em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="81532-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="81532-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81532-142">CommonParameters</span></span>
<span data-ttu-id="81532-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81532-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81532-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81532-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81532-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81532-145">INPUTS</span></span>

## <span data-ttu-id="81532-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81532-146">OUTPUTS</span></span>

### <span data-ttu-id="81532-147">Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="81532-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="81532-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81532-148">NOTES</span></span>

<span data-ttu-id="81532-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="81532-149">ALIASES</span></span>

## <span data-ttu-id="81532-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81532-150">RELATED LINKS</span></span>

