---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
ms.openlocfilehash: c2a65eeb742d4182dfad0cd32be1d78951977096
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428537"
---
# <span data-ttu-id="9bb1b-101">Remove-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="9bb1b-101">Remove-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="9bb1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bb1b-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb1b-103">Excluir uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-103">Delete a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bb1b-104">SYNTAX</span></span>

### <span data-ttu-id="9bb1b-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="9bb1b-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb1b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9bb1b-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb1b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9bb1b-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bb1b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bb1b-108">DESCRIPTION</span></span>
<span data-ttu-id="9bb1b-109">Excluir uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="9bb1b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bb1b-110">EXAMPLES</span></span>

### <span data-ttu-id="9bb1b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9bb1b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="9bb1b-112">Exclua a versão da imagem da Galeria fornecida.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="9bb1b-113">OS</span><span class="sxs-lookup"><span data-stu-id="9bb1b-113">PARAMETERS</span></span>

### <span data-ttu-id="9bb1b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bb1b-114">-AsJob</span></span>
<span data-ttu-id="9bb1b-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9bb1b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bb1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb1b-116">-DefaultProfile</span></span>
<span data-ttu-id="9bb1b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bb1b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9bb1b-118">-Force</span></span>
<span data-ttu-id="9bb1b-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bb1b-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9bb1b-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="9bb1b-121">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="9bb1b-122">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="9bb1b-122">-GalleryName</span></span>
<span data-ttu-id="9bb1b-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="9bb1b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bb1b-124">-InputObject</span></span>
<span data-ttu-id="9bb1b-125">O objeto da versão da imagem da Galeria PS</span><span class="sxs-lookup"><span data-stu-id="9bb1b-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="9bb1b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bb1b-126">-Name</span></span>
<span data-ttu-id="9bb1b-127">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="9bb1b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb1b-128">-ResourceGroupName</span></span>
<span data-ttu-id="9bb1b-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="9bb1b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bb1b-130">-ResourceId</span></span>
<span data-ttu-id="9bb1b-131">A ID do recurso para a versão da imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="9bb1b-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="9bb1b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9bb1b-132">-Confirm</span></span>
<span data-ttu-id="9bb1b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb1b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb1b-134">-WhatIf</span></span>
<span data-ttu-id="9bb1b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bb1b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb1b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb1b-137">CommonParameters</span></span>
<span data-ttu-id="9bb1b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bb1b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb1b-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb1b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb1b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bb1b-140">INPUTS</span></span>

### <span data-ttu-id="9bb1b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9bb1b-141">System.String</span></span>

### <span data-ttu-id="9bb1b-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="9bb1b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="9bb1b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bb1b-143">OUTPUTS</span></span>

### <span data-ttu-id="9bb1b-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9bb1b-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9bb1b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bb1b-145">NOTES</span></span>

## <span data-ttu-id="9bb1b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bb1b-146">RELATED LINKS</span></span>
