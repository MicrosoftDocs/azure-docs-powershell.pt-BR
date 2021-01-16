---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428265"
---
# <span data-ttu-id="3e485-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="3e485-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="3e485-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e485-102">SYNOPSIS</span></span>
<span data-ttu-id="3e485-103">Atualiza ou cria a oferta para armazenamento particular.</span><span class="sxs-lookup"><span data-stu-id="3e485-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="3e485-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e485-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e485-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e485-105">DESCRIPTION</span></span>
<span data-ttu-id="3e485-106">Atualiza ou cria a oferta para armazenamento privado que foi criada em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="3e485-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="3e485-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e485-107">EXAMPLES</span></span>

### <span data-ttu-id="3e485-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e485-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="3e485-109">Cria uma oferta com planos privados + públicos para armazenamento particular que foi criado em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="3e485-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="3e485-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3e485-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="3e485-111">Cria uma oferta com planos particulares somente para armazenamento privado criado em escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3e485-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="3e485-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3e485-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="3e485-113">As atualizações oferecem planos privados + públicos para armazenamento particular criado em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="3e485-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="3e485-114">ETag é necessário.</span><span class="sxs-lookup"><span data-stu-id="3e485-114">Etag is needed.</span></span>

### <span data-ttu-id="3e485-115">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="3e485-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="3e485-116">Atualizações oferta para armazenamento privado somente com planos particulares que foram criados em escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3e485-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="3e485-117">ETag é necessário.</span><span class="sxs-lookup"><span data-stu-id="3e485-117">Etag is needed.</span></span>


## <span data-ttu-id="3e485-118">OS</span><span class="sxs-lookup"><span data-stu-id="3e485-118">PARAMETERS</span></span>

### <span data-ttu-id="3e485-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e485-119">-DefaultProfile</span></span>
<span data-ttu-id="3e485-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e485-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e485-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="3e485-121">-ETag</span></span>
<span data-ttu-id="3e485-122">ETag do Azure Marketplace privateStore da oferta de atualização</span><span class="sxs-lookup"><span data-stu-id="3e485-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="3e485-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="3e485-123">-OfferId</span></span>
<span data-ttu-id="3e485-124">Oferta privateStore do Azure Marketplace necessária</span><span class="sxs-lookup"><span data-stu-id="3e485-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="3e485-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="3e485-125">-PrivateStoreId</span></span>
<span data-ttu-id="3e485-126">Ofertas de privateStore do Azure Marketplace necessárias</span><span class="sxs-lookup"><span data-stu-id="3e485-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="3e485-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="3e485-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="3e485-128">Limitação de IDs do plano específico do Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="3e485-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e485-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e485-129">-Confirm</span></span>
<span data-ttu-id="3e485-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e485-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e485-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e485-131">-WhatIf</span></span>
<span data-ttu-id="3e485-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e485-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e485-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e485-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e485-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e485-134">CommonParameters</span></span>
<span data-ttu-id="3e485-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e485-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e485-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e485-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e485-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e485-137">INPUTS</span></span>

### <span data-ttu-id="3e485-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3e485-138">None</span></span>

## <span data-ttu-id="3e485-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e485-139">OUTPUTS</span></span>

### <span data-ttu-id="3e485-140">Microsoft. Azure. Commands. marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="3e485-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="3e485-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e485-141">NOTES</span></span>

## <span data-ttu-id="3e485-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e485-142">RELATED LINKS</span></span>
