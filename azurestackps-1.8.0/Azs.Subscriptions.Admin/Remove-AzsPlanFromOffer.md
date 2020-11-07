---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774749"
---
# <span data-ttu-id="33520-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="33520-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="33520-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33520-102">SYNOPSIS</span></span>
<span data-ttu-id="33520-103">Desvincular um plano de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="33520-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="33520-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33520-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33520-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33520-105">DESCRIPTION</span></span>
<span data-ttu-id="33520-106">Desvincular um plano de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="33520-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="33520-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33520-107">EXAMPLES</span></span>

### <span data-ttu-id="33520-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="33520-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="33520-109">OS</span><span class="sxs-lookup"><span data-stu-id="33520-109">PARAMETERS</span></span>

### <span data-ttu-id="33520-110">-Force</span><span class="sxs-lookup"><span data-stu-id="33520-110">-Force</span></span>
<span data-ttu-id="33520-111">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="33520-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="33520-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="33520-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="33520-113">A contagem máxima de aquisições por assinantes</span><span class="sxs-lookup"><span data-stu-id="33520-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33520-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="33520-114">-OfferName</span></span>
<span data-ttu-id="33520-115">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="33520-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33520-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="33520-116">-PlanLinkType</span></span>
<span data-ttu-id="33520-117">Tipo do link do plano.</span><span class="sxs-lookup"><span data-stu-id="33520-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33520-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="33520-118">-PlanName</span></span>
<span data-ttu-id="33520-119">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="33520-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33520-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33520-120">-ResourceGroupName</span></span>
<span data-ttu-id="33520-121">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="33520-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33520-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33520-122">-Confirm</span></span>
<span data-ttu-id="33520-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33520-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33520-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33520-124">-WhatIf</span></span>
<span data-ttu-id="33520-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33520-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33520-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33520-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33520-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33520-127">CommonParameters</span></span>
<span data-ttu-id="33520-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33520-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33520-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33520-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33520-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33520-130">INPUTS</span></span>

## <span data-ttu-id="33520-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33520-131">OUTPUTS</span></span>

## <span data-ttu-id="33520-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33520-132">NOTES</span></span>

## <span data-ttu-id="33520-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33520-133">RELATED LINKS</span></span>

