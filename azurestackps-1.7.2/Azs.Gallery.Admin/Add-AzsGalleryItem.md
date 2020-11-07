---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774454"
---
# <span data-ttu-id="0fc3c-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="0fc3c-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="0fc3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc3c-103">Carrega um item de galeria de provedores para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="0fc3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fc3c-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fc3c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0fc3c-105">DESCRIPTION</span></span>
<span data-ttu-id="0fc3c-106">Carrega um item de galeria de provedores para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="0fc3c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fc3c-107">EXAMPLES</span></span>

### <span data-ttu-id="0fc3c-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0fc3c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="0fc3c-109">Criar um novo item de galeria.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-109">Create a new gallery item.</span></span>

## <span data-ttu-id="0fc3c-110">OS</span><span class="sxs-lookup"><span data-stu-id="0fc3c-110">PARAMETERS</span></span>

### <span data-ttu-id="0fc3c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0fc3c-111">-Force</span></span>
<span data-ttu-id="0fc3c-112">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0fc3c-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="0fc3c-113">-GalleryItemUri</span></span>
<span data-ttu-id="0fc3c-114">O URI para o arquivo JSON do item da galeria.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-114">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="0fc3c-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0fc3c-115">-Confirm</span></span>
<span data-ttu-id="0fc3c-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc3c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc3c-117">-WhatIf</span></span>
<span data-ttu-id="0fc3c-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc3c-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc3c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc3c-120">CommonParameters</span></span>
<span data-ttu-id="0fc3c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc3c-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fc3c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc3c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0fc3c-123">INPUTS</span></span>

## <span data-ttu-id="0fc3c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0fc3c-124">OUTPUTS</span></span>

### <span data-ttu-id="0fc3c-125">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="0fc3c-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="0fc3c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0fc3c-126">NOTES</span></span>

## <span data-ttu-id="0fc3c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fc3c-127">RELATED LINKS</span></span>

