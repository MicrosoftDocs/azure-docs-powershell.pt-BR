---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946909"
---
# <span data-ttu-id="1e848-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="1e848-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="1e848-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e848-102">SYNOPSIS</span></span>
<span data-ttu-id="1e848-103">Obter a lista de ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="1e848-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="1e848-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e848-104">SYNTAX</span></span>

### <span data-ttu-id="1e848-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e848-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e848-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1e848-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="1e848-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="1e848-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1e848-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e848-108">DESCRIPTION</span></span>
<span data-ttu-id="1e848-109">Obter a lista de ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="1e848-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="1e848-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e848-110">EXAMPLES</span></span>

### <span data-ttu-id="1e848-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e848-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="1e848-112">Obter a lista de ofertas de provedor delegado.</span><span class="sxs-lookup"><span data-stu-id="1e848-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="1e848-113">OS</span><span class="sxs-lookup"><span data-stu-id="1e848-113">PARAMETERS</span></span>

### <span data-ttu-id="1e848-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="1e848-114">-DelegatedProviderId</span></span>
<span data-ttu-id="1e848-115">Identificador DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="1e848-115">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="1e848-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e848-116">-Name</span></span>
<span data-ttu-id="1e848-117">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="1e848-117">Name of an offer.</span></span>

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

### <span data-ttu-id="1e848-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e848-118">-ResourceId</span></span>
<span data-ttu-id="1e848-119">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e848-119">The resource id.</span></span>

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

### <span data-ttu-id="1e848-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="1e848-120">-Skip</span></span>
<span data-ttu-id="1e848-121">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1e848-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1e848-122">-Início</span><span class="sxs-lookup"><span data-stu-id="1e848-122">-Top</span></span>
<span data-ttu-id="1e848-123">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1e848-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1e848-124">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="1e848-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1e848-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e848-125">CommonParameters</span></span>
<span data-ttu-id="1e848-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e848-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e848-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e848-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e848-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e848-128">INPUTS</span></span>

## <span data-ttu-id="1e848-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e848-129">OUTPUTS</span></span>

### <span data-ttu-id="1e848-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. DelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="1e848-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="1e848-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e848-131">NOTES</span></span>

## <span data-ttu-id="1e848-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e848-132">RELATED LINKS</span></span>

