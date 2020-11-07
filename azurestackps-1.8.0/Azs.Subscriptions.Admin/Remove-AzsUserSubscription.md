---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25411a71a6d8233be55ab25ac99487da0b44bd0b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774575"
---
# <span data-ttu-id="41215-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="41215-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="41215-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41215-102">SYNOPSIS</span></span>
<span data-ttu-id="41215-103">Remove a assinatura de locatário especificada.</span><span class="sxs-lookup"><span data-stu-id="41215-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="41215-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41215-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41215-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41215-105">DESCRIPTION</span></span>
<span data-ttu-id="41215-106">Remove a assinatura de locatário especificada.</span><span class="sxs-lookup"><span data-stu-id="41215-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="41215-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41215-107">EXAMPLES</span></span>

### <span data-ttu-id="41215-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41215-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="41215-109">Remover a assinatura de locatário especificada.</span><span class="sxs-lookup"><span data-stu-id="41215-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="41215-110">OS</span><span class="sxs-lookup"><span data-stu-id="41215-110">PARAMETERS</span></span>

### <span data-ttu-id="41215-111">-Force</span><span class="sxs-lookup"><span data-stu-id="41215-111">-Force</span></span>
<span data-ttu-id="41215-112">Sinalizador para remover o item sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="41215-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="41215-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41215-113">-SubscriptionId</span></span>
<span data-ttu-id="41215-114">Parâmetro ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="41215-114">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="41215-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41215-115">-Confirm</span></span>
<span data-ttu-id="41215-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41215-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41215-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41215-117">-WhatIf</span></span>
<span data-ttu-id="41215-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41215-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41215-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41215-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41215-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41215-120">CommonParameters</span></span>
<span data-ttu-id="41215-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41215-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41215-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41215-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41215-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41215-123">INPUTS</span></span>

## <span data-ttu-id="41215-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41215-124">OUTPUTS</span></span>

## <span data-ttu-id="41215-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41215-125">NOTES</span></span>

## <span data-ttu-id="41215-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41215-126">RELATED LINKS</span></span>

