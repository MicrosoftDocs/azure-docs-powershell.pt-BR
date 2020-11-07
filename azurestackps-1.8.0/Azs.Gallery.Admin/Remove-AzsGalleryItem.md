---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774711"
---
# <span data-ttu-id="95bdb-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="95bdb-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="95bdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="95bdb-103">Excluir um item de galeria específico.</span><span class="sxs-lookup"><span data-stu-id="95bdb-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="95bdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95bdb-104">SYNTAX</span></span>

### <span data-ttu-id="95bdb-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="95bdb-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95bdb-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="95bdb-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95bdb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95bdb-107">DESCRIPTION</span></span>
<span data-ttu-id="95bdb-108">Excluir um item de galeria específico.</span><span class="sxs-lookup"><span data-stu-id="95bdb-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="95bdb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95bdb-109">EXAMPLES</span></span>

### <span data-ttu-id="95bdb-110">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="95bdb-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="95bdb-111">Excluir um item de galeria.</span><span class="sxs-lookup"><span data-stu-id="95bdb-111">Delete a gallery item.</span></span>

## <span data-ttu-id="95bdb-112">OS</span><span class="sxs-lookup"><span data-stu-id="95bdb-112">PARAMETERS</span></span>

### <span data-ttu-id="95bdb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="95bdb-113">-Name</span></span>
<span data-ttu-id="95bdb-114">Identidade do item de galeria.</span><span class="sxs-lookup"><span data-stu-id="95bdb-114">Identity of the gallery item.</span></span>
<span data-ttu-id="95bdb-115">Inclui o nome do fornecedor, o nome do item e pode incluir a versão separada por um caractere de ponto.</span><span class="sxs-lookup"><span data-stu-id="95bdb-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="95bdb-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95bdb-116">-ResourceId</span></span>
<span data-ttu-id="95bdb-117">ID de recurso do Azure totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="95bdb-117">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="95bdb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="95bdb-118">-Force</span></span>
<span data-ttu-id="95bdb-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="95bdb-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="95bdb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bdb-120">-WhatIf</span></span>
<span data-ttu-id="95bdb-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95bdb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95bdb-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95bdb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95bdb-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95bdb-123">-Confirm</span></span>
<span data-ttu-id="95bdb-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95bdb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95bdb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bdb-125">CommonParameters</span></span>
<span data-ttu-id="95bdb-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bdb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bdb-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95bdb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bdb-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95bdb-128">INPUTS</span></span>

## <span data-ttu-id="95bdb-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95bdb-129">OUTPUTS</span></span>

## <span data-ttu-id="95bdb-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95bdb-130">NOTES</span></span>

## <span data-ttu-id="95bdb-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95bdb-131">RELATED LINKS</span></span>
