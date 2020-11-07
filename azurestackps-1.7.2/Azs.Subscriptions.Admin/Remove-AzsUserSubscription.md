---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774330"
---
# <span data-ttu-id="faec2-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="faec2-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="faec2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="faec2-102">SYNOPSIS</span></span>
<span data-ttu-id="faec2-103">Remove a assinatura de locatário especificada.</span><span class="sxs-lookup"><span data-stu-id="faec2-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="faec2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="faec2-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faec2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="faec2-105">DESCRIPTION</span></span>
<span data-ttu-id="faec2-106">Remove a assinatura de locatário especificada.</span><span class="sxs-lookup"><span data-stu-id="faec2-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="faec2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="faec2-107">EXAMPLES</span></span>

### <span data-ttu-id="faec2-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="faec2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="faec2-109">Remover a assinatura de locatário especificada.</span><span class="sxs-lookup"><span data-stu-id="faec2-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="faec2-110">OS</span><span class="sxs-lookup"><span data-stu-id="faec2-110">PARAMETERS</span></span>

### <span data-ttu-id="faec2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="faec2-111">-Force</span></span>
<span data-ttu-id="faec2-112">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="faec2-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="faec2-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="faec2-113">-SubscriptionId</span></span>
<span data-ttu-id="faec2-114">Parâmetro ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="faec2-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faec2-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="faec2-115">-Confirm</span></span>
<span data-ttu-id="faec2-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faec2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faec2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faec2-117">-WhatIf</span></span>
<span data-ttu-id="faec2-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="faec2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faec2-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="faec2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faec2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faec2-120">CommonParameters</span></span>
<span data-ttu-id="faec2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faec2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faec2-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faec2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faec2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="faec2-123">INPUTS</span></span>

## <span data-ttu-id="faec2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="faec2-124">OUTPUTS</span></span>

## <span data-ttu-id="faec2-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="faec2-125">NOTES</span></span>

## <span data-ttu-id="faec2-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="faec2-126">RELATED LINKS</span></span>

