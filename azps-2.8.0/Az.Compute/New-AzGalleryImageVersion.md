---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 80536a8bfce32d713649f3feab4d77b1662206b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597377"
---
# <span data-ttu-id="228f9-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="228f9-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="228f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="228f9-102">SYNOPSIS</span></span>
<span data-ttu-id="228f9-103">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="228f9-103">Create a gallery image version.</span></span>

## <span data-ttu-id="228f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="228f9-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-StorageAccountType <String>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="228f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="228f9-105">DESCRIPTION</span></span>
<span data-ttu-id="228f9-106">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="228f9-106">Create a gallery image version.</span></span>

## <span data-ttu-id="228f9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="228f9-107">EXAMPLES</span></span>

### <span data-ttu-id="228f9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="228f9-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="228f9-109">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="228f9-109">Create a gallery image version.</span></span>

## <span data-ttu-id="228f9-110">OS</span><span class="sxs-lookup"><span data-stu-id="228f9-110">PARAMETERS</span></span>

### <span data-ttu-id="228f9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="228f9-111">-AsJob</span></span>
<span data-ttu-id="228f9-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="228f9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="228f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="228f9-113">-DefaultProfile</span></span>
<span data-ttu-id="228f9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="228f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="228f9-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="228f9-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="228f9-116">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="228f9-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="228f9-117">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="228f9-117">-GalleryName</span></span>
<span data-ttu-id="228f9-118">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="228f9-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="228f9-119">-Local</span><span class="sxs-lookup"><span data-stu-id="228f9-119">-Location</span></span>
<span data-ttu-id="228f9-120">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="228f9-120">Resource location</span></span>

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

### <span data-ttu-id="228f9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="228f9-121">-Name</span></span>
<span data-ttu-id="228f9-122">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="228f9-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="228f9-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="228f9-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="228f9-124">A data de fim da vida útil da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="228f9-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="228f9-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="228f9-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="228f9-126">Se estiver definido, as máquinas virtuais implantadas da versão mais recente da definição da imagem não usarão essa versão da imagem.</span><span class="sxs-lookup"><span data-stu-id="228f9-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="228f9-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="228f9-127">-ReplicaCount</span></span>
<span data-ttu-id="228f9-128">O número de réplicas da versão da imagem a serem criadas por região.</span><span class="sxs-lookup"><span data-stu-id="228f9-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="228f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="228f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="228f9-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="228f9-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="228f9-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="228f9-131">-SourceImageId</span></span>
<span data-ttu-id="228f9-132">A ID da imagem de origem a partir da qual a versão da imagem será criada.</span><span class="sxs-lookup"><span data-stu-id="228f9-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="228f9-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="228f9-133">-StorageAccountType</span></span>
<span data-ttu-id="228f9-134">Especifica o tipo de conta de armazenamento a ser usado para armazenar a imagem.</span><span class="sxs-lookup"><span data-stu-id="228f9-134">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="228f9-135">Esta propriedade não é atualizável.</span><span class="sxs-lookup"><span data-stu-id="228f9-135">This property is not updatable.</span></span> <span data-ttu-id="228f9-136">Os valores disponíveis são Standard_LRS e Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="228f9-136">Available values are Standard_LRS and Standard_ZRS.</span></span>

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

### <span data-ttu-id="228f9-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="228f9-137">-Tag</span></span>
<span data-ttu-id="228f9-138">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="228f9-138">Resource tags</span></span>

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

### <span data-ttu-id="228f9-139">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="228f9-139">-TargetRegion</span></span>
<span data-ttu-id="228f9-140">As regiões de destino em que a versão de imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="228f9-140">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="228f9-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="228f9-141">-Confirm</span></span>
<span data-ttu-id="228f9-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="228f9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="228f9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="228f9-143">-WhatIf</span></span>
<span data-ttu-id="228f9-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="228f9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="228f9-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="228f9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="228f9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228f9-146">CommonParameters</span></span>
<span data-ttu-id="228f9-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="228f9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228f9-148">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="228f9-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228f9-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="228f9-149">INPUTS</span></span>

### <span data-ttu-id="228f9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="228f9-150">System.String</span></span>

### <span data-ttu-id="228f9-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="228f9-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="228f9-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="228f9-152">System.Int32</span></span>

### <span data-ttu-id="228f9-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="228f9-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="228f9-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="228f9-154">System.DateTime</span></span>

### <span data-ttu-id="228f9-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="228f9-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="228f9-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="228f9-156">OUTPUTS</span></span>

### <span data-ttu-id="228f9-157">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="228f9-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="228f9-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="228f9-158">NOTES</span></span>

## <span data-ttu-id="228f9-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="228f9-159">RELATED LINKS</span></span>
