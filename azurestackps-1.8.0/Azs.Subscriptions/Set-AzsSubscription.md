---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774563"
---
# <span data-ttu-id="f266d-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="f266d-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="f266d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f266d-102">SYNOPSIS</span></span>
<span data-ttu-id="f266d-103">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f266d-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="f266d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f266d-104">SYNTAX</span></span>

### <span data-ttu-id="f266d-105">Definir (padrão)</span><span class="sxs-lookup"><span data-stu-id="f266d-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f266d-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="f266d-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f266d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f266d-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f266d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f266d-108">DESCRIPTION</span></span>
<span data-ttu-id="f266d-109">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f266d-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="f266d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f266d-110">EXAMPLES</span></span>

### <span data-ttu-id="f266d-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="f266d-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="f266d-112">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f266d-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="f266d-113">OS</span><span class="sxs-lookup"><span data-stu-id="f266d-113">PARAMETERS</span></span>

### <span data-ttu-id="f266d-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="f266d-114">-OfferId</span></span>
<span data-ttu-id="f266d-115">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="f266d-115">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-116">-Digite</span><span class="sxs-lookup"><span data-stu-id="f266d-116">-Type</span></span>
<span data-ttu-id="f266d-117">Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f266d-117">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-118">-Marcas</span><span class="sxs-lookup"><span data-stu-id="f266d-118">-Tags</span></span>
<span data-ttu-id="f266d-119">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="f266d-119">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f266d-120">-SubscriptionId</span></span>
<span data-ttu-id="f266d-121">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="f266d-121">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-122">-Estado</span><span class="sxs-lookup"><span data-stu-id="f266d-122">-State</span></span>
<span data-ttu-id="f266d-123">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f266d-123">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-124">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="f266d-124">-TenantId</span></span>
<span data-ttu-id="f266d-125">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="f266d-125">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f266d-126">-DisplayName</span></span>
<span data-ttu-id="f266d-127">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f266d-127">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-128">-Local</span><span class="sxs-lookup"><span data-stu-id="f266d-128">-Location</span></span>
<span data-ttu-id="f266d-129">Local onde o recurso é local.</span><span class="sxs-lookup"><span data-stu-id="f266d-129">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f266d-130">-ResourceId</span></span>
<span data-ttu-id="f266d-131">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f266d-131">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f266d-132">-InputObject</span></span>
<span data-ttu-id="f266d-133">Posbbily cota de rede modificada retornada por Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="f266d-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f266d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f266d-134">-WhatIf</span></span>
<span data-ttu-id="f266d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f266d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f266d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f266d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f266d-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f266d-137">-Confirm</span></span>
<span data-ttu-id="f266d-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f266d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f266d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f266d-139">CommonParameters</span></span>
<span data-ttu-id="f266d-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f266d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f266d-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f266d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f266d-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f266d-142">INPUTS</span></span>

## <span data-ttu-id="f266d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f266d-143">OUTPUTS</span></span>

### <span data-ttu-id="f266d-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="f266d-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="f266d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f266d-145">NOTES</span></span>

## <span data-ttu-id="f266d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f266d-146">RELATED LINKS</span></span>
