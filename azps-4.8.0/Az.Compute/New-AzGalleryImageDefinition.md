---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955066"
---
# <span data-ttu-id="47eda-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="47eda-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="47eda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47eda-102">SYNOPSIS</span></span>
<span data-ttu-id="47eda-103">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="47eda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47eda-104">SYNTAX</span></span>

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

## <span data-ttu-id="47eda-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47eda-105">DESCRIPTION</span></span>
<span data-ttu-id="47eda-106">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="47eda-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47eda-107">EXAMPLES</span></span>

### <span data-ttu-id="47eda-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47eda-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="47eda-109">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="47eda-110">OS</span><span class="sxs-lookup"><span data-stu-id="47eda-110">PARAMETERS</span></span>

### <span data-ttu-id="47eda-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47eda-111">-AsJob</span></span>
<span data-ttu-id="47eda-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="47eda-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47eda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47eda-113">-DefaultProfile</span></span>
<span data-ttu-id="47eda-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47eda-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47eda-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="47eda-115">-Description</span></span>
<span data-ttu-id="47eda-116">A descrição do recurso de definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="47eda-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="47eda-117">-DisallowedDiskType</span></span>
<span data-ttu-id="47eda-118">Os tipos de disco não permitidos.</span><span class="sxs-lookup"><span data-stu-id="47eda-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="47eda-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="47eda-119">-EndOfLifeDate</span></span>
<span data-ttu-id="47eda-120">A data de fim da vida útil da definição de imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="47eda-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="47eda-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="47eda-121">-Eula</span></span>
<span data-ttu-id="47eda-122">O contrato de EULA para a definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="47eda-123">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="47eda-123">-GalleryName</span></span>
<span data-ttu-id="47eda-124">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="47eda-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="47eda-125">-HyperVGeneration</span></span>
<span data-ttu-id="47eda-126">A geração de hipervisor da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="47eda-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="47eda-127">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="47eda-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="47eda-128">Os valores permitidos são v1 e v2.</span><span class="sxs-lookup"><span data-stu-id="47eda-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="47eda-129">-Local</span><span class="sxs-lookup"><span data-stu-id="47eda-129">-Location</span></span>
<span data-ttu-id="47eda-130">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="47eda-130">Resource location</span></span>

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

### <span data-ttu-id="47eda-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="47eda-131">-MaximumMemory</span></span>
<span data-ttu-id="47eda-132">O máximo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="47eda-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="47eda-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="47eda-133">-MaximumVCPU</span></span>
<span data-ttu-id="47eda-134">O máximo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="47eda-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="47eda-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="47eda-135">-MinimumMemory</span></span>
<span data-ttu-id="47eda-136">O mínimo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="47eda-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="47eda-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="47eda-137">-MinimumVCPU</span></span>
<span data-ttu-id="47eda-138">O mínimo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="47eda-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="47eda-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="47eda-139">-Name</span></span>
<span data-ttu-id="47eda-140">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="47eda-141">-Oferta</span><span class="sxs-lookup"><span data-stu-id="47eda-141">-Offer</span></span>
<span data-ttu-id="47eda-142">O nome da oferta de definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="47eda-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="47eda-143">-OsState</span></span>
<span data-ttu-id="47eda-144">O estado do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="47eda-144">The state of OS</span></span>

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

### <span data-ttu-id="47eda-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="47eda-145">-OsType</span></span>
<span data-ttu-id="47eda-146">O tipo de sistema operacional</span><span class="sxs-lookup"><span data-stu-id="47eda-146">The type of OS</span></span>

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

### <span data-ttu-id="47eda-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="47eda-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="47eda-148">O URI da declaração de privacidade.</span><span class="sxs-lookup"><span data-stu-id="47eda-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="47eda-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="47eda-149">-Publisher</span></span>
<span data-ttu-id="47eda-150">O nome do fornecedor da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="47eda-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="47eda-151">-PurchasePlanName</span></span>
<span data-ttu-id="47eda-152">A ID do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="47eda-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="47eda-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="47eda-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="47eda-154">A ID do produto do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="47eda-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="47eda-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="47eda-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="47eda-156">A ID de fornecedor para o plano de compra.</span><span class="sxs-lookup"><span data-stu-id="47eda-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="47eda-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="47eda-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="47eda-158">O URI da nota de lançamento.</span><span class="sxs-lookup"><span data-stu-id="47eda-158">The release note uri.</span></span>

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

### <span data-ttu-id="47eda-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47eda-159">-ResourceGroupName</span></span>
<span data-ttu-id="47eda-160">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="47eda-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="47eda-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="47eda-161">-Sku</span></span>
<span data-ttu-id="47eda-162">O nome da SKU da definição da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="47eda-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="47eda-163">-Marca</span><span class="sxs-lookup"><span data-stu-id="47eda-163">-Tag</span></span>
<span data-ttu-id="47eda-164">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="47eda-164">Resource tags</span></span>

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

### <span data-ttu-id="47eda-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47eda-165">-Confirm</span></span>
<span data-ttu-id="47eda-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47eda-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47eda-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47eda-167">-WhatIf</span></span>
<span data-ttu-id="47eda-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47eda-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47eda-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47eda-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47eda-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47eda-170">CommonParameters</span></span>
<span data-ttu-id="47eda-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47eda-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47eda-172">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47eda-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47eda-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47eda-173">INPUTS</span></span>

### <span data-ttu-id="47eda-174">System. String</span><span class="sxs-lookup"><span data-stu-id="47eda-174">System.String</span></span>

### <span data-ttu-id="47eda-175">Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="47eda-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="47eda-176">Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="47eda-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="47eda-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="47eda-177">System.DateTime</span></span>

### <span data-ttu-id="47eda-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="47eda-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="47eda-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="47eda-179">System.Int32</span></span>

### <span data-ttu-id="47eda-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="47eda-180">System.String[]</span></span>

## <span data-ttu-id="47eda-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47eda-181">OUTPUTS</span></span>

### <span data-ttu-id="47eda-182">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="47eda-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="47eda-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47eda-183">NOTES</span></span>

## <span data-ttu-id="47eda-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47eda-184">RELATED LINKS</span></span>
