---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124839"
---
# <span data-ttu-id="06a2e-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="06a2e-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="06a2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="06a2e-103">Atualiza ou cria a oferta para armazenamento particular.</span><span class="sxs-lookup"><span data-stu-id="06a2e-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="06a2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06a2e-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a2e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="06a2e-106">Atualiza ou cria a oferta para armazenamento privado que foi criada em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="06a2e-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="06a2e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06a2e-107">EXAMPLES</span></span>

### <span data-ttu-id="06a2e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06a2e-108">Example 1</span></span>
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

<span data-ttu-id="06a2e-109">Cria uma oferta com planos privados + públicos para armazenamento particular que foi criado em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="06a2e-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="06a2e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="06a2e-110">Example 2</span></span>
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

<span data-ttu-id="06a2e-111">Cria uma oferta com planos particulares somente para armazenamento privado criado em escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="06a2e-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="06a2e-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="06a2e-112">Example 3</span></span>
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

<span data-ttu-id="06a2e-113">As atualizações oferecem planos privados + públicos para armazenamento particular criado em escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="06a2e-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="06a2e-114">ETag é necessário.</span><span class="sxs-lookup"><span data-stu-id="06a2e-114">Etag is needed.</span></span>

### <span data-ttu-id="06a2e-115">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="06a2e-115">Example 4</span></span>
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

<span data-ttu-id="06a2e-116">Atualizações oferta para armazenamento privado somente com planos particulares que foram criados em escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="06a2e-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="06a2e-117">ETag é necessário.</span><span class="sxs-lookup"><span data-stu-id="06a2e-117">Etag is needed.</span></span>


## <span data-ttu-id="06a2e-118">OS</span><span class="sxs-lookup"><span data-stu-id="06a2e-118">PARAMETERS</span></span>

### <span data-ttu-id="06a2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a2e-119">-DefaultProfile</span></span>
<span data-ttu-id="06a2e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06a2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06a2e-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="06a2e-121">-ETag</span></span>
<span data-ttu-id="06a2e-122">ETag do Azure Marketplace privateStore da oferta de atualização</span><span class="sxs-lookup"><span data-stu-id="06a2e-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="06a2e-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="06a2e-123">-OfferId</span></span>
<span data-ttu-id="06a2e-124">Oferta privateStore do Azure Marketplace necessária</span><span class="sxs-lookup"><span data-stu-id="06a2e-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="06a2e-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="06a2e-125">-PrivateStoreId</span></span>
<span data-ttu-id="06a2e-126">Ofertas de privateStore do Azure Marketplace necessárias</span><span class="sxs-lookup"><span data-stu-id="06a2e-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="06a2e-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="06a2e-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="06a2e-128">Limitação de IDs do plano específico do Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="06a2e-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="06a2e-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06a2e-129">-Confirm</span></span>
<span data-ttu-id="06a2e-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06a2e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06a2e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a2e-131">-WhatIf</span></span>
<span data-ttu-id="06a2e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06a2e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06a2e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06a2e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06a2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a2e-134">CommonParameters</span></span>
<span data-ttu-id="06a2e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a2e-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06a2e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a2e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06a2e-137">INPUTS</span></span>

### <span data-ttu-id="06a2e-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="06a2e-138">None</span></span>

## <span data-ttu-id="06a2e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06a2e-139">OUTPUTS</span></span>

### <span data-ttu-id="06a2e-140">Microsoft. Azure. Commands. marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="06a2e-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="06a2e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06a2e-141">NOTES</span></span>

## <span data-ttu-id="06a2e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06a2e-142">RELATED LINKS</span></span>
