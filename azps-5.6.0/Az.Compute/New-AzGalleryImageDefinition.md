---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: fbfb0a10016d81edcffeb62580b1ca0ff9b5b341
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886082"
---
# <span data-ttu-id="a7dc1-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="a7dc1-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="a7dc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="a7dc1-103">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="a7dc1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a7dc1-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7dc1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="a7dc1-106">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="a7dc1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7dc1-107">EXAMPLES</span></span>

### <span data-ttu-id="a7dc1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7dc1-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="a7dc1-109">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="a7dc1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a7dc1-110">PARAMETERS</span></span>

### <span data-ttu-id="a7dc1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7dc1-111">-AsJob</span></span>
<span data-ttu-id="a7dc1-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a7dc1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7dc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7dc1-113">-DefaultProfile</span></span>
<span data-ttu-id="a7dc1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7dc1-115">-Description</span><span class="sxs-lookup"><span data-stu-id="a7dc1-115">-Description</span></span>
<span data-ttu-id="a7dc1-116">A descrição do recurso definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="a7dc1-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="a7dc1-117">-DisallowedDiskType</span></span>
<span data-ttu-id="a7dc1-118">Os tipos de disco não permitidos.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="a7dc1-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="a7dc1-119">-EndOfLifeDate</span></span>
<span data-ttu-id="a7dc1-120">A data de término da vida útil da definição de imagem da galeria</span><span class="sxs-lookup"><span data-stu-id="a7dc1-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="a7dc1-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="a7dc1-121">-Eula</span></span>
<span data-ttu-id="a7dc1-122">O contrato Eula para a Definição de Imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="a7dc1-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="a7dc1-123">-GalleryName</span></span>
<span data-ttu-id="a7dc1-124">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="a7dc1-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="a7dc1-125">-HyperVGeneration</span></span>
<span data-ttu-id="a7dc1-126">A geração do hipervisor da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="a7dc1-127">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="a7dc1-128">Os valores permitidos são V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="a7dc1-129">-Location</span><span class="sxs-lookup"><span data-stu-id="a7dc1-129">-Location</span></span>
<span data-ttu-id="a7dc1-130">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="a7dc1-130">Resource location</span></span>

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

### <span data-ttu-id="a7dc1-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="a7dc1-131">-MaximumMemory</span></span>
<span data-ttu-id="a7dc1-132">O máximo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="a7dc1-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="a7dc1-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="a7dc1-133">-MaximumVCPU</span></span>
<span data-ttu-id="a7dc1-134">O máximo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="a7dc1-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="a7dc1-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="a7dc1-135">-MinimumMemory</span></span>
<span data-ttu-id="a7dc1-136">O mínimo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="a7dc1-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="a7dc1-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="a7dc1-137">-MinimumVCPU</span></span>
<span data-ttu-id="a7dc1-138">O mínimo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="a7dc1-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="a7dc1-139">-Name</span><span class="sxs-lookup"><span data-stu-id="a7dc1-139">-Name</span></span>
<span data-ttu-id="a7dc1-140">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="a7dc1-141">-Offer</span><span class="sxs-lookup"><span data-stu-id="a7dc1-141">-Offer</span></span>
<span data-ttu-id="a7dc1-142">O nome da oferta de Definição de Imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="a7dc1-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="a7dc1-143">-OsState</span></span>
<span data-ttu-id="a7dc1-144">O estado do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a7dc1-144">The state of OS</span></span>

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

### <span data-ttu-id="a7dc1-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="a7dc1-145">-OsType</span></span>
<span data-ttu-id="a7dc1-146">O tipo de sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a7dc1-146">The type of OS</span></span>

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

### <span data-ttu-id="a7dc1-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="a7dc1-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="a7dc1-148">O uri da instrução de privacidade.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="a7dc1-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a7dc1-149">-Publisher</span></span>
<span data-ttu-id="a7dc1-150">O nome do editor de Definição de Imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="a7dc1-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="a7dc1-151">-PurchasePlanName</span></span>
<span data-ttu-id="a7dc1-152">A ID do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="a7dc1-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="a7dc1-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="a7dc1-154">A ID do produto para o plano de compra.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="a7dc1-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="a7dc1-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="a7dc1-156">A ID do editor do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="a7dc1-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="a7dc1-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="a7dc1-158">O uri da nota de lançamento.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-158">The release note uri.</span></span>

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

### <span data-ttu-id="a7dc1-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7dc1-159">-ResourceGroupName</span></span>
<span data-ttu-id="a7dc1-160">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7dc1-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="a7dc1-161">-Sku</span></span>
<span data-ttu-id="a7dc1-162">O nome da SKU de Definição de Imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="a7dc1-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7dc1-163">-Tag</span></span>
<span data-ttu-id="a7dc1-164">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="a7dc1-164">Resource tags</span></span>

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

### <span data-ttu-id="a7dc1-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7dc1-165">-Confirm</span></span>
<span data-ttu-id="a7dc1-166">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7dc1-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7dc1-167">-WhatIf</span></span>
<span data-ttu-id="a7dc1-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7dc1-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7dc1-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7dc1-170">CommonParameters</span></span>
<span data-ttu-id="a7dc1-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7dc1-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7dc1-172">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7dc1-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7dc1-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7dc1-173">INPUTS</span></span>

### <span data-ttu-id="a7dc1-174">System.String</span><span class="sxs-lookup"><span data-stu-id="a7dc1-174">System.String</span></span>

### <span data-ttu-id="a7dc1-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="a7dc1-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="a7dc1-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="a7dc1-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="a7dc1-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="a7dc1-177">System.DateTime</span></span>

### <span data-ttu-id="a7dc1-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a7dc1-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a7dc1-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a7dc1-179">System.Int32</span></span>

### <span data-ttu-id="a7dc1-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a7dc1-180">System.String[]</span></span>

## <span data-ttu-id="a7dc1-181">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a7dc1-181">OUTPUTS</span></span>

### <span data-ttu-id="a7dc1-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="a7dc1-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="a7dc1-183">NOTES</span><span class="sxs-lookup"><span data-stu-id="a7dc1-183">NOTES</span></span>

## <span data-ttu-id="a7dc1-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7dc1-184">RELATED LINKS</span></span>
