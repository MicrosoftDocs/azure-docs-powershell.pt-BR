---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114266"
---
# <span data-ttu-id="1f525-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="1f525-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="1f525-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f525-102">SYNOPSIS</span></span>
<span data-ttu-id="1f525-103">Obter uma ou mais ofertas do armazenamento particular.</span><span class="sxs-lookup"><span data-stu-id="1f525-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="1f525-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f525-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f525-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f525-105">DESCRIPTION</span></span>
<span data-ttu-id="1f525-106">Obter uma ou mais ofertas do armazenamento particular com planos públicos + privados que foram adicionados sob o escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="1f525-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="1f525-107">Se a ID da assinatura for presente, obter uma ou mais ofertas do armazenamento particular com planos particulares apenas no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="1f525-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="1f525-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f525-108">EXAMPLES</span></span>

### <span data-ttu-id="1f525-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f525-109">Example 1</span></span>
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

<span data-ttu-id="1f525-110">Obter ofertas do armazenamento particular com planos privados + públicos que foram adicionados sob o escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="1f525-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="1f525-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1f525-111">Example 2</span></span>
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

<span data-ttu-id="1f525-112">Obter ofertas do armazenamento particular com planos particulares somente que foram adicionadas no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="1f525-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="1f525-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1f525-113">Example 3</span></span>
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

<span data-ttu-id="1f525-114">Obter a oferta do armazenamento particular com planos privados + públicos que foram adicionados sob o escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="1f525-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="1f525-115">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="1f525-115">Example 4</span></span>
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

<span data-ttu-id="1f525-116">Obter a oferta do armazenamento particular apenas com planos particulares que foram adicionados sob o escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="1f525-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="1f525-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f525-117">PARAMETERS</span></span>

### <span data-ttu-id="1f525-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f525-118">-DefaultProfile</span></span>
<span data-ttu-id="1f525-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f525-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f525-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="1f525-120">-OfferId</span></span>
<span data-ttu-id="1f525-121">Oferta do Azure Marketplace privateStore necessária</span><span class="sxs-lookup"><span data-stu-id="1f525-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="1f525-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="1f525-122">-PrivateStoreId</span></span>
<span data-ttu-id="1f525-123">Ofertas necessárias do Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="1f525-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="1f525-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f525-124">-SubscriptionId</span></span>
<span data-ttu-id="1f525-125">ID de assinatura do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="1f525-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="1f525-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f525-126">CommonParameters</span></span>
<span data-ttu-id="1f525-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f525-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f525-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f525-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f525-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f525-129">INPUTS</span></span>

### <span data-ttu-id="1f525-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1f525-130">None</span></span>

## <span data-ttu-id="1f525-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f525-131">OUTPUTS</span></span>

### <span data-ttu-id="1f525-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="1f525-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="1f525-133">Notas</span><span class="sxs-lookup"><span data-stu-id="1f525-133">NOTES</span></span>

## <span data-ttu-id="1f525-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f525-134">RELATED LINKS</span></span>
