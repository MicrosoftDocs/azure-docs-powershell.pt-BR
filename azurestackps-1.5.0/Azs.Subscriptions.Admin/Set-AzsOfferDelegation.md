---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e0c752c3ffd266a3615fdd5a1f5193e0202b29a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425768"
---
# <span data-ttu-id="5848f-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="5848f-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="5848f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5848f-102">SYNOPSIS</span></span>
<span data-ttu-id="5848f-103">Atualiza a delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="5848f-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="5848f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5848f-104">SYNTAX</span></span>

### <span data-ttu-id="5848f-105">Atualização (padrão)</span><span class="sxs-lookup"><span data-stu-id="5848f-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5848f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5848f-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5848f-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="5848f-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5848f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5848f-108">DESCRIPTION</span></span>
<span data-ttu-id="5848f-109">Atualiza a delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="5848f-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="5848f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5848f-110">EXAMPLES</span></span>

### <span data-ttu-id="5848f-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5848f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="5848f-112">Atualiza a delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="5848f-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="5848f-113">OS</span><span class="sxs-lookup"><span data-stu-id="5848f-113">PARAMETERS</span></span>

### <span data-ttu-id="5848f-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5848f-114">-InputObject</span></span>
<span data-ttu-id="5848f-115">O objeto de entrada do tipo Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation.</span><span class="sxs-lookup"><span data-stu-id="5848f-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5848f-116">-Local</span><span class="sxs-lookup"><span data-stu-id="5848f-116">-Location</span></span>
<span data-ttu-id="5848f-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="5848f-117">Location of the resource.</span></span>

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

### <span data-ttu-id="5848f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5848f-118">-Name</span></span>
<span data-ttu-id="5848f-119">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="5848f-119">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5848f-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="5848f-120">-OfferName</span></span>
<span data-ttu-id="5848f-121">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="5848f-121">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5848f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5848f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5848f-123">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="5848f-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5848f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5848f-124">-ResourceId</span></span>
<span data-ttu-id="5848f-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="5848f-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5848f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5848f-126">-SubscriptionId</span></span>
<span data-ttu-id="5848f-127">Identificador da assinatura que recebe a oferta delegada.</span><span class="sxs-lookup"><span data-stu-id="5848f-127">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="5848f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5848f-128">-Confirm</span></span>
<span data-ttu-id="5848f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5848f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5848f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5848f-130">-WhatIf</span></span>
<span data-ttu-id="5848f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5848f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5848f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5848f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5848f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5848f-133">CommonParameters</span></span>
<span data-ttu-id="5848f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5848f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5848f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5848f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5848f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5848f-136">INPUTS</span></span>

## <span data-ttu-id="5848f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5848f-137">OUTPUTS</span></span>

### <span data-ttu-id="5848f-138">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="5848f-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="5848f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5848f-139">NOTES</span></span>

## <span data-ttu-id="5848f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5848f-140">RELATED LINKS</span></span>

