---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9212655ecb5f67dbf459548c48ff6d25420a8537
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601716"
---
# <span data-ttu-id="88e12-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="88e12-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="88e12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88e12-102">SYNOPSIS</span></span>
<span data-ttu-id="88e12-103">Desvincular um plano de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="88e12-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="88e12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88e12-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e12-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88e12-105">DESCRIPTION</span></span>
<span data-ttu-id="88e12-106">Desvincular um plano de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="88e12-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="88e12-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88e12-107">EXAMPLES</span></span>

### <span data-ttu-id="88e12-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="88e12-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="88e12-109">OS</span><span class="sxs-lookup"><span data-stu-id="88e12-109">PARAMETERS</span></span>

### <span data-ttu-id="88e12-110">-Force</span><span class="sxs-lookup"><span data-stu-id="88e12-110">-Force</span></span>
<span data-ttu-id="88e12-111">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="88e12-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="88e12-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="88e12-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="88e12-113">A contagem máxima de aquisições por assinantes</span><span class="sxs-lookup"><span data-stu-id="88e12-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="88e12-114">-Offername</span><span class="sxs-lookup"><span data-stu-id="88e12-114">-OfferName</span></span>
<span data-ttu-id="88e12-115">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="88e12-115">Name of an offer.</span></span>

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

### <span data-ttu-id="88e12-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="88e12-116">-PlanLinkType</span></span>
<span data-ttu-id="88e12-117">Tipo do link do plano.</span><span class="sxs-lookup"><span data-stu-id="88e12-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="88e12-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="88e12-118">-PlanName</span></span>
<span data-ttu-id="88e12-119">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="88e12-119">Name of the plan.</span></span>

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

### <span data-ttu-id="88e12-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e12-120">-ResourceGroupName</span></span>
<span data-ttu-id="88e12-121">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="88e12-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="88e12-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88e12-122">-Confirm</span></span>
<span data-ttu-id="88e12-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e12-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e12-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e12-124">-WhatIf</span></span>
<span data-ttu-id="88e12-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88e12-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e12-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88e12-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e12-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e12-127">CommonParameters</span></span>
<span data-ttu-id="88e12-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e12-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e12-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e12-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e12-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88e12-130">INPUTS</span></span>

## <span data-ttu-id="88e12-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88e12-131">OUTPUTS</span></span>

## <span data-ttu-id="88e12-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88e12-132">NOTES</span></span>

## <span data-ttu-id="88e12-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88e12-133">RELATED LINKS</span></span>

