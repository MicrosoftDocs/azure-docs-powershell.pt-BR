---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425825"
---
# <span data-ttu-id="c9c8f-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="c9c8f-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="c9c8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c8f-103">Excluir um item de galeria específico.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="c9c8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9c8f-104">SYNTAX</span></span>

### <span data-ttu-id="c9c8f-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="c9c8f-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c8f-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="c9c8f-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c8f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9c8f-107">DESCRIPTION</span></span>
<span data-ttu-id="c9c8f-108">Excluir um item de galeria específico.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="c9c8f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9c8f-109">EXAMPLES</span></span>

### <span data-ttu-id="c9c8f-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c9c8f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="c9c8f-111">Excluir um item de galeria.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-111">Delete a gallery item.</span></span>

## <span data-ttu-id="c9c8f-112">OS</span><span class="sxs-lookup"><span data-stu-id="c9c8f-112">PARAMETERS</span></span>

### <span data-ttu-id="c9c8f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c9c8f-113">-Force</span></span>
<span data-ttu-id="c9c8f-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c9c8f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9c8f-115">-Name</span></span>
<span data-ttu-id="c9c8f-116">Identidade do item de galeria.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-116">Identity of the gallery item.</span></span>
<span data-ttu-id="c9c8f-117">Inclui o nome do fornecedor, o nome do item e pode incluir a versão separada por um caractere de ponto.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c8f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9c8f-118">-ResourceId</span></span>
<span data-ttu-id="c9c8f-119">ID de recurso do Azure totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-119">Fully qualified Azure resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c8f-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9c8f-120">-Confirm</span></span>
<span data-ttu-id="c9c8f-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c8f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c8f-122">-WhatIf</span></span>
<span data-ttu-id="c9c8f-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c8f-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c8f-125">CommonParameters</span></span>
<span data-ttu-id="c9c8f-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c8f-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c8f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c8f-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9c8f-128">INPUTS</span></span>

## <span data-ttu-id="c9c8f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9c8f-129">OUTPUTS</span></span>

## <span data-ttu-id="c9c8f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9c8f-130">NOTES</span></span>

## <span data-ttu-id="c9c8f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9c8f-131">RELATED LINKS</span></span>
