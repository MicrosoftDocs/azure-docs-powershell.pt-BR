---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: 7b2a0399be6412c3e33754a8e91b1a6120b5ec9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597382"
---
# <span data-ttu-id="bec4f-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="bec4f-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="bec4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bec4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bec4f-103">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="bec4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bec4f-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>]
 [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>]
 [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec4f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bec4f-105">DESCRIPTION</span></span>
<span data-ttu-id="bec4f-106">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="bec4f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bec4f-107">EXAMPLES</span></span>

### <span data-ttu-id="bec4f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bec4f-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="bec4f-109">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="bec4f-110">OS</span><span class="sxs-lookup"><span data-stu-id="bec4f-110">PARAMETERS</span></span>

### <span data-ttu-id="bec4f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bec4f-111">-AsJob</span></span>
<span data-ttu-id="bec4f-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bec4f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bec4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec4f-113">-DefaultProfile</span></span>
<span data-ttu-id="bec4f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bec4f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec4f-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="bec4f-115">-Description</span></span>
<span data-ttu-id="bec4f-116">A descrição do recurso de definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="bec4f-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="bec4f-117">-DisallowedDiskType</span></span>
<span data-ttu-id="bec4f-118">Os tipos de disco não permitidos.</span><span class="sxs-lookup"><span data-stu-id="bec4f-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="bec4f-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="bec4f-119">-EndOfLifeDate</span></span>
<span data-ttu-id="bec4f-120">A data de fim da vida útil da definição de imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="bec4f-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="bec4f-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="bec4f-121">-Eula</span></span>
<span data-ttu-id="bec4f-122">O contrato de EULA para a definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="bec4f-123">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="bec4f-123">-GalleryName</span></span>
<span data-ttu-id="bec4f-124">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="bec4f-125">-Local</span><span class="sxs-lookup"><span data-stu-id="bec4f-125">-Location</span></span>
<span data-ttu-id="bec4f-126">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="bec4f-126">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec4f-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="bec4f-127">-MaximumMemory</span></span>
<span data-ttu-id="bec4f-128">O máximo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="bec4f-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="bec4f-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="bec4f-129">-MaximumVCPU</span></span>
<span data-ttu-id="bec4f-130">O máximo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="bec4f-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="bec4f-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="bec4f-131">-MinimumMemory</span></span>
<span data-ttu-id="bec4f-132">O mínimo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="bec4f-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="bec4f-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="bec4f-133">-MinimumVCPU</span></span>
<span data-ttu-id="bec4f-134">O mínimo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="bec4f-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="bec4f-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="bec4f-135">-Name</span></span>
<span data-ttu-id="bec4f-136">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-136">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec4f-137">-Oferta</span><span class="sxs-lookup"><span data-stu-id="bec4f-137">-Offer</span></span>
<span data-ttu-id="bec4f-138">O nome da oferta de definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="bec4f-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="bec4f-139">-OsState</span></span>
<span data-ttu-id="bec4f-140">O estado do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="bec4f-140">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec4f-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="bec4f-141">-OsType</span></span>
<span data-ttu-id="bec4f-142">O tipo de sistema operacional</span><span class="sxs-lookup"><span data-stu-id="bec4f-142">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec4f-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="bec4f-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="bec4f-144">O URI da declaração de privacidade.</span><span class="sxs-lookup"><span data-stu-id="bec4f-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="bec4f-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="bec4f-145">-Publisher</span></span>
<span data-ttu-id="bec4f-146">O nome do fornecedor da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="bec4f-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="bec4f-147">-PurchasePlanName</span></span>
<span data-ttu-id="bec4f-148">A ID do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="bec4f-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="bec4f-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="bec4f-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="bec4f-150">A ID do produto do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="bec4f-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="bec4f-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="bec4f-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="bec4f-152">A ID de fornecedor para o plano de compra.</span><span class="sxs-lookup"><span data-stu-id="bec4f-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="bec4f-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="bec4f-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="bec4f-154">O URI da nota de lançamento.</span><span class="sxs-lookup"><span data-stu-id="bec4f-154">The release note uri.</span></span>

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

### <span data-ttu-id="bec4f-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec4f-155">-ResourceGroupName</span></span>
<span data-ttu-id="bec4f-156">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bec4f-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="bec4f-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="bec4f-157">-Sku</span></span>
<span data-ttu-id="bec4f-158">O nome da SKU da definição da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="bec4f-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="bec4f-159">-Marca</span><span class="sxs-lookup"><span data-stu-id="bec4f-159">-Tag</span></span>
<span data-ttu-id="bec4f-160">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="bec4f-160">Resource tags</span></span>

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

### <span data-ttu-id="bec4f-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bec4f-161">-Confirm</span></span>
<span data-ttu-id="bec4f-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bec4f-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec4f-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec4f-163">-WhatIf</span></span>
<span data-ttu-id="bec4f-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bec4f-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec4f-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bec4f-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec4f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec4f-166">CommonParameters</span></span>
<span data-ttu-id="bec4f-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec4f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec4f-168">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bec4f-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec4f-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bec4f-169">INPUTS</span></span>

### <span data-ttu-id="bec4f-170">System. String</span><span class="sxs-lookup"><span data-stu-id="bec4f-170">System.String</span></span>

### <span data-ttu-id="bec4f-171">Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="bec4f-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="bec4f-172">Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="bec4f-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="bec4f-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bec4f-173">System.DateTime</span></span>

### <span data-ttu-id="bec4f-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bec4f-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bec4f-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bec4f-175">System.Int32</span></span>

### <span data-ttu-id="bec4f-176">System. String []</span><span class="sxs-lookup"><span data-stu-id="bec4f-176">System.String[]</span></span>

## <span data-ttu-id="bec4f-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bec4f-177">OUTPUTS</span></span>

### <span data-ttu-id="bec4f-178">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="bec4f-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="bec4f-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bec4f-179">NOTES</span></span>

## <span data-ttu-id="bec4f-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bec4f-180">RELATED LINKS</span></span>
