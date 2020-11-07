---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7d51bef12f0f7808aff3fda819ac614e0bb1c9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774872"
---
# <span data-ttu-id="6c0b1-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="6c0b1-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="6c0b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0b1-103">Vincula um plano a uma oferta.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="6c0b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c0b1-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c0b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c0b1-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0b1-106">Vincula um plano a uma oferta.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="6c0b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c0b1-107">EXAMPLES</span></span>

### <span data-ttu-id="6c0b1-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6c0b1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="6c0b1-109">OS</span><span class="sxs-lookup"><span data-stu-id="6c0b1-109">PARAMETERS</span></span>

### <span data-ttu-id="6c0b1-110">-Force</span><span class="sxs-lookup"><span data-stu-id="6c0b1-110">-Force</span></span>
<span data-ttu-id="6c0b1-111">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="6c0b1-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="6c0b1-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="6c0b1-113">A contagem máxima de aquisições por assinantes</span><span class="sxs-lookup"><span data-stu-id="6c0b1-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="6c0b1-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="6c0b1-114">-OfferName</span></span>
<span data-ttu-id="6c0b1-115">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-115">Name of an offer.</span></span>

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

### <span data-ttu-id="6c0b1-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="6c0b1-116">-PlanLinkType</span></span>
<span data-ttu-id="6c0b1-117">Tipo do link do plano.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="6c0b1-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6c0b1-118">-PlanName</span></span>
<span data-ttu-id="6c0b1-119">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-119">Name of the plan.</span></span>

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

### <span data-ttu-id="6c0b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c0b1-121">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6c0b1-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c0b1-122">-Confirm</span></span>
<span data-ttu-id="6c0b1-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0b1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0b1-124">-WhatIf</span></span>
<span data-ttu-id="6c0b1-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0b1-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0b1-127">CommonParameters</span></span>
<span data-ttu-id="6c0b1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c0b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0b1-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0b1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0b1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c0b1-130">INPUTS</span></span>

## <span data-ttu-id="6c0b1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c0b1-131">OUTPUTS</span></span>

## <span data-ttu-id="6c0b1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c0b1-132">NOTES</span></span>

## <span data-ttu-id="6c0b1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c0b1-133">RELATED LINKS</span></span>

