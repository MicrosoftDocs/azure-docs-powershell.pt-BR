---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946951"
---
# <span data-ttu-id="71044-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="71044-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="71044-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71044-102">SYNOPSIS</span></span>
<span data-ttu-id="71044-103">Obtenha uma lista de todos os balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="71044-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="71044-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71044-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="71044-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71044-105">DESCRIPTION</span></span>
<span data-ttu-id="71044-106">Obtenha uma lista de todos os balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="71044-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="71044-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71044-107">EXAMPLES</span></span>

### <span data-ttu-id="71044-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="71044-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="71044-109">Obtenha uma lista de todos os balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="71044-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="71044-110">OS</span><span class="sxs-lookup"><span data-stu-id="71044-110">PARAMETERS</span></span>

### <span data-ttu-id="71044-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="71044-111">-Filter</span></span>
<span data-ttu-id="71044-112">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="71044-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="71044-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="71044-113">-OrderBy</span></span>
<span data-ttu-id="71044-114">Parâmetro orderBy do OData.</span><span class="sxs-lookup"><span data-stu-id="71044-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="71044-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="71044-115">-Skip</span></span>
<span data-ttu-id="71044-116">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="71044-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="71044-117">-Início</span><span class="sxs-lookup"><span data-stu-id="71044-117">-Top</span></span>
<span data-ttu-id="71044-118">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="71044-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="71044-119">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="71044-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="71044-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="71044-120">-InlineCount</span></span>
<span data-ttu-id="71044-121">Parâmetro de contagem embutida do OData.</span><span class="sxs-lookup"><span data-stu-id="71044-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="71044-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71044-122">CommonParameters</span></span>
<span data-ttu-id="71044-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71044-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71044-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71044-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71044-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71044-125">INPUTS</span></span>

## <span data-ttu-id="71044-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71044-126">OUTPUTS</span></span>

### <span data-ttu-id="71044-127">Microsoft. AzureStack. Management. Network. admin. Models. loadbalancer</span><span class="sxs-lookup"><span data-stu-id="71044-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="71044-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71044-128">NOTES</span></span>

## <span data-ttu-id="71044-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71044-129">RELATED LINKS</span></span>
