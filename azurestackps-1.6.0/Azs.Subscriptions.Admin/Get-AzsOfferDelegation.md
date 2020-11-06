---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426021"
---
# <span data-ttu-id="10107-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="10107-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="10107-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10107-102">SYNOPSIS</span></span>
<span data-ttu-id="10107-103">Obter a lista de ofertas delegadas.</span><span class="sxs-lookup"><span data-stu-id="10107-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="10107-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10107-104">SYNTAX</span></span>

### <span data-ttu-id="10107-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="10107-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="10107-106">Obter</span><span class="sxs-lookup"><span data-stu-id="10107-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="10107-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="10107-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="10107-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10107-108">DESCRIPTION</span></span>
<span data-ttu-id="10107-109">Obter a lista de ofertas delegadas.</span><span class="sxs-lookup"><span data-stu-id="10107-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="10107-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10107-110">EXAMPLES</span></span>

### <span data-ttu-id="10107-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="10107-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="10107-112">Obter a lista de ofertas delegadas.</span><span class="sxs-lookup"><span data-stu-id="10107-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="10107-113">OS</span><span class="sxs-lookup"><span data-stu-id="10107-113">PARAMETERS</span></span>

### <span data-ttu-id="10107-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="10107-114">-Name</span></span>
<span data-ttu-id="10107-115">Nome de uma delegação de oferta.</span><span class="sxs-lookup"><span data-stu-id="10107-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="10107-116">-Offername</span><span class="sxs-lookup"><span data-stu-id="10107-116">-OfferName</span></span>
<span data-ttu-id="10107-117">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="10107-117">Name of an offer.</span></span>

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

### <span data-ttu-id="10107-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10107-118">-ResourceGroupName</span></span>
<span data-ttu-id="10107-119">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="10107-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="10107-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10107-120">-ResourceId</span></span>
<span data-ttu-id="10107-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="10107-121">The resource id.</span></span>

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

### <span data-ttu-id="10107-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="10107-122">-Skip</span></span>
<span data-ttu-id="10107-123">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="10107-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="10107-124">-Início</span><span class="sxs-lookup"><span data-stu-id="10107-124">-Top</span></span>
<span data-ttu-id="10107-125">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="10107-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="10107-126">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="10107-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="10107-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10107-127">CommonParameters</span></span>
<span data-ttu-id="10107-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10107-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10107-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10107-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10107-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10107-130">INPUTS</span></span>

## <span data-ttu-id="10107-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10107-131">OUTPUTS</span></span>

### <span data-ttu-id="10107-132">Microsoft. AzureStack. Management. subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="10107-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="10107-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10107-133">NOTES</span></span>

## <span data-ttu-id="10107-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10107-134">RELATED LINKS</span></span>

