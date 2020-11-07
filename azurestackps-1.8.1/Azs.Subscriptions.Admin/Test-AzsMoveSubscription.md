---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774889"
---
# <span data-ttu-id="82647-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="82647-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="82647-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82647-102">SYNOPSIS</span></span>
<span data-ttu-id="82647-103">Valide se as assinaturas do usuário podem ser movidas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="82647-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="82647-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82647-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="82647-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82647-105">DESCRIPTION</span></span>
<span data-ttu-id="82647-106">Valide se as assinaturas do usuário podem ser movidas entre ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="82647-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="82647-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82647-107">EXAMPLES</span></span>

### <span data-ttu-id="82647-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="82647-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="82647-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"-ResourceId "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.subscriptions.admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="82647-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="82647-110">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="82647-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="82647-111">$resourceIds = Get-AzsUserSubscription-Filter "offername EQ ' O1 '" | Selecione-ExpandProperty ID Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="82647-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="82647-112">OS</span><span class="sxs-lookup"><span data-stu-id="82647-112">PARAMETERS</span></span>

### <span data-ttu-id="82647-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82647-113">-AsJob</span></span>
<span data-ttu-id="82647-114">Especifica se a operação de movimentação deve ser executada como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="82647-114">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="82647-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="82647-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="82647-116">Especifica a oferta do provedor delegado totalmente qualificado na qual esse cmdlet Move assinaturas.</span><span class="sxs-lookup"><span data-stu-id="82647-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="82647-117">NULO se as assinaturas forem removidas para o provedor padrão.</span><span class="sxs-lookup"><span data-stu-id="82647-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="82647-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82647-118">-ResourceId</span></span>
<span data-ttu-id="82647-119">Especifica uma matriz de identificadores de recursos de assinatura totalmente qualificados que esse cmdlet Move.</span><span class="sxs-lookup"><span data-stu-id="82647-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="82647-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82647-120">CommonParameters</span></span>
<span data-ttu-id="82647-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82647-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82647-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82647-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82647-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82647-123">INPUTS</span></span>

## <span data-ttu-id="82647-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82647-124">OUTPUTS</span></span>

## <span data-ttu-id="82647-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82647-125">NOTES</span></span>

## <span data-ttu-id="82647-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82647-126">RELATED LINKS</span></span>

