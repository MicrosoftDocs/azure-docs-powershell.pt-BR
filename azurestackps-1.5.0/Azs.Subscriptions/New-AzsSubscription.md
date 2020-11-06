---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425928"
---
# <span data-ttu-id="50444-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="50444-101">New-AzsSubscription</span></span>

## <span data-ttu-id="50444-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50444-102">SYNOPSIS</span></span>
<span data-ttu-id="50444-103">Criar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="50444-103">Create a subscription.</span></span>

## <span data-ttu-id="50444-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50444-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50444-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50444-105">DESCRIPTION</span></span>
<span data-ttu-id="50444-106">Criar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="50444-106">Create a subscription.</span></span>

## <span data-ttu-id="50444-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50444-107">EXAMPLES</span></span>

### <span data-ttu-id="50444-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="50444-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="50444-109">Criar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="50444-109">Create a subscription.</span></span>

## <span data-ttu-id="50444-110">OS</span><span class="sxs-lookup"><span data-stu-id="50444-110">PARAMETERS</span></span>

### <span data-ttu-id="50444-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50444-111">-DisplayName</span></span>
<span data-ttu-id="50444-112">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="50444-112">Subscription name.</span></span>

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

### <span data-ttu-id="50444-113">-Local</span><span class="sxs-lookup"><span data-stu-id="50444-113">-Location</span></span>
<span data-ttu-id="50444-114">Local onde o recurso é local.</span><span class="sxs-lookup"><span data-stu-id="50444-114">Location where resource is location.</span></span>

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

### <span data-ttu-id="50444-115">-OfferId</span><span class="sxs-lookup"><span data-stu-id="50444-115">-OfferId</span></span>
<span data-ttu-id="50444-116">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="50444-116">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="50444-117">-Estado</span><span class="sxs-lookup"><span data-stu-id="50444-117">-State</span></span>
<span data-ttu-id="50444-118">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="50444-118">Subscription state.</span></span>

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

### <span data-ttu-id="50444-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50444-119">-SubscriptionId</span></span>
<span data-ttu-id="50444-120">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="50444-120">Subscription identifier.</span></span>

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

### <span data-ttu-id="50444-121">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="50444-121">-TenantId</span></span>
<span data-ttu-id="50444-122">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="50444-122">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="50444-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="50444-123">-Confirm</span></span>
<span data-ttu-id="50444-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50444-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50444-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50444-125">-WhatIf</span></span>
<span data-ttu-id="50444-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="50444-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50444-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="50444-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50444-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50444-128">CommonParameters</span></span>
<span data-ttu-id="50444-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50444-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50444-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50444-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50444-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50444-131">INPUTS</span></span>

## <span data-ttu-id="50444-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50444-132">OUTPUTS</span></span>

### <span data-ttu-id="50444-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="50444-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="50444-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50444-134">NOTES</span></span>

## <span data-ttu-id="50444-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50444-135">RELATED LINKS</span></span>
