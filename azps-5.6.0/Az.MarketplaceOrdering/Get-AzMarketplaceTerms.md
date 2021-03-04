---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 9878bdaa508d2cc229f494dcd53467f9c7d62ed1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887105"
---
# <span data-ttu-id="8c7f0-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8c7f0-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="8c7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7f0-103">Obter os termos de contrato para um determinado publisher id(Publisher), id(Product) e plan id(Name).</span><span class="sxs-lookup"><span data-stu-id="8c7f0-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8c7f0-104">O objeto terms retornado por este comando deve ser passado para Set-AzMarketplaceTerms aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="8c7f0-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="8c7f0-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8c7f0-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7f0-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8c7f0-106">DESCRIPTION</span></span>
<span data-ttu-id="8c7f0-107">O cmdlet **Get-AzMarketplaceTerms** retorna termos para determinado id(Publisher), id(Product) de oferta e planejamento de id(Name).</span><span class="sxs-lookup"><span data-stu-id="8c7f0-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="8c7f0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c7f0-108">EXAMPLES</span></span>

### <span data-ttu-id="8c7f0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8c7f0-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="8c7f0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8c7f0-110">PARAMETERS</span></span>

### <span data-ttu-id="8c7f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7f0-111">-DefaultProfile</span></span>
<span data-ttu-id="8c7f0-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c7f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c7f0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8c7f0-113">-Name</span></span>
<span data-ttu-id="8c7f0-114">Planejar a cadeia de caracteres de identificador da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="8c7f0-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="8c7f0-115">-Product</span><span class="sxs-lookup"><span data-stu-id="8c7f0-115">-Product</span></span>
<span data-ttu-id="8c7f0-116">Oferecer cadeia de caracteres de identificador de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="8c7f0-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="8c7f0-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8c7f0-117">-Publisher</span></span>
<span data-ttu-id="8c7f0-118">Cadeia de caracteres de identificador do publisher da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="8c7f0-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="8c7f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7f0-119">CommonParameters</span></span>
<span data-ttu-id="8c7f0-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7f0-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7f0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7f0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c7f0-122">INPUTS</span></span>

### <span data-ttu-id="8c7f0-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8c7f0-123">None</span></span>

## <span data-ttu-id="8c7f0-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8c7f0-124">OUTPUTS</span></span>

### <span data-ttu-id="8c7f0-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="8c7f0-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="8c7f0-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="8c7f0-126">NOTES</span></span>

## <span data-ttu-id="8c7f0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c7f0-127">RELATED LINKS</span></span>
