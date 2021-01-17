---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430194"
---
# <span data-ttu-id="0fe9c-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0fe9c-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="0fe9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fe9c-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe9c-103">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-103">Create a gallery image version.</span></span>

## <span data-ttu-id="0fe9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fe9c-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0fe9c-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe9c-106">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-106">Create a gallery image version.</span></span>

## <span data-ttu-id="0fe9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fe9c-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe9c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0fe9c-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="0fe9c-109">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-109">Create a gallery image version.</span></span>

### <span data-ttu-id="0fe9c-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0fe9c-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="0fe9c-111">Criar uma versão de imagem de galeria com criptografia de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="0fe9c-112">OS</span><span class="sxs-lookup"><span data-stu-id="0fe9c-112">PARAMETERS</span></span>

### <span data-ttu-id="0fe9c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fe9c-113">-AsJob</span></span>
<span data-ttu-id="0fe9c-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0fe9c-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="0fe9c-115">-DataDiskImage</span></span>
<span data-ttu-id="0fe9c-116">Imagens de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-116">Data disk images.</span></span>   <span data-ttu-id="0fe9c-117">por exemplo, @ {Source = @ {ID =<source_id>}; LUN = 1; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="0fe9c-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe9c-118">-DefaultProfile</span></span>
<span data-ttu-id="0fe9c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe9c-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0fe9c-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="0fe9c-121">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-122">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="0fe9c-122">-GalleryName</span></span>
<span data-ttu-id="0fe9c-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-124">-Local</span><span class="sxs-lookup"><span data-stu-id="0fe9c-124">-Location</span></span>
<span data-ttu-id="0fe9c-125">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="0fe9c-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fe9c-126">-Name</span></span>
<span data-ttu-id="0fe9c-127">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="0fe9c-128">-OSDiskImage</span></span>
<span data-ttu-id="0fe9c-129">Imagem de disco do sistema operacional, por exemplo, @ {Source = @ {ID =<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="0fe9c-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="0fe9c-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="0fe9c-131">A data de fim da vida útil da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-131">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="0fe9c-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="0fe9c-133">Se estiver definido, as máquinas virtuais implantadas da versão mais recente da definição da imagem não usarão essa versão da imagem.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0fe9c-134">-ReplicaCount</span></span>
<span data-ttu-id="0fe9c-135">O número de réplicas da versão da imagem a serem criadas por região.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-135">The number of replicas of the Image Version to be created per region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe9c-136">-ResourceGroupName</span></span>
<span data-ttu-id="0fe9c-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="0fe9c-138">-SourceImageId</span></span>
<span data-ttu-id="0fe9c-139">A ID da imagem de origem a partir da qual a versão da imagem será criada.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-139">The ID of the source image from which the Image Version is going to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0fe9c-140">-StorageAccountType</span></span>
<span data-ttu-id="0fe9c-141">Especifica o tipo de conta de armazenamento a ser usado para armazenar a imagem.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="0fe9c-142">Esta propriedade não é atualizável.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-142">This property is not updatable.</span></span> <span data-ttu-id="0fe9c-143">Os valores disponíveis são Standard_LRS, Standard_ZRS e Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="0fe9c-144">-Tag</span></span>
<span data-ttu-id="0fe9c-145">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="0fe9c-145">Resource tags</span></span>

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

### <span data-ttu-id="0fe9c-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="0fe9c-146">-TargetRegion</span></span>
<span data-ttu-id="0fe9c-147">As regiões de destino em que a versão de imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-147">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe9c-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0fe9c-148">-Confirm</span></span>
<span data-ttu-id="0fe9c-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe9c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe9c-150">-WhatIf</span></span>
<span data-ttu-id="0fe9c-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe9c-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe9c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe9c-153">CommonParameters</span></span>
<span data-ttu-id="0fe9c-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe9c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe9c-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fe9c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe9c-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0fe9c-156">INPUTS</span></span>

### <span data-ttu-id="0fe9c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="0fe9c-157">System.String</span></span>

### <span data-ttu-id="0fe9c-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0fe9c-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0fe9c-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0fe9c-159">System.Int32</span></span>

### <span data-ttu-id="0fe9c-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0fe9c-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0fe9c-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0fe9c-161">System.DateTime</span></span>

### <span data-ttu-id="0fe9c-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="0fe9c-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="0fe9c-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0fe9c-163">OUTPUTS</span></span>

### <span data-ttu-id="0fe9c-164">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0fe9c-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="0fe9c-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0fe9c-165">NOTES</span></span>

## <span data-ttu-id="0fe9c-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fe9c-166">RELATED LINKS</span></span>
