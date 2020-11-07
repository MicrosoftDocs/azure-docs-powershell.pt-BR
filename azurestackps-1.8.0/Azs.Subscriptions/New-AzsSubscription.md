---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774564"
---
# <span data-ttu-id="28e8b-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="28e8b-101">New-AzsSubscription</span></span>

## <span data-ttu-id="28e8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="28e8b-103">Criar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="28e8b-103">Create a subscription.</span></span>

## <span data-ttu-id="28e8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28e8b-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28e8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28e8b-105">DESCRIPTION</span></span>
<span data-ttu-id="28e8b-106">Criar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="28e8b-106">Create a subscription.</span></span>

## <span data-ttu-id="28e8b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28e8b-107">EXAMPLES</span></span>

### <span data-ttu-id="28e8b-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="28e8b-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="28e8b-109">Criar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="28e8b-109">Create a subscription.</span></span>

## <span data-ttu-id="28e8b-110">OS</span><span class="sxs-lookup"><span data-stu-id="28e8b-110">PARAMETERS</span></span>

### <span data-ttu-id="28e8b-111">-OfferId</span><span class="sxs-lookup"><span data-stu-id="28e8b-111">-OfferId</span></span>
<span data-ttu-id="28e8b-112">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="28e8b-112">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="28e8b-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="28e8b-113">-DisplayName</span></span>
<span data-ttu-id="28e8b-114">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="28e8b-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e8b-115">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="28e8b-115">-TenantId</span></span>
<span data-ttu-id="28e8b-116">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="28e8b-116">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e8b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28e8b-117">-SubscriptionId</span></span>
<span data-ttu-id="28e8b-118">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="28e8b-118">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e8b-119">-Estado</span><span class="sxs-lookup"><span data-stu-id="28e8b-119">-State</span></span>
<span data-ttu-id="28e8b-120">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="28e8b-120">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e8b-121">-Local</span><span class="sxs-lookup"><span data-stu-id="28e8b-121">-Location</span></span>
<span data-ttu-id="28e8b-122">Local onde o recurso é local.</span><span class="sxs-lookup"><span data-stu-id="28e8b-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e8b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e8b-123">-WhatIf</span></span>
<span data-ttu-id="28e8b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28e8b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28e8b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28e8b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28e8b-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28e8b-126">-Confirm</span></span>
<span data-ttu-id="28e8b-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28e8b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28e8b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e8b-128">CommonParameters</span></span>
<span data-ttu-id="28e8b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28e8b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e8b-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28e8b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e8b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28e8b-131">INPUTS</span></span>

## <span data-ttu-id="28e8b-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28e8b-132">OUTPUTS</span></span>

### <span data-ttu-id="28e8b-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="28e8b-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="28e8b-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28e8b-134">NOTES</span></span>

## <span data-ttu-id="28e8b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28e8b-135">RELATED LINKS</span></span>
