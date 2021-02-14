---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111143"
---
# <span data-ttu-id="175bc-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="175bc-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="175bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="175bc-102">SYNOPSIS</span></span>
<span data-ttu-id="175bc-103">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="175bc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="175bc-104">SYNTAX</span></span>

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

## <span data-ttu-id="175bc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="175bc-105">DESCRIPTION</span></span>
<span data-ttu-id="175bc-106">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="175bc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="175bc-107">EXAMPLES</span></span>

### <span data-ttu-id="175bc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="175bc-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="175bc-109">Criar uma definição de imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="175bc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="175bc-110">PARAMETERS</span></span>

### <span data-ttu-id="175bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="175bc-111">-AsJob</span></span>
<span data-ttu-id="175bc-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="175bc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="175bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="175bc-113">-DefaultProfile</span></span>
<span data-ttu-id="175bc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="175bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="175bc-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="175bc-115">-Description</span></span>
<span data-ttu-id="175bc-116">A descrição do recurso Definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="175bc-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="175bc-117">-DisallowedDiskType</span></span>
<span data-ttu-id="175bc-118">Os tipos de disco não permitidos.</span><span class="sxs-lookup"><span data-stu-id="175bc-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="175bc-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="175bc-119">-EndOfLifeDate</span></span>
<span data-ttu-id="175bc-120">A data de fim da vida útil da Galeria de Definição de Imagens</span><span class="sxs-lookup"><span data-stu-id="175bc-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="175bc-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="175bc-121">-Eula</span></span>
<span data-ttu-id="175bc-122">O contrato Eula para a Definição de Imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="175bc-123">-Nomeda Galeria</span><span class="sxs-lookup"><span data-stu-id="175bc-123">-GalleryName</span></span>
<span data-ttu-id="175bc-124">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="175bc-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="175bc-125">-HyperVGeneration</span></span>
<span data-ttu-id="175bc-126">A geração de hipervisor da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="175bc-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="175bc-127">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="175bc-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="175bc-128">Os valores permitidos são V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="175bc-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="175bc-129">-Local</span><span class="sxs-lookup"><span data-stu-id="175bc-129">-Location</span></span>
<span data-ttu-id="175bc-130">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="175bc-130">Resource location</span></span>

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

### <span data-ttu-id="175bc-131">-MáximoMemory</span><span class="sxs-lookup"><span data-stu-id="175bc-131">-MaximumMemory</span></span>
<span data-ttu-id="175bc-132">O máximo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="175bc-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="175bc-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="175bc-133">-MaximumVCPU</span></span>
<span data-ttu-id="175bc-134">O máximo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="175bc-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="175bc-135">-MínimoMemory</span><span class="sxs-lookup"><span data-stu-id="175bc-135">-MinimumMemory</span></span>
<span data-ttu-id="175bc-136">O mínimo da memória recomendada</span><span class="sxs-lookup"><span data-stu-id="175bc-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="175bc-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="175bc-137">-MinimumVCPU</span></span>
<span data-ttu-id="175bc-138">O mínimo do núcleo de CPU recomendado</span><span class="sxs-lookup"><span data-stu-id="175bc-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="175bc-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="175bc-139">-Name</span></span>
<span data-ttu-id="175bc-140">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="175bc-141">-Oferta</span><span class="sxs-lookup"><span data-stu-id="175bc-141">-Offer</span></span>
<span data-ttu-id="175bc-142">O nome da oferta definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="175bc-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="175bc-143">-OsState</span></span>
<span data-ttu-id="175bc-144">O estado do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="175bc-144">The state of OS</span></span>

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

### <span data-ttu-id="175bc-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="175bc-145">-OsType</span></span>
<span data-ttu-id="175bc-146">O tipo de sistema operacional</span><span class="sxs-lookup"><span data-stu-id="175bc-146">The type of OS</span></span>

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

### <span data-ttu-id="175bc-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="175bc-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="175bc-148">A política de privacidade uri.</span><span class="sxs-lookup"><span data-stu-id="175bc-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="175bc-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="175bc-149">-Publisher</span></span>
<span data-ttu-id="175bc-150">O nome do editor definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="175bc-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="175bc-151">-PurchasePlanName</span></span>
<span data-ttu-id="175bc-152">A ID do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="175bc-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="175bc-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="175bc-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="175bc-154">A ID do produto para o plano de compra.</span><span class="sxs-lookup"><span data-stu-id="175bc-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="175bc-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="175bc-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="175bc-156">A ID do editor do plano de compra.</span><span class="sxs-lookup"><span data-stu-id="175bc-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="175bc-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="175bc-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="175bc-158">A nota de lançamento uri.</span><span class="sxs-lookup"><span data-stu-id="175bc-158">The release note uri.</span></span>

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

### <span data-ttu-id="175bc-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="175bc-159">-ResourceGroupName</span></span>
<span data-ttu-id="175bc-160">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="175bc-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="175bc-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="175bc-161">-Sku</span></span>
<span data-ttu-id="175bc-162">O nome da SKU de Definição de Imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="175bc-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="175bc-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="175bc-163">-Tag</span></span>
<span data-ttu-id="175bc-164">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="175bc-164">Resource tags</span></span>

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

### <span data-ttu-id="175bc-165">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="175bc-165">-Confirm</span></span>
<span data-ttu-id="175bc-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="175bc-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="175bc-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="175bc-167">-WhatIf</span></span>
<span data-ttu-id="175bc-168">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="175bc-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="175bc-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="175bc-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="175bc-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="175bc-170">CommonParameters</span></span>
<span data-ttu-id="175bc-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="175bc-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="175bc-172">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="175bc-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="175bc-173">Entradas</span><span class="sxs-lookup"><span data-stu-id="175bc-173">INPUTS</span></span>

### <span data-ttu-id="175bc-174">System.String</span><span class="sxs-lookup"><span data-stu-id="175bc-174">System.String</span></span>

### <span data-ttu-id="175bc-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="175bc-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="175bc-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="175bc-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="175bc-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="175bc-177">System.DateTime</span></span>

### <span data-ttu-id="175bc-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="175bc-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="175bc-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="175bc-179">System.Int32</span></span>

### <span data-ttu-id="175bc-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="175bc-180">System.String[]</span></span>

## <span data-ttu-id="175bc-181">Saídas</span><span class="sxs-lookup"><span data-stu-id="175bc-181">OUTPUTS</span></span>

### <span data-ttu-id="175bc-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="175bc-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="175bc-183">Notas</span><span class="sxs-lookup"><span data-stu-id="175bc-183">NOTES</span></span>

## <span data-ttu-id="175bc-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="175bc-184">RELATED LINKS</span></span>
