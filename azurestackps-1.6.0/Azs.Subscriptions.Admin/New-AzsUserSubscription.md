---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 33544da0c95e6b53da2a0dc189ca0dfe538da270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425691"
---
# <span data-ttu-id="75cfa-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="75cfa-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="75cfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="75cfa-103">Criar uma nova assinatura.</span><span class="sxs-lookup"><span data-stu-id="75cfa-103">Create a new subscription.</span></span>

## <span data-ttu-id="75cfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75cfa-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75cfa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75cfa-105">DESCRIPTION</span></span>
<span data-ttu-id="75cfa-106">Criar uma nova assinatura.</span><span class="sxs-lookup"><span data-stu-id="75cfa-106">Create a new subscription.</span></span>

## <span data-ttu-id="75cfa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75cfa-107">EXAMPLES</span></span>

### <span data-ttu-id="75cfa-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="75cfa-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="75cfa-109">Cria uma nova assinatura de usuário</span><span class="sxs-lookup"><span data-stu-id="75cfa-109">Creates a new user subscription</span></span>

## <span data-ttu-id="75cfa-110">OS</span><span class="sxs-lookup"><span data-stu-id="75cfa-110">PARAMETERS</span></span>

### <span data-ttu-id="75cfa-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75cfa-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="75cfa-112">Identificador de assinatura do DelegatedProvider pai.</span><span class="sxs-lookup"><span data-stu-id="75cfa-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cfa-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="75cfa-113">-DisplayName</span></span>
<span data-ttu-id="75cfa-114">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="75cfa-114">Subscription name.</span></span>

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

### <span data-ttu-id="75cfa-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="75cfa-115">-ExternalReferenceId</span></span>
<span data-ttu-id="75cfa-116">Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="75cfa-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cfa-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="75cfa-117">-OfferId</span></span>
<span data-ttu-id="75cfa-118">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="75cfa-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="75cfa-119">-Proprietário</span><span class="sxs-lookup"><span data-stu-id="75cfa-119">-Owner</span></span>
<span data-ttu-id="75cfa-120">Proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="75cfa-120">Subscription owner.</span></span>

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

### <span data-ttu-id="75cfa-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="75cfa-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="75cfa-122">Tipo de Gerenciador de recursos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="75cfa-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cfa-123">-Estado</span><span class="sxs-lookup"><span data-stu-id="75cfa-123">-State</span></span>
<span data-ttu-id="75cfa-124">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="75cfa-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cfa-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75cfa-125">-SubscriptionId</span></span>
<span data-ttu-id="75cfa-126">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="75cfa-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cfa-127">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="75cfa-127">-TenantId</span></span>
<span data-ttu-id="75cfa-128">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="75cfa-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="75cfa-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75cfa-129">-Confirm</span></span>
<span data-ttu-id="75cfa-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75cfa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75cfa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75cfa-131">-WhatIf</span></span>
<span data-ttu-id="75cfa-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75cfa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75cfa-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75cfa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75cfa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cfa-134">CommonParameters</span></span>
<span data-ttu-id="75cfa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cfa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cfa-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75cfa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cfa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75cfa-137">INPUTS</span></span>

## <span data-ttu-id="75cfa-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75cfa-138">OUTPUTS</span></span>

### <span data-ttu-id="75cfa-139">Microsoft. AzureStack. Management. inscrições. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="75cfa-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="75cfa-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75cfa-140">NOTES</span></span>

## <span data-ttu-id="75cfa-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75cfa-141">RELATED LINKS</span></span>
