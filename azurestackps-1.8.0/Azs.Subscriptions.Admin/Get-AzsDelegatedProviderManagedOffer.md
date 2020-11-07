---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774787"
---
# <span data-ttu-id="76ffe-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="76ffe-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="76ffe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="76ffe-103">Obter a lista de ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="76ffe-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="76ffe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76ffe-104">SYNTAX</span></span>

### <span data-ttu-id="76ffe-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="76ffe-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="76ffe-106">Obter</span><span class="sxs-lookup"><span data-stu-id="76ffe-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="76ffe-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="76ffe-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="76ffe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76ffe-108">DESCRIPTION</span></span>
<span data-ttu-id="76ffe-109">Obter a lista de ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="76ffe-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="76ffe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76ffe-110">EXAMPLES</span></span>

### <span data-ttu-id="76ffe-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="76ffe-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="76ffe-112">Obter a lista de ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="76ffe-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="76ffe-113">OS</span><span class="sxs-lookup"><span data-stu-id="76ffe-113">PARAMETERS</span></span>

### <span data-ttu-id="76ffe-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="76ffe-114">-DelegatedProviderId</span></span>
<span data-ttu-id="76ffe-115">Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="76ffe-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ffe-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="76ffe-116">-Name</span></span>
<span data-ttu-id="76ffe-117">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="76ffe-117">Name of an offer.</span></span>

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

### <span data-ttu-id="76ffe-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76ffe-118">-ResourceId</span></span>
<span data-ttu-id="76ffe-119">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="76ffe-119">The resource id.</span></span>

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

### <span data-ttu-id="76ffe-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="76ffe-120">-Skip</span></span>
<span data-ttu-id="76ffe-121">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="76ffe-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="76ffe-122">-Início</span><span class="sxs-lookup"><span data-stu-id="76ffe-122">-Top</span></span>
<span data-ttu-id="76ffe-123">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="76ffe-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="76ffe-124">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="76ffe-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="76ffe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ffe-125">CommonParameters</span></span>
<span data-ttu-id="76ffe-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ffe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ffe-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ffe-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ffe-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76ffe-128">INPUTS</span></span>

## <span data-ttu-id="76ffe-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76ffe-129">OUTPUTS</span></span>

### <span data-ttu-id="76ffe-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="76ffe-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="76ffe-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76ffe-131">NOTES</span></span>

## <span data-ttu-id="76ffe-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76ffe-132">RELATED LINKS</span></span>

