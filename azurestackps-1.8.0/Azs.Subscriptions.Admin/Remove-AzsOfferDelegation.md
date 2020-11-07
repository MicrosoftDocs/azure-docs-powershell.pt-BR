---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774750"
---
# <span data-ttu-id="a912e-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a912e-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="a912e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a912e-102">SYNOPSIS</span></span>
<span data-ttu-id="a912e-103">Remove a delegação de oferta</span><span class="sxs-lookup"><span data-stu-id="a912e-103">Removes the offer delegation</span></span>

## <span data-ttu-id="a912e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a912e-104">SYNTAX</span></span>

### <span data-ttu-id="a912e-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="a912e-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a912e-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="a912e-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a912e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a912e-107">DESCRIPTION</span></span>
<span data-ttu-id="a912e-108">Remove a delegação de oferta</span><span class="sxs-lookup"><span data-stu-id="a912e-108">Removes the offer delegation</span></span>

## <span data-ttu-id="a912e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a912e-109">EXAMPLES</span></span>

### <span data-ttu-id="a912e-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a912e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="a912e-111">Remove a delegação de oferta</span><span class="sxs-lookup"><span data-stu-id="a912e-111">Removes the offer delegation</span></span>

## <span data-ttu-id="a912e-112">OS</span><span class="sxs-lookup"><span data-stu-id="a912e-112">PARAMETERS</span></span>

### <span data-ttu-id="a912e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a912e-113">-Force</span></span>
<span data-ttu-id="a912e-114">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="a912e-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="a912e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a912e-115">-Name</span></span>
<span data-ttu-id="a912e-116">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="a912e-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="a912e-117">-Offername</span><span class="sxs-lookup"><span data-stu-id="a912e-117">-OfferName</span></span>
<span data-ttu-id="a912e-118">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="a912e-118">Name of an offer.</span></span>

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

### <span data-ttu-id="a912e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a912e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a912e-120">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="a912e-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a912e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a912e-121">-ResourceId</span></span>
<span data-ttu-id="a912e-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a912e-122">The resource id.</span></span>

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

### <span data-ttu-id="a912e-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a912e-123">-Confirm</span></span>
<span data-ttu-id="a912e-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a912e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a912e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a912e-125">-WhatIf</span></span>
<span data-ttu-id="a912e-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a912e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a912e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a912e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a912e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a912e-128">CommonParameters</span></span>
<span data-ttu-id="a912e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a912e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a912e-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a912e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a912e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a912e-131">INPUTS</span></span>

## <span data-ttu-id="a912e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a912e-132">OUTPUTS</span></span>

## <span data-ttu-id="a912e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a912e-133">NOTES</span></span>

## <span data-ttu-id="a912e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a912e-134">RELATED LINKS</span></span>

