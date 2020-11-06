---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 730861b055259fd0aee5490de2421abe96afc10b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595910"
---
# <span data-ttu-id="02d2e-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="02d2e-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="02d2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="02d2e-103">Obtenha os termos do contrato para um determinado ID de fornecedor (fornecedor), ID da oferta (produto) e ID do plano (nome).</span><span class="sxs-lookup"><span data-stu-id="02d2e-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="02d2e-104">O objeto terms que é retornado por esse comando deve ser passado para Set-AzMarketplaceTerms para aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="02d2e-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="02d2e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02d2e-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d2e-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02d2e-106">DESCRIPTION</span></span>
<span data-ttu-id="02d2e-107">O cmdlet **Get-AzMarketplaceTerms** retorna termos para a ID de fornecedor (fornecedor), a ID de oferta (produto) e a tupla de ID de plano (nome) fornecidas.</span><span class="sxs-lookup"><span data-stu-id="02d2e-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="02d2e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02d2e-108">EXAMPLES</span></span>

### <span data-ttu-id="02d2e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02d2e-109">Example 1</span></span>
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

## <span data-ttu-id="02d2e-110">OS</span><span class="sxs-lookup"><span data-stu-id="02d2e-110">PARAMETERS</span></span>

### <span data-ttu-id="02d2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d2e-111">-DefaultProfile</span></span>
<span data-ttu-id="02d2e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02d2e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02d2e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="02d2e-113">-Name</span></span>
<span data-ttu-id="02d2e-114">Cadeia do identificador de plano da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="02d2e-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="02d2e-115">-Produto</span><span class="sxs-lookup"><span data-stu-id="02d2e-115">-Product</span></span>
<span data-ttu-id="02d2e-116">Cadeia de caracteres do identificador de oferta de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="02d2e-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="02d2e-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="02d2e-117">-Publisher</span></span>
<span data-ttu-id="02d2e-118">Identificador de editores cadeia de caracteres de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="02d2e-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="02d2e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d2e-119">CommonParameters</span></span>
<span data-ttu-id="02d2e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d2e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d2e-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d2e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d2e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02d2e-122">INPUTS</span></span>

### <span data-ttu-id="02d2e-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="02d2e-123">None</span></span>

## <span data-ttu-id="02d2e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02d2e-124">OUTPUTS</span></span>

### <span data-ttu-id="02d2e-125">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="02d2e-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="02d2e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02d2e-126">NOTES</span></span>

## <span data-ttu-id="02d2e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02d2e-127">RELATED LINKS</span></span>
