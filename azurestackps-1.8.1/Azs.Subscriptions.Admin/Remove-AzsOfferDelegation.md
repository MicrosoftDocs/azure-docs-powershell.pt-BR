---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774884"
---
# <span data-ttu-id="eb6f5-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="eb6f5-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="eb6f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6f5-103">Remove a delegação de oferta</span><span class="sxs-lookup"><span data-stu-id="eb6f5-103">Removes the offer delegation</span></span>

## <span data-ttu-id="eb6f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb6f5-104">SYNTAX</span></span>

### <span data-ttu-id="eb6f5-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb6f5-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb6f5-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="eb6f5-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb6f5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb6f5-107">DESCRIPTION</span></span>
<span data-ttu-id="eb6f5-108">Remove a delegação de oferta</span><span class="sxs-lookup"><span data-stu-id="eb6f5-108">Removes the offer delegation</span></span>

## <span data-ttu-id="eb6f5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb6f5-109">EXAMPLES</span></span>

### <span data-ttu-id="eb6f5-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb6f5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="eb6f5-111">Remove a delegação de oferta</span><span class="sxs-lookup"><span data-stu-id="eb6f5-111">Removes the offer delegation</span></span>

## <span data-ttu-id="eb6f5-112">OS</span><span class="sxs-lookup"><span data-stu-id="eb6f5-112">PARAMETERS</span></span>

### <span data-ttu-id="eb6f5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="eb6f5-113">-Force</span></span>
<span data-ttu-id="eb6f5-114">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="eb6f5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb6f5-115">-Name</span></span>
<span data-ttu-id="eb6f5-116">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="eb6f5-117">-Offername</span><span class="sxs-lookup"><span data-stu-id="eb6f5-117">-OfferName</span></span>
<span data-ttu-id="eb6f5-118">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-118">Name of an offer.</span></span>

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

### <span data-ttu-id="eb6f5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6f5-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb6f5-120">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="eb6f5-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb6f5-121">-ResourceId</span></span>
<span data-ttu-id="eb6f5-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-122">The resource id.</span></span>

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

### <span data-ttu-id="eb6f5-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eb6f5-123">-Confirm</span></span>
<span data-ttu-id="eb6f5-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb6f5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb6f5-125">-WhatIf</span></span>
<span data-ttu-id="eb6f5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb6f5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb6f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6f5-128">CommonParameters</span></span>
<span data-ttu-id="eb6f5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6f5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb6f5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6f5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb6f5-131">INPUTS</span></span>

## <span data-ttu-id="eb6f5-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb6f5-132">OUTPUTS</span></span>

## <span data-ttu-id="eb6f5-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb6f5-133">NOTES</span></span>

## <span data-ttu-id="eb6f5-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb6f5-134">RELATED LINKS</span></span>

