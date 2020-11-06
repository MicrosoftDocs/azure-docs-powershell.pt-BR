---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 6d5731916309baf93552f9b5d71f30943178f11c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601313"
---
# <span data-ttu-id="3c303-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3c303-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="3c303-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c303-102">SYNOPSIS</span></span>
<span data-ttu-id="3c303-103">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="3c303-103">Create a gallery image version.</span></span>

## <span data-ttu-id="3c303-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c303-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c303-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c303-105">DESCRIPTION</span></span>
<span data-ttu-id="3c303-106">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="3c303-106">Create a gallery image version.</span></span>

## <span data-ttu-id="3c303-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c303-107">EXAMPLES</span></span>

### <span data-ttu-id="3c303-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c303-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="3c303-109">Criar uma versão de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="3c303-109">Create a gallery image version.</span></span>

## <span data-ttu-id="3c303-110">OS</span><span class="sxs-lookup"><span data-stu-id="3c303-110">PARAMETERS</span></span>

### <span data-ttu-id="3c303-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c303-111">-AsJob</span></span>
<span data-ttu-id="3c303-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3c303-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c303-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c303-113">-DefaultProfile</span></span>
<span data-ttu-id="3c303-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c303-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c303-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3c303-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="3c303-116">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="3c303-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="3c303-117">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="3c303-117">-GalleryName</span></span>
<span data-ttu-id="3c303-118">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="3c303-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="3c303-119">-Local</span><span class="sxs-lookup"><span data-stu-id="3c303-119">-Location</span></span>
<span data-ttu-id="3c303-120">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="3c303-120">Resource location</span></span>

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

### <span data-ttu-id="3c303-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c303-121">-Name</span></span>
<span data-ttu-id="3c303-122">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="3c303-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="3c303-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="3c303-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="3c303-124">A data de fim da vida útil da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="3c303-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="3c303-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="3c303-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="3c303-126">Se estiver definido, as máquinas virtuais implantadas da versão mais recente da definição da imagem não usarão essa versão da imagem.</span><span class="sxs-lookup"><span data-stu-id="3c303-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="3c303-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3c303-127">-ReplicaCount</span></span>
<span data-ttu-id="3c303-128">O número de réplicas da versão da imagem a serem criadas por região.</span><span class="sxs-lookup"><span data-stu-id="3c303-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="3c303-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c303-129">-ResourceGroupName</span></span>
<span data-ttu-id="3c303-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c303-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c303-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="3c303-131">-SourceImageId</span></span>
<span data-ttu-id="3c303-132">A ID da imagem de origem a partir da qual a versão da imagem será criada.</span><span class="sxs-lookup"><span data-stu-id="3c303-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="3c303-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="3c303-133">-Tag</span></span>
<span data-ttu-id="3c303-134">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="3c303-134">Resource tags</span></span>

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

### <span data-ttu-id="3c303-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="3c303-135">-TargetRegion</span></span>
<span data-ttu-id="3c303-136">As regiões de destino em que a versão de imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="3c303-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="3c303-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c303-137">-Confirm</span></span>
<span data-ttu-id="3c303-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c303-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c303-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c303-139">-WhatIf</span></span>
<span data-ttu-id="3c303-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c303-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c303-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c303-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c303-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c303-142">CommonParameters</span></span>
<span data-ttu-id="3c303-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c303-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c303-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c303-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c303-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c303-145">INPUTS</span></span>

### <span data-ttu-id="3c303-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3c303-146">System.String</span></span>

### <span data-ttu-id="3c303-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3c303-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3c303-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3c303-148">System.Int32</span></span>

### <span data-ttu-id="3c303-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c303-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3c303-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="3c303-150">System.DateTime</span></span>

### <span data-ttu-id="3c303-151">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="3c303-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="3c303-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c303-152">OUTPUTS</span></span>

### <span data-ttu-id="3c303-153">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3c303-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="3c303-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c303-154">NOTES</span></span>

## <span data-ttu-id="3c303-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c303-155">RELATED LINKS</span></span>
