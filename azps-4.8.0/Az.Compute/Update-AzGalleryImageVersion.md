---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113068"
---
# <span data-ttu-id="8b2e7-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8b2e7-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="8b2e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2e7-103">Atualize uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-103">Update a gallery image version.</span></span>

## <span data-ttu-id="8b2e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b2e7-104">SYNTAX</span></span>

### <span data-ttu-id="8b2e7-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b2e7-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b2e7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8b2e7-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b2e7-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8b2e7-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b2e7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b2e7-108">DESCRIPTION</span></span>
<span data-ttu-id="8b2e7-109">Atualize uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-109">Update a gallery image version.</span></span>

## <span data-ttu-id="8b2e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b2e7-110">EXAMPLES</span></span>

### <span data-ttu-id="8b2e7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8b2e7-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="8b2e7-112">Atualize uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-112">Update a gallery image version.</span></span>

## <span data-ttu-id="8b2e7-113">OS</span><span class="sxs-lookup"><span data-stu-id="8b2e7-113">PARAMETERS</span></span>

### <span data-ttu-id="8b2e7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b2e7-114">-AsJob</span></span>
<span data-ttu-id="8b2e7-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8b2e7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b2e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2e7-116">-DefaultProfile</span></span>
<span data-ttu-id="8b2e7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b2e7-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8b2e7-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="8b2e7-119">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2e7-120">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="8b2e7-120">-GalleryName</span></span>
<span data-ttu-id="8b2e7-121">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2e7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b2e7-122">-InputObject</span></span>
<span data-ttu-id="8b2e7-123">O objeto da versão da imagem da Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2e7-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b2e7-124">-Name</span></span>
<span data-ttu-id="8b2e7-125">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2e7-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="8b2e7-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="8b2e7-127">A data de fim da vida útil da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="8b2e7-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="8b2e7-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="8b2e7-129">Se estiver definido, as máquinas virtuais implantadas da versão mais recente da definição da imagem não usarão essa versão da imagem.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="8b2e7-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8b2e7-130">-ReplicaCount</span></span>
<span data-ttu-id="8b2e7-131">O número de réplicas da versão da imagem a serem criadas por região.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="8b2e7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2e7-132">-ResourceGroupName</span></span>
<span data-ttu-id="8b2e7-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2e7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b2e7-134">-ResourceId</span></span>
<span data-ttu-id="8b2e7-135">A ID do recurso da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2e7-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="8b2e7-136">-Tag</span></span>
<span data-ttu-id="8b2e7-137">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="8b2e7-137">Resource tags</span></span>

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

### <span data-ttu-id="8b2e7-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="8b2e7-138">-TargetRegion</span></span>
<span data-ttu-id="8b2e7-139">As regiões de destino em que a versão de imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="8b2e7-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b2e7-140">-Confirm</span></span>
<span data-ttu-id="8b2e7-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b2e7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b2e7-142">-WhatIf</span></span>
<span data-ttu-id="8b2e7-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b2e7-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b2e7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2e7-145">CommonParameters</span></span>
<span data-ttu-id="8b2e7-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b2e7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2e7-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b2e7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2e7-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b2e7-148">INPUTS</span></span>

### <span data-ttu-id="8b2e7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8b2e7-149">System.String</span></span>

### <span data-ttu-id="8b2e7-150">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8b2e7-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="8b2e7-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b2e7-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8b2e7-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8b2e7-152">System.Int32</span></span>

### <span data-ttu-id="8b2e7-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8b2e7-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8b2e7-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="8b2e7-154">System.DateTime</span></span>

### <span data-ttu-id="8b2e7-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="8b2e7-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="8b2e7-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b2e7-156">OUTPUTS</span></span>

### <span data-ttu-id="8b2e7-157">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8b2e7-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="8b2e7-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b2e7-158">NOTES</span></span>

## <span data-ttu-id="8b2e7-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b2e7-159">RELATED LINKS</span></span>
