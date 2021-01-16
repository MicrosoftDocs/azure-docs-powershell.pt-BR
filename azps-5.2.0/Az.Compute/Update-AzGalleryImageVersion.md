---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259331"
---
# <span data-ttu-id="bec94-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bec94-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="bec94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bec94-102">SYNOPSIS</span></span>
<span data-ttu-id="bec94-103">Atualize uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec94-103">Update a gallery image version.</span></span>

## <span data-ttu-id="bec94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bec94-104">SYNTAX</span></span>

### <span data-ttu-id="bec94-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="bec94-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec94-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="bec94-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec94-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="bec94-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec94-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bec94-108">DESCRIPTION</span></span>
<span data-ttu-id="bec94-109">Atualize uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec94-109">Update a gallery image version.</span></span>

## <span data-ttu-id="bec94-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bec94-110">EXAMPLES</span></span>

### <span data-ttu-id="bec94-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bec94-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="bec94-112">Atualize uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec94-112">Update a gallery image version.</span></span>

## <span data-ttu-id="bec94-113">OS</span><span class="sxs-lookup"><span data-stu-id="bec94-113">PARAMETERS</span></span>

### <span data-ttu-id="bec94-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bec94-114">-AsJob</span></span>
<span data-ttu-id="bec94-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bec94-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bec94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec94-116">-DefaultProfile</span></span>
<span data-ttu-id="bec94-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bec94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec94-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="bec94-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="bec94-119">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec94-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="bec94-120">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="bec94-120">-GalleryName</span></span>
<span data-ttu-id="bec94-121">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec94-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="bec94-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bec94-122">-InputObject</span></span>
<span data-ttu-id="bec94-123">O objeto da versão da imagem da Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="bec94-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="bec94-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="bec94-124">-Name</span></span>
<span data-ttu-id="bec94-125">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec94-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="bec94-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="bec94-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="bec94-127">A data de fim da vida útil da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec94-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="bec94-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="bec94-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="bec94-129">Se estiver definido, as máquinas virtuais implantadas da versão mais recente da definição da imagem não usarão essa versão da imagem.</span><span class="sxs-lookup"><span data-stu-id="bec94-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="bec94-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="bec94-130">-ReplicaCount</span></span>
<span data-ttu-id="bec94-131">O número de réplicas da versão da imagem a serem criadas por região.</span><span class="sxs-lookup"><span data-stu-id="bec94-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="bec94-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec94-132">-ResourceGroupName</span></span>
<span data-ttu-id="bec94-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bec94-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="bec94-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bec94-134">-ResourceId</span></span>
<span data-ttu-id="bec94-135">A ID do recurso da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec94-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="bec94-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="bec94-136">-Tag</span></span>
<span data-ttu-id="bec94-137">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="bec94-137">Resource tags</span></span>

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

### <span data-ttu-id="bec94-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="bec94-138">-TargetRegion</span></span>
<span data-ttu-id="bec94-139">As regiões de destino em que a versão de imagem será replicada.</span><span class="sxs-lookup"><span data-stu-id="bec94-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="bec94-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bec94-140">-Confirm</span></span>
<span data-ttu-id="bec94-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bec94-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec94-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec94-142">-WhatIf</span></span>
<span data-ttu-id="bec94-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bec94-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec94-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bec94-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec94-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec94-145">CommonParameters</span></span>
<span data-ttu-id="bec94-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec94-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec94-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bec94-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec94-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bec94-148">INPUTS</span></span>

### <span data-ttu-id="bec94-149">System. String</span><span class="sxs-lookup"><span data-stu-id="bec94-149">System.String</span></span>

### <span data-ttu-id="bec94-150">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bec94-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="bec94-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bec94-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bec94-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bec94-152">System.Int32</span></span>

### <span data-ttu-id="bec94-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bec94-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bec94-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bec94-154">System.DateTime</span></span>

### <span data-ttu-id="bec94-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="bec94-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="bec94-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bec94-156">OUTPUTS</span></span>

### <span data-ttu-id="bec94-157">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bec94-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="bec94-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bec94-158">NOTES</span></span>

## <span data-ttu-id="bec94-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bec94-159">RELATED LINKS</span></span>
