---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f415da1d6f9bb086d796c0c1bf191282c2880a09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601692"
---
# <span data-ttu-id="a20b0-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="a20b0-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="a20b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a20b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a20b0-103">Mover assinaturas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="a20b0-103">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="a20b0-104">Esse processo executará apenas uma remarcação, a oferta subjacente, planos, as cotas para as assinaturas não serão alteradas.</span><span class="sxs-lookup"><span data-stu-id="a20b0-104">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="a20b0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a20b0-105">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="a20b0-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a20b0-106">DESCRIPTION</span></span>
<span data-ttu-id="a20b0-107">Mover assinaturas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="a20b0-107">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="a20b0-108">Esse processo executará apenas uma remarcação, a oferta subjacente, planos, as cotas para as assinaturas não serão alteradas.</span><span class="sxs-lookup"><span data-stu-id="a20b0-108">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="a20b0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a20b0-109">EXAMPLES</span></span>

### <span data-ttu-id="a20b0-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a20b0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="a20b0-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="a20b0-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="a20b0-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a20b0-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="a20b0-113">$resourceIds = Get-AzsUserSubscription-Filter "offername EQ ' O1 '" | em que {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select-ExpandProperty ID Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="a20b0-113">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="a20b0-114">OS</span><span class="sxs-lookup"><span data-stu-id="a20b0-114">PARAMETERS</span></span>

### <span data-ttu-id="a20b0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a20b0-115">-AsJob</span></span>
<span data-ttu-id="a20b0-116">Especifica se a operação de movimentação deve ser executada como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a20b0-116">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="a20b0-117">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="a20b0-117">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="a20b0-118">Especifica a oferta do provedor delegado totalmente qualificado na qual esse cmdlet Move assinaturas.</span><span class="sxs-lookup"><span data-stu-id="a20b0-118">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="a20b0-119">NULO se as assinaturas forem removidas para o provedor padrão.</span><span class="sxs-lookup"><span data-stu-id="a20b0-119">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20b0-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a20b0-120">-ResourceId</span></span>
<span data-ttu-id="a20b0-121">Especifica uma matriz de identificadores de recursos de assinatura totalmente qualificados que esse cmdlet Move.</span><span class="sxs-lookup"><span data-stu-id="a20b0-121">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20b0-122">CommonParameters</span></span>
<span data-ttu-id="a20b0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20b0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a20b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20b0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a20b0-125">INPUTS</span></span>

## <span data-ttu-id="a20b0-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a20b0-126">OUTPUTS</span></span>

## <span data-ttu-id="a20b0-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a20b0-127">NOTES</span></span>

## <span data-ttu-id="a20b0-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a20b0-128">RELATED LINKS</span></span>

