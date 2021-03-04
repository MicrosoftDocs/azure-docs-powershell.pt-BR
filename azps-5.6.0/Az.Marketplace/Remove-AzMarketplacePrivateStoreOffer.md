---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 829f6b4e95e1d45d68f12ed6dbd8ad7c7987eba3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892122"
---
# <span data-ttu-id="4069f-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="4069f-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="4069f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4069f-102">SYNOPSIS</span></span>
<span data-ttu-id="4069f-103">Remova uma oferta do armazenamento particular.</span><span class="sxs-lookup"><span data-stu-id="4069f-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="4069f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4069f-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4069f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4069f-105">DESCRIPTION</span></span>
<span data-ttu-id="4069f-106">Remova uma oferta do armazenamento particular criado no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="4069f-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="4069f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4069f-107">EXAMPLES</span></span>

### <span data-ttu-id="4069f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4069f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="4069f-109">Remova uma oferta do armazenamento particular criado no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="4069f-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="4069f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4069f-110">PARAMETERS</span></span>

### <span data-ttu-id="4069f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4069f-111">-DefaultProfile</span></span>
<span data-ttu-id="4069f-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4069f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4069f-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="4069f-113">-OfferId</span></span>
<span data-ttu-id="4069f-114">Oferta de privateStore necessária do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="4069f-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="4069f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4069f-115">-PassThru</span></span>
<span data-ttu-id="4069f-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="4069f-116">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4069f-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="4069f-117">-PrivateStoreId</span></span>
<span data-ttu-id="4069f-118">PrivateStore necessário do Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="4069f-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="4069f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4069f-119">-Confirm</span></span>
<span data-ttu-id="4069f-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4069f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4069f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4069f-121">-WhatIf</span></span>
<span data-ttu-id="4069f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4069f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4069f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4069f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4069f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4069f-124">CommonParameters</span></span>
<span data-ttu-id="4069f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4069f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4069f-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4069f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4069f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4069f-127">INPUTS</span></span>

### <span data-ttu-id="4069f-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4069f-128">None</span></span>

## <span data-ttu-id="4069f-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4069f-129">OUTPUTS</span></span>

### <span data-ttu-id="4069f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4069f-130">System.Boolean</span></span>

## <span data-ttu-id="4069f-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="4069f-131">NOTES</span></span>

## <span data-ttu-id="4069f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4069f-132">RELATED LINKS</span></span>
