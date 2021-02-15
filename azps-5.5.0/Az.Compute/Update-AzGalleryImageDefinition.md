---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115461"
---
# <span data-ttu-id="6600b-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="6600b-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="6600b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6600b-102">SYNOPSIS</span></span>
<span data-ttu-id="6600b-103">Atualizar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="6600b-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="6600b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6600b-104">SYNTAX</span></span>

### <span data-ttu-id="6600b-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6600b-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6600b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6600b-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6600b-107">Objectparameter</span><span class="sxs-lookup"><span data-stu-id="6600b-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6600b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6600b-108">DESCRIPTION</span></span>
<span data-ttu-id="6600b-109">Atualizar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="6600b-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="6600b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6600b-110">EXAMPLES</span></span>

### <span data-ttu-id="6600b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6600b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="6600b-112">Atualizar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="6600b-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="6600b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6600b-113">PARAMETERS</span></span>

### <span data-ttu-id="6600b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6600b-114">-AsJob</span></span>
<span data-ttu-id="6600b-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6600b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6600b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6600b-116">-DefaultProfile</span></span>
<span data-ttu-id="6600b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6600b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6600b-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6600b-118">-Description</span></span>
<span data-ttu-id="6600b-119">A descrição do recurso Definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="6600b-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="6600b-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="6600b-120">-DisallowedDiskType</span></span>
<span data-ttu-id="6600b-121">Os tipos de disco não permitidos.</span><span class="sxs-lookup"><span data-stu-id="6600b-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="6600b-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="6600b-122">-EndOfLifeDate</span></span>
<span data-ttu-id="6600b-123">A data de fim da vida útil da Galeria de Definição de Imagens</span><span class="sxs-lookup"><span data-stu-id="6600b-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="6600b-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="6600b-124">-Eula</span></span>
<span data-ttu-id="6600b-125">O contrato Eula para a Definição de Imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="6600b-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="6600b-126">-Nomeda Gallery</span><span class="sxs-lookup"><span data-stu-id="6600b-126">-GalleryName</span></span>
<span data-ttu-id="6600b-127">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="6600b-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="6600b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6600b-128">-InputObject</span></span>
<span data-ttu-id="6600b-129">O objeto de definição de imagem da Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="6600b-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="6600b-130">-MáximoMemory</span><span class="sxs-lookup"><span data-stu-id="6600b-130">-MaximumMemory</span></span>
<span data-ttu-id="6600b-131">O máximo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="6600b-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="6600b-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="6600b-132">-MaximumVCPU</span></span>
<span data-ttu-id="6600b-133">O máximo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="6600b-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="6600b-134">-MínimoMemory</span><span class="sxs-lookup"><span data-stu-id="6600b-134">-MinimumMemory</span></span>
<span data-ttu-id="6600b-135">O mínimo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="6600b-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="6600b-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="6600b-136">-MinimumVCPU</span></span>
<span data-ttu-id="6600b-137">O mínimo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="6600b-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="6600b-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="6600b-138">-Name</span></span>
<span data-ttu-id="6600b-139">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="6600b-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="6600b-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="6600b-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="6600b-141">A política de privacidade uri.</span><span class="sxs-lookup"><span data-stu-id="6600b-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="6600b-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="6600b-142">-PurchasePlanName</span></span>
<span data-ttu-id="6600b-143">A ID do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="6600b-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6600b-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="6600b-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="6600b-145">A ID do produto para o plano de compra.</span><span class="sxs-lookup"><span data-stu-id="6600b-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6600b-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6600b-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="6600b-147">A ID do editor do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="6600b-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6600b-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="6600b-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="6600b-149">A nota de lançamento uri.</span><span class="sxs-lookup"><span data-stu-id="6600b-149">The release note uri.</span></span>

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

### <span data-ttu-id="6600b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6600b-150">-ResourceGroupName</span></span>
<span data-ttu-id="6600b-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6600b-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="6600b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6600b-152">-ResourceId</span></span>
<span data-ttu-id="6600b-153">A ID do recurso para a definição de imagem</span><span class="sxs-lookup"><span data-stu-id="6600b-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="6600b-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="6600b-154">-Tag</span></span>
<span data-ttu-id="6600b-155">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="6600b-155">Resource tags</span></span>

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

### <span data-ttu-id="6600b-156">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6600b-156">-Confirm</span></span>
<span data-ttu-id="6600b-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6600b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6600b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6600b-158">-WhatIf</span></span>
<span data-ttu-id="6600b-159">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6600b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6600b-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6600b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6600b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6600b-161">CommonParameters</span></span>
<span data-ttu-id="6600b-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6600b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6600b-163">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6600b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6600b-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="6600b-164">INPUTS</span></span>

### <span data-ttu-id="6600b-165">System.String</span><span class="sxs-lookup"><span data-stu-id="6600b-165">System.String</span></span>

### <span data-ttu-id="6600b-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="6600b-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="6600b-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="6600b-167">System.DateTime</span></span>

### <span data-ttu-id="6600b-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6600b-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6600b-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6600b-169">System.Int32</span></span>

### <span data-ttu-id="6600b-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6600b-170">System.String[]</span></span>

## <span data-ttu-id="6600b-171">Saídas</span><span class="sxs-lookup"><span data-stu-id="6600b-171">OUTPUTS</span></span>

### <span data-ttu-id="6600b-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="6600b-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="6600b-173">Notas</span><span class="sxs-lookup"><span data-stu-id="6600b-173">NOTES</span></span>

## <span data-ttu-id="6600b-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6600b-174">RELATED LINKS</span></span>
