---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: a106435739d7e4ec358038be476cc3f2ba8cd09d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893282"
---
# <span data-ttu-id="487d9-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="487d9-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="487d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="487d9-102">SYNOPSIS</span></span>
<span data-ttu-id="487d9-103">Descreve uma fonte de imagem de máquina virtual para criação, personalização e distribuição.</span><span class="sxs-lookup"><span data-stu-id="487d9-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="487d9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="487d9-104">SYNTAX</span></span>

### <span data-ttu-id="487d9-105">ManagedImage (Padrão)</span><span class="sxs-lookup"><span data-stu-id="487d9-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="487d9-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="487d9-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="487d9-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="487d9-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="487d9-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="487d9-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="487d9-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="487d9-109">DESCRIPTION</span></span>
<span data-ttu-id="487d9-110">Descreve uma fonte de imagem de máquina virtual para criação, personalização e distribuição.</span><span class="sxs-lookup"><span data-stu-id="487d9-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="487d9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="487d9-111">EXAMPLES</span></span>

### <span data-ttu-id="487d9-112">Exemplo 1: Criar uma fonte de imagem gerenciada</span><span class="sxs-lookup"><span data-stu-id="487d9-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="487d9-113">Este comando cria uma fonte de imagem gerenciada.</span><span class="sxs-lookup"><span data-stu-id="487d9-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="487d9-114">Exemplo 2: Criar uma fonte de imagem compartilhada</span><span class="sxs-lookup"><span data-stu-id="487d9-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="487d9-115">Este comando cria uma fonte de imagem compartilhada.</span><span class="sxs-lookup"><span data-stu-id="487d9-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="487d9-116">Exemplo 3: Criar uma fonte de imagem platfrom</span><span class="sxs-lookup"><span data-stu-id="487d9-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="487d9-117">Este comando cria uma fonte de imagem platfrom.</span><span class="sxs-lookup"><span data-stu-id="487d9-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="487d9-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="487d9-118">PARAMETERS</span></span>

### <span data-ttu-id="487d9-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="487d9-119">-ImageId</span></span>
<span data-ttu-id="487d9-120">ARM id de recurso da imagem gerenciada na assinatura do cliente.</span><span class="sxs-lookup"><span data-stu-id="487d9-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="487d9-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="487d9-121">-ImageVersionId</span></span>
<span data-ttu-id="487d9-122">ARM id de recurso da versão da imagem na galeria de imagens compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="487d9-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="487d9-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="487d9-123">-Offer</span></span>
<span data-ttu-id="487d9-124">Oferta de imagem das [Imagens da Galeria do Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="487d9-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="487d9-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="487d9-125">-PlanName</span></span>
<span data-ttu-id="487d9-126">Nome do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="487d9-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="487d9-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="487d9-127">-PlanProduct</span></span>
<span data-ttu-id="487d9-128">Produto do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="487d9-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="487d9-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="487d9-129">-PlanPublisher</span></span>
<span data-ttu-id="487d9-130">Editor do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="487d9-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="487d9-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="487d9-131">-Publisher</span></span>
<span data-ttu-id="487d9-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="487d9-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="487d9-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="487d9-133">-Sku</span></span>
<span data-ttu-id="487d9-134">Sku de imagem das Imagens [da Galeria do Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="487d9-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="487d9-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="487d9-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="487d9-136">Descreve uma fonte de imagem que é uma imagem gerenciada na assinatura do cliente.</span><span class="sxs-lookup"><span data-stu-id="487d9-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="487d9-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="487d9-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="487d9-138">Descreve uma fonte de imagem de [Imagens da Galeria do Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="487d9-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="487d9-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="487d9-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="487d9-140">Descreve uma fonte de imagem que é uma versão de imagem em uma galeria de imagens compartilhada.</span><span class="sxs-lookup"><span data-stu-id="487d9-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="487d9-141">-Version</span><span class="sxs-lookup"><span data-stu-id="487d9-141">-Version</span></span>
<span data-ttu-id="487d9-142">Versão da imagem das [Imagens da Galeria do Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="487d9-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="487d9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="487d9-143">CommonParameters</span></span>
<span data-ttu-id="487d9-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="487d9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="487d9-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="487d9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="487d9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="487d9-146">INPUTS</span></span>

## <span data-ttu-id="487d9-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="487d9-147">OUTPUTS</span></span>

### <span data-ttu-id="487d9-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="487d9-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="487d9-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="487d9-149">NOTES</span></span>

<span data-ttu-id="487d9-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="487d9-150">ALIASES</span></span>

## <span data-ttu-id="487d9-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="487d9-151">RELATED LINKS</span></span>

