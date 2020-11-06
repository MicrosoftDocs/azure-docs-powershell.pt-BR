---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 445029c41e27cce14bff2ac14d826adf28f3c9ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601981"
---
# <span data-ttu-id="7f10e-101">Update-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="7f10e-101">Update-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="7f10e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f10e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f10e-103">Atualize uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="7f10e-103">Update a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f10e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f10e-104">SYNTAX</span></span>

### <span data-ttu-id="7f10e-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f10e-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f10e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="7f10e-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f10e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="7f10e-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f10e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f10e-108">DESCRIPTION</span></span>
<span data-ttu-id="7f10e-109">Atualize uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="7f10e-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="7f10e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f10e-110">EXAMPLES</span></span>

### <span data-ttu-id="7f10e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7f10e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="7f10e-112">Atualize uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="7f10e-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="7f10e-113">OS</span><span class="sxs-lookup"><span data-stu-id="7f10e-113">PARAMETERS</span></span>

### <span data-ttu-id="7f10e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f10e-114">-AsJob</span></span>
<span data-ttu-id="7f10e-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7f10e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f10e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f10e-116">-DefaultProfile</span></span>
<span data-ttu-id="7f10e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f10e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f10e-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7f10e-118">-Description</span></span>
<span data-ttu-id="7f10e-119">A descrição do recurso de definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="7f10e-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="7f10e-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="7f10e-120">-DisallowedDiskType</span></span>
<span data-ttu-id="7f10e-121">Os tipos de disco não permitidos.</span><span class="sxs-lookup"><span data-stu-id="7f10e-121">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f10e-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="7f10e-122">-EndOfLifeDate</span></span>
<span data-ttu-id="7f10e-123">A data de fim da vida útil da definição de imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="7f10e-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="7f10e-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="7f10e-124">-Eula</span></span>
<span data-ttu-id="7f10e-125">O contrato de EULA para a definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="7f10e-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="7f10e-126">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="7f10e-126">-GalleryName</span></span>
<span data-ttu-id="7f10e-127">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="7f10e-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="7f10e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f10e-128">-InputObject</span></span>
<span data-ttu-id="7f10e-129">O objeto de definição de imagem da Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="7f10e-129">The PS Gallery Image Definition Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f10e-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="7f10e-130">-MaximumMemory</span></span>
<span data-ttu-id="7f10e-131">O máximo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="7f10e-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="7f10e-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="7f10e-132">-MaximumVCPU</span></span>
<span data-ttu-id="7f10e-133">O máximo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="7f10e-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="7f10e-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="7f10e-134">-MinimumMemory</span></span>
<span data-ttu-id="7f10e-135">O mínimo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="7f10e-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="7f10e-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="7f10e-136">-MinimumVCPU</span></span>
<span data-ttu-id="7f10e-137">O mínimo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="7f10e-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="7f10e-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f10e-138">-Name</span></span>
<span data-ttu-id="7f10e-139">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="7f10e-139">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f10e-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="7f10e-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="7f10e-141">O URI da declaração de privacidade.</span><span class="sxs-lookup"><span data-stu-id="7f10e-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="7f10e-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="7f10e-142">-PurchasePlanName</span></span>
<span data-ttu-id="7f10e-143">A ID do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="7f10e-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7f10e-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="7f10e-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="7f10e-145">A ID do produto do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="7f10e-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7f10e-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="7f10e-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="7f10e-147">A ID de fornecedor para o plano de compra.</span><span class="sxs-lookup"><span data-stu-id="7f10e-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7f10e-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="7f10e-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="7f10e-149">O URI da nota de lançamento.</span><span class="sxs-lookup"><span data-stu-id="7f10e-149">The release note uri.</span></span>

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

### <span data-ttu-id="7f10e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f10e-150">-ResourceGroupName</span></span>
<span data-ttu-id="7f10e-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f10e-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f10e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f10e-152">-ResourceId</span></span>
<span data-ttu-id="7f10e-153">A ID do recurso para a definição da imagem</span><span class="sxs-lookup"><span data-stu-id="7f10e-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="7f10e-154">-Marca</span><span class="sxs-lookup"><span data-stu-id="7f10e-154">-Tag</span></span>
<span data-ttu-id="7f10e-155">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="7f10e-155">Resource tags</span></span>

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

### <span data-ttu-id="7f10e-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f10e-156">-Confirm</span></span>
<span data-ttu-id="7f10e-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f10e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f10e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f10e-158">-WhatIf</span></span>
<span data-ttu-id="7f10e-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f10e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f10e-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f10e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f10e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f10e-161">CommonParameters</span></span>
<span data-ttu-id="7f10e-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f10e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f10e-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f10e-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f10e-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f10e-164">INPUTS</span></span>

### <span data-ttu-id="7f10e-165">System. String</span><span class="sxs-lookup"><span data-stu-id="7f10e-165">System.String</span></span>

### <span data-ttu-id="7f10e-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="7f10e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="7f10e-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="7f10e-167">System.DateTime</span></span>

### <span data-ttu-id="7f10e-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7f10e-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7f10e-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7f10e-169">System.Int32</span></span>

### <span data-ttu-id="7f10e-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="7f10e-170">System.String[]</span></span>

## <span data-ttu-id="7f10e-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f10e-171">OUTPUTS</span></span>

### <span data-ttu-id="7f10e-172">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="7f10e-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="7f10e-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f10e-173">NOTES</span></span>

## <span data-ttu-id="7f10e-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f10e-174">RELATED LINKS</span></span>
