---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426220"
---
# <span data-ttu-id="49296-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="49296-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="49296-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49296-102">SYNOPSIS</span></span>
<span data-ttu-id="49296-103">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="49296-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="49296-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49296-104">SYNTAX</span></span>

### <span data-ttu-id="49296-105">Definir (padrão)</span><span class="sxs-lookup"><span data-stu-id="49296-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49296-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="49296-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49296-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="49296-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49296-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49296-108">DESCRIPTION</span></span>
<span data-ttu-id="49296-109">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="49296-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="49296-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49296-110">EXAMPLES</span></span>

### <span data-ttu-id="49296-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="49296-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="49296-112">Criar ou atualizar uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="49296-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="49296-113">OS</span><span class="sxs-lookup"><span data-stu-id="49296-113">PARAMETERS</span></span>

### <span data-ttu-id="49296-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49296-114">-DisplayName</span></span>
<span data-ttu-id="49296-115">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="49296-115">Subscription name.</span></span>

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

### <span data-ttu-id="49296-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49296-116">-InputObject</span></span>
<span data-ttu-id="49296-117">Posbbily cota de rede modificada retornada por Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="49296-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="49296-118">-Local</span><span class="sxs-lookup"><span data-stu-id="49296-118">-Location</span></span>
<span data-ttu-id="49296-119">Local onde o recurso é local.</span><span class="sxs-lookup"><span data-stu-id="49296-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="49296-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="49296-120">-OfferId</span></span>
<span data-ttu-id="49296-121">Identificador da oferta sob o escopo de um provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="49296-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="49296-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49296-122">-ResourceId</span></span>
<span data-ttu-id="49296-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="49296-123">The resource ID.</span></span>

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

### <span data-ttu-id="49296-124">-Estado</span><span class="sxs-lookup"><span data-stu-id="49296-124">-State</span></span>
<span data-ttu-id="49296-125">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="49296-125">Subscription state.</span></span>

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

### <span data-ttu-id="49296-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49296-126">-SubscriptionId</span></span>
<span data-ttu-id="49296-127">Identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="49296-127">Subscription identifier.</span></span>

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

### <span data-ttu-id="49296-128">-Marcas</span><span class="sxs-lookup"><span data-stu-id="49296-128">-Tags</span></span>
<span data-ttu-id="49296-129">Lista de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="49296-129">List of key-value pairs.</span></span>

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

### <span data-ttu-id="49296-130">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="49296-130">-TenantId</span></span>
<span data-ttu-id="49296-131">Identificador de locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="49296-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="49296-132">-Digite</span><span class="sxs-lookup"><span data-stu-id="49296-132">-Type</span></span>
<span data-ttu-id="49296-133">Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="49296-133">Type of resource.</span></span>

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

### <span data-ttu-id="49296-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="49296-134">-Confirm</span></span>
<span data-ttu-id="49296-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49296-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49296-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49296-136">-WhatIf</span></span>
<span data-ttu-id="49296-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49296-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49296-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49296-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49296-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49296-139">CommonParameters</span></span>
<span data-ttu-id="49296-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49296-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49296-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49296-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49296-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49296-142">INPUTS</span></span>

## <span data-ttu-id="49296-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49296-143">OUTPUTS</span></span>

### <span data-ttu-id="49296-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="49296-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="49296-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49296-145">NOTES</span></span>

## <span data-ttu-id="49296-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49296-146">RELATED LINKS</span></span>

