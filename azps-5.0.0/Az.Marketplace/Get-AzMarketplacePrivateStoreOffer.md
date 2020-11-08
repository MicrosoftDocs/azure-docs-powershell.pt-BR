---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117320"
---
# <span data-ttu-id="b9548-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="b9548-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="b9548-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9548-102">SYNOPSIS</span></span>
<span data-ttu-id="b9548-103">Obtenha uma ou mais ofertas de repositório particular.</span><span class="sxs-lookup"><span data-stu-id="b9548-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="b9548-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9548-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9548-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9548-105">DESCRIPTION</span></span>
<span data-ttu-id="b9548-106">Obtenha uma ou mais ofertas de repositório particular com planos públicos + privados que foram adicionados em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="b9548-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="b9548-107">Se a ID da assinatura for apresentada, obtenha uma ou mais ofertas da loja privada com planos particulares somente sob o escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="b9548-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="b9548-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9548-108">EXAMPLES</span></span>

### <span data-ttu-id="b9548-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9548-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="b9548-110">Obter ofertas de repositório particular com planos privados + públicos que foram adicionados em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="b9548-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="b9548-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b9548-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="b9548-112">Obter ofertas de repositório particular com planos particulares somente que foram adicionados sob o escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9548-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="b9548-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b9548-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="b9548-114">Obter a oferta da loja privada com planos privados + públicos que foram adicionados em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="b9548-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="b9548-115">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="b9548-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="b9548-116">Obtenha a oferta da loja privada com planos particulares somente que tenha sido adicionado em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="b9548-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="b9548-117">OS</span><span class="sxs-lookup"><span data-stu-id="b9548-117">PARAMETERS</span></span>

### <span data-ttu-id="b9548-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9548-118">-DefaultProfile</span></span>
<span data-ttu-id="b9548-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9548-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9548-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="b9548-120">-OfferId</span></span>
<span data-ttu-id="b9548-121">Oferta privateStore do Azure Marketplace necessária</span><span class="sxs-lookup"><span data-stu-id="b9548-121">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9548-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="b9548-122">-PrivateStoreId</span></span>
<span data-ttu-id="b9548-123">Ofertas de privateStore do Azure Marketplace necessárias</span><span class="sxs-lookup"><span data-stu-id="b9548-123">Required Azure Marketplace privateStore offers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9548-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9548-124">-SubscriptionId</span></span>
<span data-ttu-id="b9548-125">ID da assinatura do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="b9548-125">Azure Marketplace subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9548-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9548-126">CommonParameters</span></span>
<span data-ttu-id="b9548-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9548-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9548-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9548-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9548-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9548-129">INPUTS</span></span>

### <span data-ttu-id="b9548-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b9548-130">None</span></span>

## <span data-ttu-id="b9548-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9548-131">OUTPUTS</span></span>

### <span data-ttu-id="b9548-132">Microsoft. Azure. Commands. marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="b9548-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="b9548-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9548-133">NOTES</span></span>

## <span data-ttu-id="b9548-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9548-134">RELATED LINKS</span></span>
