---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262199"
---
# <span data-ttu-id="e95e0-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e95e0-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="e95e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e95e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e95e0-103">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="e95e0-103">Create a gallery image version.</span></span>

## <span data-ttu-id="e95e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e95e0-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95e0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e95e0-105">DESCRIPTION</span></span>
<span data-ttu-id="e95e0-106">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="e95e0-106">Create a gallery image version.</span></span>

## <span data-ttu-id="e95e0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e95e0-107">EXAMPLES</span></span>

### <span data-ttu-id="e95e0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e95e0-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="e95e0-109">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="e95e0-109">Create a gallery image version.</span></span>

### <span data-ttu-id="e95e0-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e95e0-110">Example 2</span></span>
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

<span data-ttu-id="e95e0-111">Criar uma versão de imagem de galeria com criptografia de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="e95e0-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="e95e0-112">OS</span><span class="sxs-lookup"><span data-stu-id="e95e0-112">PARAMETERS</span></span>

### <span data-ttu-id="e95e0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e95e0-113">-AsJob</span></span>
<span data-ttu-id="e95e0-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e95e0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e95e0-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="e95e0-115">-DataDiskImage</span></span>
<span data-ttu-id="e95e0-116">Imagens de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="e95e0-116">Data disk images.</span></span>   <span data-ttu-id="e95e0-117">por exemplo, @ {Source = @ {ID =<source_id>}; LUN = 1; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="e95e0-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="e95e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95e0-118">-DefaultProfile</span></span>
<span data-ttu-id="e95e0-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e95e0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95e0-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e95e0-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="e95e0-121">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="e95e0-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="e95e0-122">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="e95e0-122">-GalleryName</span></span>
<span data-ttu-id="e95e0-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="e95e0-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="e95e0-124">-Local</span><span class="sxs-lookup"><span data-stu-id="e95e0-124">-Location</span></span>
<span data-ttu-id="e95e0-125">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="e95e0-125">Resource location</span></span>

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

### <span data-ttu-id="e95e0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e95e0-126">-Name</span></span>
<span data-ttu-id="e95e0-127">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="e95e0-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="e95e0-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="e95e0-128">-OSDiskImage</span></span>
<span data-ttu-id="e95e0-129">Imagem de disco do sistema operacional, por exemplo, @ {Source = @ {ID =<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="e95e0-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="e95e0-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="e95e0-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="e95e0-131">A data de fim da vida útil da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="e95e0-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="e95e0-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="e95e0-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="e95e0-133">Se estiver definido, as máquinas virtuais implantadas da versão mais recente da definição da imagem não usarão essa versão da imagem.</span><span class="sxs-lookup"><span data-stu-id="e95e0-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="e95e0-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="e95e0-134">-ReplicaCount</span></span>
<span data-ttu-id="e95e0-135">O número de réplicas da versão da imagem a serem criadas por região.</span><span class="sxs-lookup"><span data-stu-id="e95e0-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="e95e0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95e0-136">-ResourceGroupName</span></span>
<span data-ttu-id="e95e0-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e95e0-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="e95e0-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="e95e0-138">-SourceImageId</span></span>
<span data-ttu-id="e95e0-139">A ID da imagem de origem a partir da qual a versão da imagem será criada.</span><span class="sxs-lookup"><span data-stu-id="e95e0-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="e95e0-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e95e0-140">-StorageAccountType</span></span>
<span data-ttu-id="e95e0-141">Especifica o tipo de conta de armazenamento a ser usado para armazenar a imagem.</span><span class="sxs-lookup"><span data-stu-id="e95e0-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="e95e0-142">Esta propriedade não é atualizável.</span><span class="sxs-lookup"><span data-stu-id="e95e0-142">This property is not updatable.</span></span> <span data-ttu-id="e95e0-143">Os valores disponíveis são Standard_LRS, Standard_ZRS e Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="e95e0-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="e95e0-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="e95e0-144">-Tag</span></span>
<span data-ttu-id="e95e0-145">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="e95e0-145">Resource tags</span></span>

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

### <span data-ttu-id="e95e0-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="e95e0-146">-TargetRegion</span></span>
<span data-ttu-id="e95e0-147">As regiões de destino em que a versão de imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="e95e0-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="e95e0-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e95e0-148">-Confirm</span></span>
<span data-ttu-id="e95e0-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95e0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95e0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95e0-150">-WhatIf</span></span>
<span data-ttu-id="e95e0-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e95e0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95e0-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e95e0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95e0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95e0-153">CommonParameters</span></span>
<span data-ttu-id="e95e0-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95e0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95e0-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e95e0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95e0-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e95e0-156">INPUTS</span></span>

### <span data-ttu-id="e95e0-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e95e0-157">System.String</span></span>

### <span data-ttu-id="e95e0-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e95e0-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e95e0-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e95e0-159">System.Int32</span></span>

### <span data-ttu-id="e95e0-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e95e0-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e95e0-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e95e0-161">System.DateTime</span></span>

### <span data-ttu-id="e95e0-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="e95e0-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="e95e0-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e95e0-163">OUTPUTS</span></span>

### <span data-ttu-id="e95e0-164">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e95e0-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="e95e0-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e95e0-165">NOTES</span></span>

## <span data-ttu-id="e95e0-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e95e0-166">RELATED LINKS</span></span>
