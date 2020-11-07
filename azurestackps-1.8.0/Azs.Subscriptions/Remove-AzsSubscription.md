---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774730"
---
# <span data-ttu-id="4ff8c-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="4ff8c-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="4ff8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ff8c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff8c-103">Exclua a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="4ff8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ff8c-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ff8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ff8c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ff8c-106">Exclua a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="4ff8c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ff8c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ff8c-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="4ff8c-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="4ff8c-109">Exclua a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="4ff8c-110">OS</span><span class="sxs-lookup"><span data-stu-id="4ff8c-110">PARAMETERS</span></span>

### <span data-ttu-id="4ff8c-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ff8c-111">-SubscriptionId</span></span>
<span data-ttu-id="4ff8c-112">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="4ff8c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4ff8c-113">-Force</span></span>
<span data-ttu-id="4ff8c-114">Remover assinatura sem solicitação</span><span class="sxs-lookup"><span data-stu-id="4ff8c-114">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="4ff8c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ff8c-115">-WhatIf</span></span>
<span data-ttu-id="4ff8c-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ff8c-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ff8c-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ff8c-118">-Confirm</span></span>
<span data-ttu-id="4ff8c-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ff8c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff8c-120">CommonParameters</span></span>
<span data-ttu-id="4ff8c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff8c-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ff8c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff8c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ff8c-123">INPUTS</span></span>

## <span data-ttu-id="4ff8c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ff8c-124">OUTPUTS</span></span>

## <span data-ttu-id="4ff8c-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ff8c-125">NOTES</span></span>

## <span data-ttu-id="4ff8c-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ff8c-126">RELATED LINKS</span></span>
