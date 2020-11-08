---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113371"
---
# <span data-ttu-id="1377e-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="1377e-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="1377e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1377e-102">SYNOPSIS</span></span>
<span data-ttu-id="1377e-103">Descreve uma fonte de imagem de máquina virtual para criar, personalizar e distribuir.</span><span class="sxs-lookup"><span data-stu-id="1377e-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="1377e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1377e-104">SYNTAX</span></span>

### <span data-ttu-id="1377e-105">ManagedImage (padrão)</span><span class="sxs-lookup"><span data-stu-id="1377e-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="1377e-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="1377e-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="1377e-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="1377e-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1377e-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="1377e-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="1377e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1377e-109">DESCRIPTION</span></span>
<span data-ttu-id="1377e-110">Descreve uma fonte de imagem de máquina virtual para criar, personalizar e distribuir.</span><span class="sxs-lookup"><span data-stu-id="1377e-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="1377e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1377e-111">EXAMPLES</span></span>

### <span data-ttu-id="1377e-112">Exemplo 1: criar uma fonte de imagem gerenciada</span><span class="sxs-lookup"><span data-stu-id="1377e-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="1377e-113">Esse comando cria uma fonte de imagem gerenciada.</span><span class="sxs-lookup"><span data-stu-id="1377e-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="1377e-114">Exemplo 2: criar uma fonte de imagem compartilhada</span><span class="sxs-lookup"><span data-stu-id="1377e-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="1377e-115">Esse comando cria uma fonte de imagem compartilhada.</span><span class="sxs-lookup"><span data-stu-id="1377e-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="1377e-116">Exemplo 3: criar uma fonte de imagem do platfrom</span><span class="sxs-lookup"><span data-stu-id="1377e-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="1377e-117">Esse comando cria uma fonte de imagem platfrom.</span><span class="sxs-lookup"><span data-stu-id="1377e-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="1377e-118">OS</span><span class="sxs-lookup"><span data-stu-id="1377e-118">PARAMETERS</span></span>

### <span data-ttu-id="1377e-119">-Imageid</span><span class="sxs-lookup"><span data-stu-id="1377e-119">-ImageId</span></span>
<span data-ttu-id="1377e-120">ID do recurso ARM da imagem gerenciada na assinatura do cliente.</span><span class="sxs-lookup"><span data-stu-id="1377e-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="1377e-121">-ImageVersionId</span></span>
<span data-ttu-id="1377e-122">ID do recurso ARM da versão da imagem na Galeria de imagens compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="1377e-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-123">-Oferta</span><span class="sxs-lookup"><span data-stu-id="1377e-123">-Offer</span></span>
<span data-ttu-id="1377e-124">Oferta de imagem das [imagens da galeria do Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="1377e-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="1377e-125">-PlanName</span></span>
<span data-ttu-id="1377e-126">Nome do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="1377e-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="1377e-127">-PlanProduct</span></span>
<span data-ttu-id="1377e-128">Produto do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="1377e-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="1377e-129">-PlanPublisher</span></span>
<span data-ttu-id="1377e-130">Fornecedor do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="1377e-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1377e-131">-Publisher</span></span>
<span data-ttu-id="1377e-132">Publicador de imagens em [imagens do Azure Gallery](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="1377e-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="1377e-133">-Sku</span></span>
<span data-ttu-id="1377e-134">SKU da imagem a partir das [imagens da galeria do Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="1377e-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="1377e-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="1377e-136">Descreve uma fonte de imagem que é uma imagem gerenciada na assinatura do cliente.</span><span class="sxs-lookup"><span data-stu-id="1377e-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="1377e-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="1377e-138">Descreve uma fonte de imagem de [imagens da galeria do Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="1377e-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="1377e-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="1377e-140">Descreve uma fonte de imagem que é uma versão de imagem em uma galeria de imagens compartilhada.</span><span class="sxs-lookup"><span data-stu-id="1377e-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-141">-Versão</span><span class="sxs-lookup"><span data-stu-id="1377e-141">-Version</span></span>
<span data-ttu-id="1377e-142">Versão de imagem das [imagens da galeria do Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="1377e-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1377e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1377e-143">CommonParameters</span></span>
<span data-ttu-id="1377e-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1377e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1377e-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1377e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1377e-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1377e-146">INPUTS</span></span>

## <span data-ttu-id="1377e-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1377e-147">OUTPUTS</span></span>

### <span data-ttu-id="1377e-148">Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="1377e-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="1377e-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1377e-149">NOTES</span></span>

<span data-ttu-id="1377e-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1377e-150">ALIASES</span></span>

## <span data-ttu-id="1377e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1377e-151">RELATED LINKS</span></span>

