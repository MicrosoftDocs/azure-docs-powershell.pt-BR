---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 09871f6d7876b5f197af515f531c85b8bf6a3d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887894"
---
# <span data-ttu-id="14a15-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="14a15-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="14a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14a15-102">SYNOPSIS</span></span>
<span data-ttu-id="14a15-103">Atualize uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="14a15-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="14a15-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14a15-104">SYNTAX</span></span>

### <span data-ttu-id="14a15-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="14a15-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a15-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="14a15-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14a15-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="14a15-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14a15-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14a15-108">DESCRIPTION</span></span>
<span data-ttu-id="14a15-109">Atualize uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="14a15-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="14a15-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14a15-110">EXAMPLES</span></span>

### <span data-ttu-id="14a15-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14a15-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="14a15-112">Atualize uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="14a15-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="14a15-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14a15-113">PARAMETERS</span></span>

### <span data-ttu-id="14a15-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14a15-114">-AsJob</span></span>
<span data-ttu-id="14a15-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="14a15-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14a15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a15-116">-DefaultProfile</span></span>
<span data-ttu-id="14a15-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14a15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a15-118">-Description</span><span class="sxs-lookup"><span data-stu-id="14a15-118">-Description</span></span>
<span data-ttu-id="14a15-119">A descrição do recurso definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="14a15-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="14a15-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="14a15-120">-DisallowedDiskType</span></span>
<span data-ttu-id="14a15-121">Os tipos de disco não permitidos.</span><span class="sxs-lookup"><span data-stu-id="14a15-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="14a15-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="14a15-122">-EndOfLifeDate</span></span>
<span data-ttu-id="14a15-123">A data de término da vida útil da definição de imagem da galeria</span><span class="sxs-lookup"><span data-stu-id="14a15-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="14a15-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="14a15-124">-Eula</span></span>
<span data-ttu-id="14a15-125">O contrato Eula para a Definição de Imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="14a15-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="14a15-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="14a15-126">-GalleryName</span></span>
<span data-ttu-id="14a15-127">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="14a15-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="14a15-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a15-128">-InputObject</span></span>
<span data-ttu-id="14a15-129">O objeto de definição de imagem da Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="14a15-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="14a15-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="14a15-130">-MaximumMemory</span></span>
<span data-ttu-id="14a15-131">O máximo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="14a15-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="14a15-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="14a15-132">-MaximumVCPU</span></span>
<span data-ttu-id="14a15-133">O máximo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="14a15-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="14a15-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="14a15-134">-MinimumMemory</span></span>
<span data-ttu-id="14a15-135">O mínimo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="14a15-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="14a15-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="14a15-136">-MinimumVCPU</span></span>
<span data-ttu-id="14a15-137">O mínimo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="14a15-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="14a15-138">-Name</span><span class="sxs-lookup"><span data-stu-id="14a15-138">-Name</span></span>
<span data-ttu-id="14a15-139">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="14a15-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="14a15-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="14a15-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="14a15-141">O uri da instrução de privacidade.</span><span class="sxs-lookup"><span data-stu-id="14a15-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="14a15-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="14a15-142">-PurchasePlanName</span></span>
<span data-ttu-id="14a15-143">A ID do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="14a15-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="14a15-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="14a15-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="14a15-145">A ID do produto para o plano de compra.</span><span class="sxs-lookup"><span data-stu-id="14a15-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="14a15-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="14a15-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="14a15-147">A ID do editor do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="14a15-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="14a15-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="14a15-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="14a15-149">O uri da nota de lançamento.</span><span class="sxs-lookup"><span data-stu-id="14a15-149">The release note uri.</span></span>

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

### <span data-ttu-id="14a15-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a15-150">-ResourceGroupName</span></span>
<span data-ttu-id="14a15-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14a15-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="14a15-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14a15-152">-ResourceId</span></span>
<span data-ttu-id="14a15-153">A ID do recurso para a definição de imagem</span><span class="sxs-lookup"><span data-stu-id="14a15-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="14a15-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="14a15-154">-Tag</span></span>
<span data-ttu-id="14a15-155">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="14a15-155">Resource tags</span></span>

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

### <span data-ttu-id="14a15-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14a15-156">-Confirm</span></span>
<span data-ttu-id="14a15-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14a15-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a15-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a15-158">-WhatIf</span></span>
<span data-ttu-id="14a15-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14a15-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a15-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14a15-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a15-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a15-161">CommonParameters</span></span>
<span data-ttu-id="14a15-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a15-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a15-163">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14a15-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a15-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14a15-164">INPUTS</span></span>

### <span data-ttu-id="14a15-165">System.String</span><span class="sxs-lookup"><span data-stu-id="14a15-165">System.String</span></span>

### <span data-ttu-id="14a15-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="14a15-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="14a15-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="14a15-167">System.DateTime</span></span>

### <span data-ttu-id="14a15-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="14a15-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="14a15-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="14a15-169">System.Int32</span></span>

### <span data-ttu-id="14a15-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="14a15-170">System.String[]</span></span>

## <span data-ttu-id="14a15-171">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14a15-171">OUTPUTS</span></span>

### <span data-ttu-id="14a15-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="14a15-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="14a15-173">NOTES</span><span class="sxs-lookup"><span data-stu-id="14a15-173">NOTES</span></span>

## <span data-ttu-id="14a15-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14a15-174">RELATED LINKS</span></span>
