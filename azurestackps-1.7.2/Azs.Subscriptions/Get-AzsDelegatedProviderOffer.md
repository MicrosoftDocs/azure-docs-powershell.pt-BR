---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8034887f8b44bef5c3dd59f73186027af1a1e5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774244"
---
# <span data-ttu-id="52f1b-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="52f1b-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="52f1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="52f1b-103">Obter a lista de ofertas para o provedor delegado especificado.</span><span class="sxs-lookup"><span data-stu-id="52f1b-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="52f1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52f1b-104">SYNTAX</span></span>

### <span data-ttu-id="52f1b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="52f1b-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="52f1b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="52f1b-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -Name <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="52f1b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52f1b-107">DESCRIPTION</span></span>
<span data-ttu-id="52f1b-108">Obter a lista de ofertas para o provedor delegado especificado.</span><span class="sxs-lookup"><span data-stu-id="52f1b-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="52f1b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52f1b-109">EXAMPLES</span></span>

### <span data-ttu-id="52f1b-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="52f1b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="52f1b-111">Obter a lista de ofertas para o provedor delegado especificado.</span><span class="sxs-lookup"><span data-stu-id="52f1b-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="52f1b-112">OS</span><span class="sxs-lookup"><span data-stu-id="52f1b-112">PARAMETERS</span></span>

### <span data-ttu-id="52f1b-113">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="52f1b-113">-DelegatedProviderId</span></span>
<span data-ttu-id="52f1b-114">ID do provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="52f1b-114">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f1b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="52f1b-115">-Name</span></span>
<span data-ttu-id="52f1b-116">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="52f1b-116">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: OfferName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f1b-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="52f1b-117">-Skip</span></span>
<span data-ttu-id="52f1b-118">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="52f1b-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f1b-119">-Início</span><span class="sxs-lookup"><span data-stu-id="52f1b-119">-Top</span></span>
<span data-ttu-id="52f1b-120">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="52f1b-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="52f1b-121">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="52f1b-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f1b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f1b-122">CommonParameters</span></span>
<span data-ttu-id="52f1b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f1b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f1b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f1b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f1b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52f1b-125">INPUTS</span></span>

## <span data-ttu-id="52f1b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52f1b-126">OUTPUTS</span></span>

### <span data-ttu-id="52f1b-127">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="52f1b-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="52f1b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52f1b-128">NOTES</span></span>

## <span data-ttu-id="52f1b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52f1b-129">RELATED LINKS</span></span>
