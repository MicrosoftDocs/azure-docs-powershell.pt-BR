---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 29f3d645791dfa0b4f70ed936ccfcb4f72671038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441024"
---
# <span data-ttu-id="26763-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="26763-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="26763-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26763-102">SYNOPSIS</span></span>
<span data-ttu-id="26763-103">Obtenha os termos do contrato para um determinado ID de fornecedor (fornecedor), ID da oferta (produto) e ID do plano (nome).</span><span class="sxs-lookup"><span data-stu-id="26763-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="26763-104">O objeto terms que é retornado por esse comando deve ser passado para Set-AzureRmMarketplaceTerms para aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="26763-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26763-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26763-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26763-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26763-106">DESCRIPTION</span></span>
<span data-ttu-id="26763-107">O cmdlet **Get-AzureRmMarketplaceTerms** retorna termos para a ID de fornecedor (fornecedor), a ID de oferta (produto) e a tupla de ID de plano (nome) fornecidas.</span><span class="sxs-lookup"><span data-stu-id="26763-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="26763-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26763-108">EXAMPLES</span></span>

### <span data-ttu-id="26763-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="26763-109">Example 1</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="26763-110">OS</span><span class="sxs-lookup"><span data-stu-id="26763-110">PARAMETERS</span></span>

### <span data-ttu-id="26763-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26763-111">-DefaultProfile</span></span>
<span data-ttu-id="26763-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26763-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26763-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="26763-113">-Name</span></span>
<span data-ttu-id="26763-114">Cadeia do identificador de plano da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="26763-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26763-115">-Produto</span><span class="sxs-lookup"><span data-stu-id="26763-115">-Product</span></span>
<span data-ttu-id="26763-116">Cadeia de caracteres do identificador de oferta de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="26763-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26763-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="26763-117">-Publisher</span></span>
<span data-ttu-id="26763-118">Identificador de editores cadeia de caracteres de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="26763-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26763-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26763-119">CommonParameters</span></span>
<span data-ttu-id="26763-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26763-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26763-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26763-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26763-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26763-122">INPUTS</span></span>

### <span data-ttu-id="26763-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="26763-123">None</span></span>

## <span data-ttu-id="26763-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26763-124">OUTPUTS</span></span>

### <span data-ttu-id="26763-125">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="26763-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="26763-126">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="26763-126">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="26763-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26763-127">NOTES</span></span>

## <span data-ttu-id="26763-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26763-128">RELATED LINKS</span></span>
