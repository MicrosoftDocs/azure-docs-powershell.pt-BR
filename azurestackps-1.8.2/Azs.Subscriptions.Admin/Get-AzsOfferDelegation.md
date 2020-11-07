---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946972"
---
# <span data-ttu-id="e9c59-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e9c59-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="e9c59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9c59-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c59-103">Obter a lista de ofertas delegadas.</span><span class="sxs-lookup"><span data-stu-id="e9c59-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="e9c59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9c59-104">SYNTAX</span></span>

### <span data-ttu-id="e9c59-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="e9c59-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9c59-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e9c59-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="e9c59-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="e9c59-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e9c59-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9c59-108">DESCRIPTION</span></span>
<span data-ttu-id="e9c59-109">Obter a lista de ofertas delegadas.</span><span class="sxs-lookup"><span data-stu-id="e9c59-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="e9c59-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9c59-110">EXAMPLES</span></span>

### <span data-ttu-id="e9c59-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9c59-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="e9c59-112">Obter a lista de ofertas delegadas.</span><span class="sxs-lookup"><span data-stu-id="e9c59-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="e9c59-113">OS</span><span class="sxs-lookup"><span data-stu-id="e9c59-113">PARAMETERS</span></span>

### <span data-ttu-id="e9c59-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9c59-114">-Name</span></span>
<span data-ttu-id="e9c59-115">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="e9c59-115">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c59-116">-Offername</span><span class="sxs-lookup"><span data-stu-id="e9c59-116">-OfferName</span></span>
<span data-ttu-id="e9c59-117">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="e9c59-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c59-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c59-118">-ResourceGroupName</span></span>
<span data-ttu-id="e9c59-119">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="e9c59-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c59-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9c59-120">-ResourceId</span></span>
<span data-ttu-id="e9c59-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e9c59-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9c59-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="e9c59-122">-Skip</span></span>
<span data-ttu-id="e9c59-123">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e9c59-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c59-124">-Início</span><span class="sxs-lookup"><span data-stu-id="e9c59-124">-Top</span></span>
<span data-ttu-id="e9c59-125">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e9c59-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e9c59-126">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="e9c59-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c59-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c59-127">CommonParameters</span></span>
<span data-ttu-id="e9c59-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c59-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c59-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c59-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c59-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9c59-130">INPUTS</span></span>

## <span data-ttu-id="e9c59-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9c59-131">OUTPUTS</span></span>

### <span data-ttu-id="e9c59-132">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e9c59-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="e9c59-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9c59-133">NOTES</span></span>

## <span data-ttu-id="e9c59-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9c59-134">RELATED LINKS</span></span>

