---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774733"
---
# <span data-ttu-id="8eb3a-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="8eb3a-101">Get-AzsOffer</span></span>

## <span data-ttu-id="8eb3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb3a-103">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-103">Get the list of public offers.</span></span>

## <span data-ttu-id="8eb3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8eb3a-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="8eb3a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8eb3a-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb3a-106">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-106">Get the list of public offers.</span></span>

## <span data-ttu-id="8eb3a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8eb3a-107">EXAMPLES</span></span>

### <span data-ttu-id="8eb3a-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="8eb3a-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="8eb3a-109">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-109">Get the list of public offers.</span></span>

## <span data-ttu-id="8eb3a-110">OS</span><span class="sxs-lookup"><span data-stu-id="8eb3a-110">PARAMETERS</span></span>

### <span data-ttu-id="8eb3a-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="8eb3a-111">-Skip</span></span>
<span data-ttu-id="8eb3a-112">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8eb3a-113">-Início</span><span class="sxs-lookup"><span data-stu-id="8eb3a-113">-Top</span></span>
<span data-ttu-id="8eb3a-114">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8eb3a-115">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8eb3a-116">-Provedor</span><span class="sxs-lookup"><span data-stu-id="8eb3a-116">-Provider</span></span>
<span data-ttu-id="8eb3a-117">Parâmetro opcional para especificar o nome do provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="8eb3a-118">Este parâmetro não está sendo usado e será preterido no futuro.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-118">This parameter is not being used and will be deprecated in future.</span></span>

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

### <span data-ttu-id="8eb3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb3a-119">CommonParameters</span></span>
<span data-ttu-id="8eb3a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb3a-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb3a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb3a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8eb3a-122">INPUTS</span></span>

## <span data-ttu-id="8eb3a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8eb3a-123">OUTPUTS</span></span>

### <span data-ttu-id="8eb3a-124">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="8eb3a-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="8eb3a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8eb3a-125">NOTES</span></span>

## <span data-ttu-id="8eb3a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eb3a-126">RELATED LINKS</span></span>
