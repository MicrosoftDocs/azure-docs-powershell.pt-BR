---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257690"
---
# <span data-ttu-id="dc067-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="dc067-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="dc067-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc067-102">SYNOPSIS</span></span>
<span data-ttu-id="dc067-103">Remover uma oferta do repositório particular.</span><span class="sxs-lookup"><span data-stu-id="dc067-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="dc067-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc067-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc067-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc067-105">DESCRIPTION</span></span>
<span data-ttu-id="dc067-106">Remover uma oferta do repositório privado que foi criada no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="dc067-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="dc067-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc067-107">EXAMPLES</span></span>

### <span data-ttu-id="dc067-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc067-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="dc067-109">Remover uma oferta do repositório privado que foi criada no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="dc067-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="dc067-110">OS</span><span class="sxs-lookup"><span data-stu-id="dc067-110">PARAMETERS</span></span>

### <span data-ttu-id="dc067-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc067-111">-DefaultProfile</span></span>
<span data-ttu-id="dc067-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc067-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc067-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="dc067-113">-OfferId</span></span>
<span data-ttu-id="dc067-114">Oferta privateStore do Azure Marketplace necessária</span><span class="sxs-lookup"><span data-stu-id="dc067-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="dc067-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc067-115">-PassThru</span></span>
<span data-ttu-id="dc067-116">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="dc067-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="dc067-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="dc067-117">-PrivateStoreId</span></span>
<span data-ttu-id="dc067-118">Requisitos do Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="dc067-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="dc067-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc067-119">-Confirm</span></span>
<span data-ttu-id="dc067-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc067-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc067-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc067-121">-WhatIf</span></span>
<span data-ttu-id="dc067-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc067-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc067-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc067-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc067-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc067-124">CommonParameters</span></span>
<span data-ttu-id="dc067-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc067-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc067-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc067-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc067-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc067-127">INPUTS</span></span>

### <span data-ttu-id="dc067-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dc067-128">None</span></span>

## <span data-ttu-id="dc067-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc067-129">OUTPUTS</span></span>

### <span data-ttu-id="dc067-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc067-130">System.Boolean</span></span>

## <span data-ttu-id="dc067-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc067-131">NOTES</span></span>

## <span data-ttu-id="dc067-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc067-132">RELATED LINKS</span></span>
