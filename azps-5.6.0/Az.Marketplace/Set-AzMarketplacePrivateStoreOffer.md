---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 9a2f5744f5595b7be4a0a59c3181435e4f1d0eb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892854"
---
# <span data-ttu-id="b7a44-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="b7a44-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="b7a44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7a44-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a44-103">Atualiza ou cria oferta para o armazenamento particular.</span><span class="sxs-lookup"><span data-stu-id="b7a44-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="b7a44-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7a44-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7a44-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7a44-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a44-106">Atualiza ou cria oferta para o armazenamento particular criado no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="b7a44-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="b7a44-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7a44-107">EXAMPLES</span></span>

### <span data-ttu-id="b7a44-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7a44-108">Example 1</span></span>
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

<span data-ttu-id="b7a44-109">Cria oferta com planos privados + públicos para o armazenamento privado que foi criado no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="b7a44-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="b7a44-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b7a44-110">Example 2</span></span>
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

<span data-ttu-id="b7a44-111">Cria oferta com planos privados apenas para o armazenamento particular que foi criado no escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="b7a44-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="b7a44-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b7a44-112">Example 3</span></span>
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

<span data-ttu-id="b7a44-113">As atualizações oferecem com planos privados + públicos para o armazenamento privado que foi criado no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="b7a44-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="b7a44-114">Etag é necessário.</span><span class="sxs-lookup"><span data-stu-id="b7a44-114">Etag is needed.</span></span>

### <span data-ttu-id="b7a44-115">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="b7a44-115">Example 4</span></span>
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

<span data-ttu-id="b7a44-116">Oferta de atualizações para o armazenamento particular com planos privados somente que foi criado no escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="b7a44-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="b7a44-117">Etag é necessário.</span><span class="sxs-lookup"><span data-stu-id="b7a44-117">Etag is needed.</span></span>


## <span data-ttu-id="b7a44-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7a44-118">PARAMETERS</span></span>

### <span data-ttu-id="b7a44-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a44-119">-DefaultProfile</span></span>
<span data-ttu-id="b7a44-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a44-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7a44-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="b7a44-121">-ETag</span></span>
<span data-ttu-id="b7a44-122">Oferta de privateStore do Azure Marketplace para atualização</span><span class="sxs-lookup"><span data-stu-id="b7a44-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="b7a44-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="b7a44-123">-OfferId</span></span>
<span data-ttu-id="b7a44-124">Oferta de privateStore necessária do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="b7a44-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="b7a44-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="b7a44-125">-PrivateStoreId</span></span>
<span data-ttu-id="b7a44-126">Ofertas necessárias do Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="b7a44-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="b7a44-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="b7a44-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="b7a44-128">Limitação de IDs de plano específicas da oferta do Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="b7a44-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="b7a44-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7a44-129">-Confirm</span></span>
<span data-ttu-id="b7a44-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7a44-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7a44-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a44-131">-WhatIf</span></span>
<span data-ttu-id="b7a44-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7a44-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7a44-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7a44-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7a44-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a44-134">CommonParameters</span></span>
<span data-ttu-id="b7a44-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a44-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a44-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7a44-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a44-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7a44-137">INPUTS</span></span>

### <span data-ttu-id="b7a44-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b7a44-138">None</span></span>

## <span data-ttu-id="b7a44-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7a44-139">OUTPUTS</span></span>

### <span data-ttu-id="b7a44-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="b7a44-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="b7a44-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7a44-141">NOTES</span></span>

## <span data-ttu-id="b7a44-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7a44-142">RELATED LINKS</span></span>
