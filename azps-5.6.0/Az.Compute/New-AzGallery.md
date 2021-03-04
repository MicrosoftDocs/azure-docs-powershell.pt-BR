---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 47ba904378ed8f58da29876d5835ca43bb8a7a31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886347"
---
# <span data-ttu-id="218a2-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="218a2-101">New-AzGallery</span></span>

## <span data-ttu-id="218a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="218a2-102">SYNOPSIS</span></span>
<span data-ttu-id="218a2-103">Crie uma galeria.</span><span class="sxs-lookup"><span data-stu-id="218a2-103">Create a gallery.</span></span>

## <span data-ttu-id="218a2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="218a2-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="218a2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="218a2-105">DESCRIPTION</span></span>
<span data-ttu-id="218a2-106">Crie uma galeria.</span><span class="sxs-lookup"><span data-stu-id="218a2-106">Create a gallery.</span></span>

## <span data-ttu-id="218a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="218a2-107">EXAMPLES</span></span>

### <span data-ttu-id="218a2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="218a2-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="218a2-109">Crie uma galeria.</span><span class="sxs-lookup"><span data-stu-id="218a2-109">Create a gallery.</span></span>

## <span data-ttu-id="218a2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="218a2-110">PARAMETERS</span></span>

### <span data-ttu-id="218a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="218a2-111">-AsJob</span></span>
<span data-ttu-id="218a2-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="218a2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="218a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="218a2-113">-DefaultProfile</span></span>
<span data-ttu-id="218a2-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="218a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="218a2-115">-Description</span><span class="sxs-lookup"><span data-stu-id="218a2-115">-Description</span></span>
<span data-ttu-id="218a2-116">A descrição do recurso galeria.</span><span class="sxs-lookup"><span data-stu-id="218a2-116">The description of the gallery resource.</span></span>

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

### <span data-ttu-id="218a2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="218a2-117">-Location</span></span>
<span data-ttu-id="218a2-118">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="218a2-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218a2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="218a2-119">-Name</span></span>
<span data-ttu-id="218a2-120">O nome da galeria.</span><span class="sxs-lookup"><span data-stu-id="218a2-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="218a2-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="218a2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="218a2-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="218a2-123">-Tag</span></span>
<span data-ttu-id="218a2-124">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="218a2-124">Resource tags</span></span>

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

### <span data-ttu-id="218a2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="218a2-125">-Confirm</span></span>
<span data-ttu-id="218a2-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="218a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="218a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218a2-127">-WhatIf</span></span>
<span data-ttu-id="218a2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="218a2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="218a2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="218a2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="218a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218a2-130">CommonParameters</span></span>
<span data-ttu-id="218a2-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="218a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218a2-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="218a2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218a2-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="218a2-133">INPUTS</span></span>

### <span data-ttu-id="218a2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="218a2-134">System.String</span></span>

### <span data-ttu-id="218a2-135">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="218a2-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="218a2-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="218a2-136">OUTPUTS</span></span>

### <span data-ttu-id="218a2-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="218a2-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="218a2-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="218a2-138">NOTES</span></span>

## <span data-ttu-id="218a2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="218a2-139">RELATED LINKS</span></span>
