---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774795"
---
# <span data-ttu-id="5415f-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5415f-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="5415f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5415f-102">SYNOPSIS</span></span>
<span data-ttu-id="5415f-103">Obter uma lista de todas as redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="5415f-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="5415f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5415f-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="5415f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5415f-105">DESCRIPTION</span></span>
<span data-ttu-id="5415f-106">Obter uma lista de todas as redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="5415f-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="5415f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5415f-107">EXAMPLES</span></span>

### <span data-ttu-id="5415f-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="5415f-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="5415f-109">Retornar uma lista de redes virtuais para o selo de pilha do Azure.</span><span class="sxs-lookup"><span data-stu-id="5415f-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="5415f-110">OS</span><span class="sxs-lookup"><span data-stu-id="5415f-110">PARAMETERS</span></span>

### <span data-ttu-id="5415f-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5415f-111">-Filter</span></span>
<span data-ttu-id="5415f-112">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="5415f-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5415f-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5415f-113">-OrderBy</span></span>
<span data-ttu-id="5415f-114">Parâmetro orderBy do OData.</span><span class="sxs-lookup"><span data-stu-id="5415f-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5415f-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="5415f-115">-Skip</span></span>
<span data-ttu-id="5415f-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5415f-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5415f-117">-Início</span><span class="sxs-lookup"><span data-stu-id="5415f-117">-Top</span></span>
<span data-ttu-id="5415f-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5415f-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5415f-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="5415f-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5415f-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="5415f-120">-InlineCount</span></span>
<span data-ttu-id="5415f-121">Parâmetro de contagem embutida do OData.</span><span class="sxs-lookup"><span data-stu-id="5415f-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5415f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5415f-122">CommonParameters</span></span>
<span data-ttu-id="5415f-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5415f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5415f-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5415f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5415f-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5415f-125">INPUTS</span></span>

## <span data-ttu-id="5415f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5415f-126">OUTPUTS</span></span>

### <span data-ttu-id="5415f-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5415f-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="5415f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5415f-128">NOTES</span></span>

## <span data-ttu-id="5415f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5415f-129">RELATED LINKS</span></span>
