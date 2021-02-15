---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113800"
---
# <span data-ttu-id="7183f-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="7183f-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="7183f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7183f-102">SYNOPSIS</span></span>
<span data-ttu-id="7183f-103">Objeto de distribuição genérico</span><span class="sxs-lookup"><span data-stu-id="7183f-103">Generic distribution object</span></span>

## <span data-ttu-id="7183f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7183f-104">SYNTAX</span></span>

### <span data-ttu-id="7183f-105">ManagedImageDistributor (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7183f-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="7183f-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="7183f-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="7183f-107">Redistribuição de dados</span><span class="sxs-lookup"><span data-stu-id="7183f-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="7183f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7183f-108">DESCRIPTION</span></span>
<span data-ttu-id="7183f-109">Objeto de distribuição genérico</span><span class="sxs-lookup"><span data-stu-id="7183f-109">Generic distribution object</span></span>

## <span data-ttu-id="7183f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7183f-110">EXAMPLES</span></span>

### <span data-ttu-id="7183f-111">Exemplo 1: Criar um distribuidor de imagem gerenciado</span><span class="sxs-lookup"><span data-stu-id="7183f-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="7183f-112">Esse comando cria um distribuidor de imagens gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7183f-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="7183f-113">Exemplo 2: Criar um distribuidor DAD.</span><span class="sxs-lookup"><span data-stu-id="7183f-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="7183f-114">Esse comando cria um distribuidor PELAD.</span><span class="sxs-lookup"><span data-stu-id="7183f-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="7183f-115">Exemplo 3: Criar um distribuidor de imagens compartilhadas</span><span class="sxs-lookup"><span data-stu-id="7183f-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="7183f-116">Esse comando cria um distribuidor de imagem compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7183f-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="7183f-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7183f-117">PARAMETERS</span></span>

### <span data-ttu-id="7183f-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="7183f-118">-ArtifactTag</span></span>
<span data-ttu-id="7183f-119">Marcas que serão aplicadas ao artefato depois que ele tiver sido criado/atualizado pelo distribuidor.</span><span class="sxs-lookup"><span data-stu-id="7183f-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="7183f-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="7183f-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="7183f-121">Sinalizador que indica se a versão da imagem criada deve ser excluída da versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="7183f-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="7183f-122">Omitir para usar o padrão (falso).</span><span class="sxs-lookup"><span data-stu-id="7183f-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="7183f-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="7183f-123">-GalleryImageId</span></span>
<span data-ttu-id="7183f-124">ID do Recurso da imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="7183f-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="7183f-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="7183f-125">-ImageId</span></span>
<span data-ttu-id="7183f-126">ID do Recurso da Imagem de Disco Gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7183f-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="7183f-127">-Local</span><span class="sxs-lookup"><span data-stu-id="7183f-127">-Location</span></span>
<span data-ttu-id="7183f-128">O local do Azure para a imagem deve corresponder se a imagem já existir.</span><span class="sxs-lookup"><span data-stu-id="7183f-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="7183f-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="7183f-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="7183f-130">Distribuir como uma Imagem de Disco Gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7183f-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="7183f-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="7183f-131">-ReplicationRegion</span></span>
<span data-ttu-id="7183f-132">Uma lista de regiões para as que a imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="7183f-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="7183f-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="7183f-133">-RunOutputName</span></span>
<span data-ttu-id="7183f-134">O nome a ser usado para o RunOutput associado.</span><span class="sxs-lookup"><span data-stu-id="7183f-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="7183f-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="7183f-135">-SharedImageDistributor</span></span>
<span data-ttu-id="7183f-136">Distribuir por meio da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="7183f-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="7183f-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7183f-137">-StorageAccountType</span></span>
<span data-ttu-id="7183f-138">Tipo de conta de armazenamento a ser usado para armazenar a imagem compartilhada.</span><span class="sxs-lookup"><span data-stu-id="7183f-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="7183f-139">Omitir para usar o padrão (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="7183f-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="7183f-140">-Redistribuição Desdados</span><span class="sxs-lookup"><span data-stu-id="7183f-140">-VhdDistributor</span></span>
<span data-ttu-id="7183f-141">Distribua por MEIOD em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7183f-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="7183f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7183f-142">CommonParameters</span></span>
<span data-ttu-id="7183f-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7183f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7183f-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7183f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7183f-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="7183f-145">INPUTS</span></span>

## <span data-ttu-id="7183f-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="7183f-146">OUTPUTS</span></span>

### <span data-ttu-id="7183f-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="7183f-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="7183f-148">Notas</span><span class="sxs-lookup"><span data-stu-id="7183f-148">NOTES</span></span>

<span data-ttu-id="7183f-149">Aliases</span><span class="sxs-lookup"><span data-stu-id="7183f-149">ALIASES</span></span>

## <span data-ttu-id="7183f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7183f-150">RELATED LINKS</span></span>

