---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946761"
---
# <span data-ttu-id="a6a1d-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="a6a1d-101">Get-AzsOffer</span></span>

## <span data-ttu-id="a6a1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a1d-103">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-103">Get the list of public offers.</span></span>

## <span data-ttu-id="a6a1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6a1d-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a6a1d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6a1d-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a1d-106">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-106">Get the list of public offers.</span></span>

## <span data-ttu-id="a6a1d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6a1d-107">EXAMPLES</span></span>

### <span data-ttu-id="a6a1d-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="a6a1d-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="a6a1d-109">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-109">Get the list of public offers.</span></span>

## <span data-ttu-id="a6a1d-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6a1d-110">PARAMETERS</span></span>

### <span data-ttu-id="a6a1d-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="a6a1d-111">-Skip</span></span>
<span data-ttu-id="a6a1d-112">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a1d-113">-Início</span><span class="sxs-lookup"><span data-stu-id="a6a1d-113">-Top</span></span>
<span data-ttu-id="a6a1d-114">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a6a1d-115">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a1d-116">-Provedor</span><span class="sxs-lookup"><span data-stu-id="a6a1d-116">-Provider</span></span>
<span data-ttu-id="a6a1d-117">Parâmetro opcional para especificar o nome do provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="a6a1d-118">Este parâmetro não está sendo usado e será preterido no futuro.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a1d-119">CommonParameters</span></span>
<span data-ttu-id="a6a1d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a1d-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a1d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a1d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6a1d-122">INPUTS</span></span>

## <span data-ttu-id="a6a1d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6a1d-123">OUTPUTS</span></span>

### <span data-ttu-id="a6a1d-124">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="a6a1d-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="a6a1d-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6a1d-125">NOTES</span></span>

## <span data-ttu-id="a6a1d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6a1d-126">RELATED LINKS</span></span>
