---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774453"
---
# <span data-ttu-id="82886-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="82886-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="82886-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82886-102">SYNOPSIS</span></span>
<span data-ttu-id="82886-103">Lista itens da galeria.</span><span class="sxs-lookup"><span data-stu-id="82886-103">Lists gallery items.</span></span>

## <span data-ttu-id="82886-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82886-104">SYNTAX</span></span>

### <span data-ttu-id="82886-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="82886-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="82886-106">Obter</span><span class="sxs-lookup"><span data-stu-id="82886-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="82886-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82886-107">DESCRIPTION</span></span>
<span data-ttu-id="82886-108">Obter uma lista de itens de galeria disponíveis no Azure Stack Marketplace</span><span class="sxs-lookup"><span data-stu-id="82886-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="82886-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82886-109">EXAMPLES</span></span>

### <span data-ttu-id="82886-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="82886-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="82886-111">Listar itens da galeria.</span><span class="sxs-lookup"><span data-stu-id="82886-111">List gallery items.</span></span>

### <span data-ttu-id="82886-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="82886-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="82886-113">Obter um item de Galeria por nome.</span><span class="sxs-lookup"><span data-stu-id="82886-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="82886-114">OS</span><span class="sxs-lookup"><span data-stu-id="82886-114">PARAMETERS</span></span>

### <span data-ttu-id="82886-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="82886-115">-Name</span></span>
<span data-ttu-id="82886-116">Identidade do item de galeria.</span><span class="sxs-lookup"><span data-stu-id="82886-116">Identity of the gallery item.</span></span>
<span data-ttu-id="82886-117">Inclui o nome do fornecedor, o nome do item e pode incluir a versão separada por um caractere de ponto.</span><span class="sxs-lookup"><span data-stu-id="82886-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82886-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82886-118">CommonParameters</span></span>
<span data-ttu-id="82886-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82886-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82886-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82886-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82886-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82886-121">INPUTS</span></span>

## <span data-ttu-id="82886-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82886-122">OUTPUTS</span></span>

### <span data-ttu-id="82886-123">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="82886-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="82886-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82886-124">NOTES</span></span>

## <span data-ttu-id="82886-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82886-125">RELATED LINKS</span></span>

