---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774766"
---
# <span data-ttu-id="542bf-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="542bf-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="542bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="542bf-102">SYNOPSIS</span></span>
<span data-ttu-id="542bf-103">Mover assinaturas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="542bf-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="542bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="542bf-104">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="542bf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="542bf-105">DESCRIPTION</span></span>
<span data-ttu-id="542bf-106">Mover assinaturas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="542bf-106">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="542bf-107">Esse processo executará apenas uma remarcação, a oferta subjacente, planos, as cotas para as assinaturas não serão alteradas.</span><span class="sxs-lookup"><span data-stu-id="542bf-107">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="542bf-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="542bf-108">EXAMPLES</span></span>

### <span data-ttu-id="542bf-109">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="542bf-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="542bf-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="542bf-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="542bf-111">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="542bf-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="542bf-112">$resourceIds = Get-AzsUserSubscription-Filter "offername EQ ' O1 '" | em que {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select-ExpandProperty ID Move-AzsSubscription-ResourceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="542bf-112">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="542bf-113">OS</span><span class="sxs-lookup"><span data-stu-id="542bf-113">PARAMETERS</span></span>

### <span data-ttu-id="542bf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="542bf-114">-AsJob</span></span>
<span data-ttu-id="542bf-115">Especifica se a operação de movimentação deve ser executada como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="542bf-115">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="542bf-116">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="542bf-116">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="542bf-117">Especifica a oferta do provedor delegado totalmente qualificado na qual esse cmdlet Move assinaturas.</span><span class="sxs-lookup"><span data-stu-id="542bf-117">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="542bf-118">NULO se as assinaturas forem removidas para o provedor padrão.</span><span class="sxs-lookup"><span data-stu-id="542bf-118">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="542bf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="542bf-119">-ResourceId</span></span>
<span data-ttu-id="542bf-120">Especifica uma matriz de identificadores de recursos de assinatura totalmente qualificados que esse cmdlet Move.</span><span class="sxs-lookup"><span data-stu-id="542bf-120">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="542bf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542bf-121">CommonParameters</span></span>
<span data-ttu-id="542bf-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542bf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542bf-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542bf-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542bf-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="542bf-124">INPUTS</span></span>

## <span data-ttu-id="542bf-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="542bf-125">OUTPUTS</span></span>

## <span data-ttu-id="542bf-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="542bf-126">NOTES</span></span>

## <span data-ttu-id="542bf-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="542bf-127">RELATED LINKS</span></span>

