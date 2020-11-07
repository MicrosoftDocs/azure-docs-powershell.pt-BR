---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775040"
---
# <span data-ttu-id="9f6e4-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="9f6e4-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="9f6e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6e4-103">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="9f6e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f6e4-104">SYNTAX</span></span>

### <span data-ttu-id="9f6e4-105">Definir (padrão)</span><span class="sxs-lookup"><span data-stu-id="9f6e4-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f6e4-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="9f6e4-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f6e4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9f6e4-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6e4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f6e4-108">DESCRIPTION</span></span>
<span data-ttu-id="9f6e4-109">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="9f6e4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f6e4-110">EXAMPLES</span></span>

### <span data-ttu-id="9f6e4-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="9f6e4-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="9f6e4-112">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="9f6e4-113">OS</span><span class="sxs-lookup"><span data-stu-id="9f6e4-113">PARAMETERS</span></span>

### <span data-ttu-id="9f6e4-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="9f6e4-114">-OfferId</span></span>
<span data-ttu-id="9f6e4-115">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="9f6e4-116">-Digite</span><span class="sxs-lookup"><span data-stu-id="9f6e4-116">-Type</span></span>
<span data-ttu-id="9f6e4-117">Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-117">Type of resource.</span></span>

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

### <span data-ttu-id="9f6e4-118">-Marcas</span><span class="sxs-lookup"><span data-stu-id="9f6e4-118">-Tags</span></span>
<span data-ttu-id="9f6e4-119">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-119">List of key-value pairs.</span></span>

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

### <span data-ttu-id="9f6e4-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f6e4-120">-SubscriptionId</span></span>
<span data-ttu-id="9f6e4-121">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-121">Subscription identifier.</span></span>

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

### <span data-ttu-id="9f6e4-122">-Estado</span><span class="sxs-lookup"><span data-stu-id="9f6e4-122">-State</span></span>
<span data-ttu-id="9f6e4-123">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-123">Subscription state.</span></span>

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

### <span data-ttu-id="9f6e4-124">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="9f6e4-124">-TenantId</span></span>
<span data-ttu-id="9f6e4-125">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="9f6e4-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9f6e4-126">-DisplayName</span></span>
<span data-ttu-id="9f6e4-127">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-127">Subscription name.</span></span>

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

### <span data-ttu-id="9f6e4-128">-Local</span><span class="sxs-lookup"><span data-stu-id="9f6e4-128">-Location</span></span>
<span data-ttu-id="9f6e4-129">Local onde o recurso é local.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="9f6e4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f6e4-130">-ResourceId</span></span>
<span data-ttu-id="9f6e4-131">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-131">The resource ID.</span></span>

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

### <span data-ttu-id="9f6e4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f6e4-132">-InputObject</span></span>
<span data-ttu-id="9f6e4-133">Posbbily cota de rede modificada retornada por Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="9f6e4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6e4-134">-WhatIf</span></span>
<span data-ttu-id="9f6e4-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f6e4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f6e4-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9f6e4-137">-Confirm</span></span>
<span data-ttu-id="9f6e4-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f6e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6e4-139">CommonParameters</span></span>
<span data-ttu-id="9f6e4-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6e4-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6e4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6e4-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f6e4-142">INPUTS</span></span>

## <span data-ttu-id="9f6e4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f6e4-143">OUTPUTS</span></span>

### <span data-ttu-id="9f6e4-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="9f6e4-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="9f6e4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f6e4-145">NOTES</span></span>

## <span data-ttu-id="9f6e4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f6e4-146">RELATED LINKS</span></span>
