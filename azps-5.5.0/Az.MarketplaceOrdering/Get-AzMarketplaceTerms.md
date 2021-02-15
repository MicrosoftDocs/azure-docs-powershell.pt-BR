---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111782"
---
# <span data-ttu-id="04d9b-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="04d9b-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="04d9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="04d9b-103">Obter os termos do contrato para uma determinada ID do publisher(Publisher), id da oferta(Produto) e id do plano(Nome).</span><span class="sxs-lookup"><span data-stu-id="04d9b-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="04d9b-104">O objeto de termos que é retornado por este comando deve ser passado para Set-AzMarketplaceTerms aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="04d9b-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="04d9b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04d9b-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04d9b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="04d9b-106">DESCRIPTION</span></span>
<span data-ttu-id="04d9b-107">O cmdlet **Get-AzMarketplaceTerms** retorna termos para determinada id do publisher(Publisher), id da oferta(Produto) e id (nome) da tupla.</span><span class="sxs-lookup"><span data-stu-id="04d9b-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="04d9b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="04d9b-108">EXAMPLES</span></span>

### <span data-ttu-id="04d9b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04d9b-109">Example 1</span></span>
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

## <span data-ttu-id="04d9b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04d9b-110">PARAMETERS</span></span>

### <span data-ttu-id="04d9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d9b-111">-DefaultProfile</span></span>
<span data-ttu-id="04d9b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04d9b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04d9b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="04d9b-113">-Name</span></span>
<span data-ttu-id="04d9b-114">Cadeia de caracteres identificador de plano da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="04d9b-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="04d9b-115">-Produto</span><span class="sxs-lookup"><span data-stu-id="04d9b-115">-Product</span></span>
<span data-ttu-id="04d9b-116">Oferecer cadeia de caracteres identificador da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="04d9b-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="04d9b-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="04d9b-117">-Publisher</span></span>
<span data-ttu-id="04d9b-118">Cadeia de caracteres identificador do Publisher da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="04d9b-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="04d9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d9b-119">CommonParameters</span></span>
<span data-ttu-id="04d9b-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04d9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d9b-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04d9b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d9b-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="04d9b-122">INPUTS</span></span>

### <span data-ttu-id="04d9b-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="04d9b-123">None</span></span>

## <span data-ttu-id="04d9b-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="04d9b-124">OUTPUTS</span></span>

### <span data-ttu-id="04d9b-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="04d9b-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="04d9b-126">Notas</span><span class="sxs-lookup"><span data-stu-id="04d9b-126">NOTES</span></span>

## <span data-ttu-id="04d9b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04d9b-127">RELATED LINKS</span></span>
