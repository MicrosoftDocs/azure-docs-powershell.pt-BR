---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774714"
---
# <span data-ttu-id="2b659-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="2b659-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="2b659-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b659-102">SYNOPSIS</span></span>
<span data-ttu-id="2b659-103">Carrega um item de galeria de provedores para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b659-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="2b659-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b659-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b659-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b659-105">DESCRIPTION</span></span>
<span data-ttu-id="2b659-106">Carrega um item de galeria de provedores para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b659-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="2b659-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b659-107">EXAMPLES</span></span>

### <span data-ttu-id="2b659-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="2b659-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="2b659-109">Criar um novo item de galeria.</span><span class="sxs-lookup"><span data-stu-id="2b659-109">Create a new gallery item.</span></span>

## <span data-ttu-id="2b659-110">OS</span><span class="sxs-lookup"><span data-stu-id="2b659-110">PARAMETERS</span></span>

### <span data-ttu-id="2b659-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="2b659-111">-GalleryItemUri</span></span>
<span data-ttu-id="2b659-112">O URI para o arquivo JSON do item da galeria.</span><span class="sxs-lookup"><span data-stu-id="2b659-112">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b659-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2b659-113">-Force</span></span>
<span data-ttu-id="2b659-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2b659-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b659-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b659-115">-WhatIf</span></span>
<span data-ttu-id="2b659-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b659-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b659-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b659-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b659-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2b659-118">-Confirm</span></span>
<span data-ttu-id="2b659-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b659-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b659-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b659-120">CommonParameters</span></span>
<span data-ttu-id="2b659-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b659-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b659-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b659-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b659-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b659-123">INPUTS</span></span>

## <span data-ttu-id="2b659-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b659-124">OUTPUTS</span></span>

### <span data-ttu-id="2b659-125">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="2b659-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="2b659-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b659-126">NOTES</span></span>

## <span data-ttu-id="2b659-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b659-127">RELATED LINKS</span></span>
