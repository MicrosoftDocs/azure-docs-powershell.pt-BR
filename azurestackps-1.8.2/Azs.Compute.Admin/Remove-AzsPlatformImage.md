---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946783"
---
# <span data-ttu-id="687ca-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="687ca-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="687ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="687ca-102">SYNOPSIS</span></span>
<span data-ttu-id="687ca-103">Exclua uma imagem de máquina virtual do repositório de imagens da plataforma.</span><span class="sxs-lookup"><span data-stu-id="687ca-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="687ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="687ca-104">SYNTAX</span></span>

### <span data-ttu-id="687ca-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="687ca-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="687ca-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="687ca-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="687ca-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="687ca-107">DESCRIPTION</span></span>
<span data-ttu-id="687ca-108">Excluir uma imagem de plataforma</span><span class="sxs-lookup"><span data-stu-id="687ca-108">Delete a platform image</span></span>

## <span data-ttu-id="687ca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="687ca-109">EXAMPLES</span></span>

### <span data-ttu-id="687ca-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="687ca-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="687ca-111">Excluir uma imagem de plataforma existente.</span><span class="sxs-lookup"><span data-stu-id="687ca-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="687ca-112">OS</span><span class="sxs-lookup"><span data-stu-id="687ca-112">PARAMETERS</span></span>

### <span data-ttu-id="687ca-113">-Force</span><span class="sxs-lookup"><span data-stu-id="687ca-113">-Force</span></span>
<span data-ttu-id="687ca-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="687ca-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="687ca-115">-Local</span><span class="sxs-lookup"><span data-stu-id="687ca-115">-Location</span></span>
<span data-ttu-id="687ca-116">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="687ca-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ca-117">-Oferta</span><span class="sxs-lookup"><span data-stu-id="687ca-117">-Offer</span></span>
<span data-ttu-id="687ca-118">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="687ca-118">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ca-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="687ca-119">-Publisher</span></span>
<span data-ttu-id="687ca-120">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="687ca-120">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ca-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="687ca-121">-ResourceId</span></span>
<span data-ttu-id="687ca-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="687ca-122">The resource id.</span></span>

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

### <span data-ttu-id="687ca-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="687ca-123">-Sku</span></span>
<span data-ttu-id="687ca-124">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="687ca-124">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ca-125">-Versão</span><span class="sxs-lookup"><span data-stu-id="687ca-125">-Version</span></span>
<span data-ttu-id="687ca-126">A versão da imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="687ca-126">The version of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ca-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="687ca-127">-Confirm</span></span>
<span data-ttu-id="687ca-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="687ca-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="687ca-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="687ca-129">-WhatIf</span></span>
<span data-ttu-id="687ca-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="687ca-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="687ca-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="687ca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="687ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687ca-132">CommonParameters</span></span>
<span data-ttu-id="687ca-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="687ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687ca-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="687ca-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687ca-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="687ca-135">INPUTS</span></span>

## <span data-ttu-id="687ca-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="687ca-136">OUTPUTS</span></span>

## <span data-ttu-id="687ca-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="687ca-137">NOTES</span></span>

## <span data-ttu-id="687ca-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="687ca-138">RELATED LINKS</span></span>

