---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 7c62860f3829c07621c951175b00a4be4960c95f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597324"
---
# <span data-ttu-id="4a307-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4a307-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="4a307-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a307-102">SYNOPSIS</span></span>
<span data-ttu-id="4a307-103">Excluir uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="4a307-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="4a307-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a307-104">SYNTAX</span></span>

### <span data-ttu-id="4a307-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a307-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a307-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4a307-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a307-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4a307-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a307-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a307-108">DESCRIPTION</span></span>
<span data-ttu-id="4a307-109">Excluir uma versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="4a307-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="4a307-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a307-110">EXAMPLES</span></span>

### <span data-ttu-id="4a307-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a307-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="4a307-112">Exclua a versão da imagem da Galeria fornecida.</span><span class="sxs-lookup"><span data-stu-id="4a307-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="4a307-113">OS</span><span class="sxs-lookup"><span data-stu-id="4a307-113">PARAMETERS</span></span>

### <span data-ttu-id="4a307-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a307-114">-AsJob</span></span>
<span data-ttu-id="4a307-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4a307-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a307-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a307-116">-DefaultProfile</span></span>
<span data-ttu-id="4a307-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a307-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a307-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4a307-118">-Force</span></span>
<span data-ttu-id="4a307-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4a307-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4a307-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="4a307-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="4a307-121">O nome da definição de imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="4a307-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="4a307-122">-Galleryname</span><span class="sxs-lookup"><span data-stu-id="4a307-122">-GalleryName</span></span>
<span data-ttu-id="4a307-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="4a307-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="4a307-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a307-124">-InputObject</span></span>
<span data-ttu-id="4a307-125">O objeto da versão da imagem da Galeria PS</span><span class="sxs-lookup"><span data-stu-id="4a307-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="4a307-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a307-126">-Name</span></span>
<span data-ttu-id="4a307-127">O nome da versão da imagem da galeria.</span><span class="sxs-lookup"><span data-stu-id="4a307-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="4a307-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a307-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a307-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a307-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a307-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a307-130">-ResourceId</span></span>
<span data-ttu-id="4a307-131">A ID do recurso para a versão da imagem da Galeria</span><span class="sxs-lookup"><span data-stu-id="4a307-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="4a307-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a307-132">-Confirm</span></span>
<span data-ttu-id="4a307-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a307-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a307-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a307-134">-WhatIf</span></span>
<span data-ttu-id="4a307-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a307-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a307-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a307-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a307-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a307-137">CommonParameters</span></span>
<span data-ttu-id="4a307-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a307-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a307-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a307-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a307-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a307-140">INPUTS</span></span>

### <span data-ttu-id="4a307-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4a307-141">System.String</span></span>

### <span data-ttu-id="4a307-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4a307-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="4a307-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a307-143">OUTPUTS</span></span>

### <span data-ttu-id="4a307-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4a307-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4a307-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a307-145">NOTES</span></span>

## <span data-ttu-id="4a307-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a307-146">RELATED LINKS</span></span>
