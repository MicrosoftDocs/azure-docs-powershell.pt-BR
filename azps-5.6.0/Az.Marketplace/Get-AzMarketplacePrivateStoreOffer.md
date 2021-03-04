---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 3c7356768db35ce2c21499db0a94402f040b5162
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892124"
---
# <span data-ttu-id="e6b7f-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="e6b7f-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="e6b7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b7f-103">Obter uma ou mais ofertas de loja privada.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="e6b7f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e6b7f-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b7f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e6b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b7f-106">Obter uma ou mais ofertas de loja privada com planos públicos + privados que foram adicionados no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="e6b7f-107">Se a ID da assinatura estiver presente, receba uma ou mais ofertas de loja privada com planos privados somente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="e6b7f-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="e6b7f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6b7f-108">EXAMPLES</span></span>

### <span data-ttu-id="e6b7f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e6b7f-109">Example 1</span></span>
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

<span data-ttu-id="e6b7f-110">Obter ofertas de loja privada com planos privados + públicos que foram adicionados no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="e6b7f-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e6b7f-111">Example 2</span></span>
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

<span data-ttu-id="e6b7f-112">Obter ofertas de loja privada com planos privados somente que foram adicionadas em escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="e6b7f-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e6b7f-113">Example 3</span></span>
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

<span data-ttu-id="e6b7f-114">Obter a oferta do armazenamento privado com planos privados + públicos que foram adicionados no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="e6b7f-115">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e6b7f-115">Example 4</span></span>
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

<span data-ttu-id="e6b7f-116">Obter a oferta do armazenamento particular com planos privados somente que foi adicionado no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="e6b7f-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e6b7f-117">PARAMETERS</span></span>

### <span data-ttu-id="e6b7f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b7f-118">-DefaultProfile</span></span>
<span data-ttu-id="e6b7f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b7f-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e6b7f-120">-OfferId</span></span>
<span data-ttu-id="e6b7f-121">Oferta de privateStore necessária do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="e6b7f-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="e6b7f-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="e6b7f-122">-PrivateStoreId</span></span>
<span data-ttu-id="e6b7f-123">Ofertas necessárias do Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="e6b7f-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="e6b7f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6b7f-124">-SubscriptionId</span></span>
<span data-ttu-id="e6b7f-125">ID de assinatura do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="e6b7f-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="e6b7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b7f-126">CommonParameters</span></span>
<span data-ttu-id="e6b7f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b7f-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6b7f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b7f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6b7f-129">INPUTS</span></span>

### <span data-ttu-id="e6b7f-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e6b7f-130">None</span></span>

## <span data-ttu-id="e6b7f-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e6b7f-131">OUTPUTS</span></span>

### <span data-ttu-id="e6b7f-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="e6b7f-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="e6b7f-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="e6b7f-133">NOTES</span></span>

## <span data-ttu-id="e6b7f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6b7f-134">RELATED LINKS</span></span>
