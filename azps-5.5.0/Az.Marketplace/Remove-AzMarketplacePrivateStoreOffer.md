---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113572"
---
# <span data-ttu-id="fbacc-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="fbacc-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="fbacc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbacc-102">SYNOPSIS</span></span>
<span data-ttu-id="fbacc-103">Remover uma oferta do armazenamento particular.</span><span class="sxs-lookup"><span data-stu-id="fbacc-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="fbacc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbacc-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbacc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbacc-105">DESCRIPTION</span></span>
<span data-ttu-id="fbacc-106">Remover uma oferta do armazenamento particular que foi criada no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="fbacc-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="fbacc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fbacc-107">EXAMPLES</span></span>

### <span data-ttu-id="fbacc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fbacc-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="fbacc-109">Remover uma oferta do armazenamento particular que foi criada no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="fbacc-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="fbacc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbacc-110">PARAMETERS</span></span>

### <span data-ttu-id="fbacc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbacc-111">-DefaultProfile</span></span>
<span data-ttu-id="fbacc-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbacc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbacc-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="fbacc-113">-OfferId</span></span>
<span data-ttu-id="fbacc-114">Oferta do Azure Marketplace privateStore necessária</span><span class="sxs-lookup"><span data-stu-id="fbacc-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="fbacc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbacc-115">-PassThru</span></span>
<span data-ttu-id="fbacc-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="fbacc-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="fbacc-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="fbacc-117">-PrivateStoreId</span></span>
<span data-ttu-id="fbacc-118">Azure Marketplace privateStore obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbacc-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="fbacc-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fbacc-119">-Confirm</span></span>
<span data-ttu-id="fbacc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbacc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbacc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbacc-121">-WhatIf</span></span>
<span data-ttu-id="fbacc-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fbacc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbacc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fbacc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbacc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbacc-124">CommonParameters</span></span>
<span data-ttu-id="fbacc-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbacc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbacc-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbacc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbacc-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="fbacc-127">INPUTS</span></span>

### <span data-ttu-id="fbacc-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fbacc-128">None</span></span>

## <span data-ttu-id="fbacc-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="fbacc-129">OUTPUTS</span></span>

### <span data-ttu-id="fbacc-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbacc-130">System.Boolean</span></span>

## <span data-ttu-id="fbacc-131">Notas</span><span class="sxs-lookup"><span data-stu-id="fbacc-131">NOTES</span></span>

## <span data-ttu-id="fbacc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbacc-132">RELATED LINKS</span></span>
