---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGallery.md
ms.openlocfilehash: 5d8ed5a26e141d0ae8d6eb7494a76d8c53590d29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609820"
---
# <span data-ttu-id="76fd4-101">Update-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="76fd4-101">Update-AzureRmGallery</span></span>

## <span data-ttu-id="76fd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="76fd4-103">Atualizar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="76fd4-103">Update a gallery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76fd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76fd4-104">SYNTAX</span></span>

### <span data-ttu-id="76fd4-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="76fd4-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76fd4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="76fd4-106">ResourceIdParameter</span></span>
```
Update-AzureRmGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76fd4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="76fd4-107">ObjectParameter</span></span>
```
Update-AzureRmGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76fd4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76fd4-108">DESCRIPTION</span></span>
<span data-ttu-id="76fd4-109">Atualizar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="76fd4-109">Update a gallery.</span></span>

## <span data-ttu-id="76fd4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76fd4-110">EXAMPLES</span></span>

### <span data-ttu-id="76fd4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76fd4-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="76fd4-112">Atualizar uma galeria.</span><span class="sxs-lookup"><span data-stu-id="76fd4-112">Update a gallery.</span></span>

## <span data-ttu-id="76fd4-113">OS</span><span class="sxs-lookup"><span data-stu-id="76fd4-113">PARAMETERS</span></span>

### <span data-ttu-id="76fd4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76fd4-114">-AsJob</span></span>
<span data-ttu-id="76fd4-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="76fd4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76fd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fd4-116">-DefaultProfile</span></span>
<span data-ttu-id="76fd4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76fd4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76fd4-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="76fd4-118">-Description</span></span>
<span data-ttu-id="76fd4-119">A descrição do recurso de galeria.</span><span class="sxs-lookup"><span data-stu-id="76fd4-119">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="76fd4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76fd4-120">-InputObject</span></span>
<span data-ttu-id="76fd4-121">O objeto da Galeria PS.</span><span class="sxs-lookup"><span data-stu-id="76fd4-121">The PS Gallery Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76fd4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="76fd4-122">-Name</span></span>
<span data-ttu-id="76fd4-123">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="76fd4-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76fd4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fd4-124">-ResourceGroupName</span></span>
<span data-ttu-id="76fd4-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76fd4-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="76fd4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76fd4-126">-ResourceId</span></span>
<span data-ttu-id="76fd4-127">A ID do recurso para a Galeria</span><span class="sxs-lookup"><span data-stu-id="76fd4-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="76fd4-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="76fd4-128">-Tag</span></span>
<span data-ttu-id="76fd4-129">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="76fd4-129">Resource tags</span></span>

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

### <span data-ttu-id="76fd4-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76fd4-130">-Confirm</span></span>
<span data-ttu-id="76fd4-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76fd4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76fd4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76fd4-132">-WhatIf</span></span>
<span data-ttu-id="76fd4-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76fd4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76fd4-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76fd4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76fd4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fd4-135">CommonParameters</span></span>
<span data-ttu-id="76fd4-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fd4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fd4-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76fd4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fd4-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76fd4-138">INPUTS</span></span>

### <span data-ttu-id="76fd4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="76fd4-139">System.String</span></span>

### <span data-ttu-id="76fd4-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="76fd4-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="76fd4-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="76fd4-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="76fd4-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76fd4-142">OUTPUTS</span></span>

### <span data-ttu-id="76fd4-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="76fd4-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="76fd4-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76fd4-144">NOTES</span></span>

## <span data-ttu-id="76fd4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76fd4-145">RELATED LINKS</span></span>
