---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43691cfa3299fc0534ce2d44fd2a2f6ed1043d04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426090"
---
# <span data-ttu-id="69588-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="69588-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="69588-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69588-102">SYNOPSIS</span></span>
<span data-ttu-id="69588-103">Obter uma lista de todas as redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="69588-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="69588-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69588-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="69588-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69588-105">DESCRIPTION</span></span>
<span data-ttu-id="69588-106">Obter uma lista de todas as redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="69588-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="69588-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69588-107">EXAMPLES</span></span>

### <span data-ttu-id="69588-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="69588-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="69588-109">Retornar uma lista de redes virtuais para o selo de pilha do Azure.</span><span class="sxs-lookup"><span data-stu-id="69588-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="69588-110">OS</span><span class="sxs-lookup"><span data-stu-id="69588-110">PARAMETERS</span></span>

### <span data-ttu-id="69588-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="69588-111">-Filter</span></span>
<span data-ttu-id="69588-112">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="69588-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="69588-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="69588-113">-InlineCount</span></span>
<span data-ttu-id="69588-114">Parâmetro de contagem embutida do OData.</span><span class="sxs-lookup"><span data-stu-id="69588-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="69588-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="69588-115">-OrderBy</span></span>
<span data-ttu-id="69588-116">Parâmetro orderBy do OData.</span><span class="sxs-lookup"><span data-stu-id="69588-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="69588-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="69588-117">-Skip</span></span>
<span data-ttu-id="69588-118">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="69588-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="69588-119">-Início</span><span class="sxs-lookup"><span data-stu-id="69588-119">-Top</span></span>
<span data-ttu-id="69588-120">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="69588-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="69588-121">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="69588-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="69588-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69588-122">CommonParameters</span></span>
<span data-ttu-id="69588-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69588-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69588-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69588-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69588-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69588-125">INPUTS</span></span>

## <span data-ttu-id="69588-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69588-126">OUTPUTS</span></span>

### <span data-ttu-id="69588-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="69588-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="69588-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69588-128">NOTES</span></span>

## <span data-ttu-id="69588-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69588-129">RELATED LINKS</span></span>

