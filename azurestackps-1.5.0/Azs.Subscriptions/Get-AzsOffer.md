---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425905"
---
# <span data-ttu-id="c4e10-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="c4e10-101">Get-AzsOffer</span></span>

## <span data-ttu-id="c4e10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4e10-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e10-103">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="c4e10-103">Get the list of public offers.</span></span>

## <span data-ttu-id="c4e10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4e10-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c4e10-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4e10-105">DESCRIPTION</span></span>
<span data-ttu-id="c4e10-106">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="c4e10-106">Get the list of public offers.</span></span>

## <span data-ttu-id="c4e10-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4e10-107">EXAMPLES</span></span>

### <span data-ttu-id="c4e10-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4e10-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="c4e10-109">Obtenha a lista de ofertas públicas.</span><span class="sxs-lookup"><span data-stu-id="c4e10-109">Get the list of public offers.</span></span>

## <span data-ttu-id="c4e10-110">OS</span><span class="sxs-lookup"><span data-stu-id="c4e10-110">PARAMETERS</span></span>

### <span data-ttu-id="c4e10-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="c4e10-111">-Skip</span></span>
<span data-ttu-id="c4e10-112">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c4e10-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c4e10-113">-Início</span><span class="sxs-lookup"><span data-stu-id="c4e10-113">-Top</span></span>
<span data-ttu-id="c4e10-114">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c4e10-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c4e10-115">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="c4e10-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c4e10-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e10-116">CommonParameters</span></span>
<span data-ttu-id="c4e10-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4e10-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e10-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e10-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e10-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4e10-119">INPUTS</span></span>

## <span data-ttu-id="c4e10-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4e10-120">OUTPUTS</span></span>

### <span data-ttu-id="c4e10-121">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="c4e10-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="c4e10-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4e10-122">NOTES</span></span>

## <span data-ttu-id="c4e10-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4e10-123">RELATED LINKS</span></span>

