---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e501feeea3509725b53c85007934c8e682de48a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774158"
---
# <span data-ttu-id="53507-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="53507-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="53507-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53507-102">SYNOPSIS</span></span>
<span data-ttu-id="53507-103">Vincula um plano a uma oferta.</span><span class="sxs-lookup"><span data-stu-id="53507-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="53507-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53507-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53507-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53507-105">DESCRIPTION</span></span>
<span data-ttu-id="53507-106">Vincula um plano a uma oferta.</span><span class="sxs-lookup"><span data-stu-id="53507-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="53507-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53507-107">EXAMPLES</span></span>

### <span data-ttu-id="53507-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="53507-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="53507-109">OS</span><span class="sxs-lookup"><span data-stu-id="53507-109">PARAMETERS</span></span>

### <span data-ttu-id="53507-110">-Force</span><span class="sxs-lookup"><span data-stu-id="53507-110">-Force</span></span>
<span data-ttu-id="53507-111">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="53507-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="53507-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="53507-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="53507-113">A contagem máxima de aquisições por assinantes</span><span class="sxs-lookup"><span data-stu-id="53507-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53507-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="53507-114">-OfferName</span></span>
<span data-ttu-id="53507-115">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="53507-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53507-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="53507-116">-PlanLinkType</span></span>
<span data-ttu-id="53507-117">Tipo do link do plano.</span><span class="sxs-lookup"><span data-stu-id="53507-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53507-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="53507-118">-PlanName</span></span>
<span data-ttu-id="53507-119">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="53507-119">Name of the plan.</span></span>

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

### <span data-ttu-id="53507-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53507-120">-ResourceGroupName</span></span>
<span data-ttu-id="53507-121">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="53507-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53507-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53507-122">-Confirm</span></span>
<span data-ttu-id="53507-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53507-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53507-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53507-124">-WhatIf</span></span>
<span data-ttu-id="53507-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53507-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53507-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53507-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53507-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53507-127">CommonParameters</span></span>
<span data-ttu-id="53507-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53507-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53507-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53507-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53507-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53507-130">INPUTS</span></span>

## <span data-ttu-id="53507-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53507-131">OUTPUTS</span></span>

## <span data-ttu-id="53507-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53507-132">NOTES</span></span>

## <span data-ttu-id="53507-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53507-133">RELATED LINKS</span></span>

