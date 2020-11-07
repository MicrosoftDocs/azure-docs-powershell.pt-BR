---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2cb2886e84b42d499fb04693757cee333458f9b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774770"
---
# <span data-ttu-id="568a4-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="568a4-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="568a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="568a4-102">SYNOPSIS</span></span>
<span data-ttu-id="568a4-103">Obtenha uma coleção de todos os planos adquiridos com acesso à assinatura.</span><span class="sxs-lookup"><span data-stu-id="568a4-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="568a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="568a4-104">SYNTAX</span></span>

### <span data-ttu-id="568a4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="568a4-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="568a4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="568a4-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="568a4-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="568a4-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="568a4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="568a4-108">DESCRIPTION</span></span>
<span data-ttu-id="568a4-109">Obtenha uma coleção de todos os planos adquiridos com acesso à assinatura.</span><span class="sxs-lookup"><span data-stu-id="568a4-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="568a4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="568a4-110">EXAMPLES</span></span>

### <span data-ttu-id="568a4-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="568a4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="568a4-112">Obtenha uma coleção de todos os planos adquiridos com acesso à assinatura.</span><span class="sxs-lookup"><span data-stu-id="568a4-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="568a4-113">OS</span><span class="sxs-lookup"><span data-stu-id="568a4-113">PARAMETERS</span></span>

### <span data-ttu-id="568a4-114">-Acquisitionid</span><span class="sxs-lookup"><span data-stu-id="568a4-114">-AcquisitionId</span></span>
<span data-ttu-id="568a4-115">O identificador de aquisição do plano</span><span class="sxs-lookup"><span data-stu-id="568a4-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568a4-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="568a4-116">-ResourceId</span></span>
<span data-ttu-id="568a4-117">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="568a4-117">The resource id.</span></span>

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

### <span data-ttu-id="568a4-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="568a4-118">-Skip</span></span>
<span data-ttu-id="568a4-119">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="568a4-119">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="568a4-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="568a4-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="568a4-121">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="568a4-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="568a4-122">-Início</span><span class="sxs-lookup"><span data-stu-id="568a4-122">-Top</span></span>
<span data-ttu-id="568a4-123">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="568a4-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="568a4-124">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="568a4-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="568a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568a4-125">CommonParameters</span></span>
<span data-ttu-id="568a4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="568a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568a4-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="568a4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568a4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="568a4-128">INPUTS</span></span>

## <span data-ttu-id="568a4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="568a4-129">OUTPUTS</span></span>

### <span data-ttu-id="568a4-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="568a4-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="568a4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="568a4-131">NOTES</span></span>

## <span data-ttu-id="568a4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="568a4-132">RELATED LINKS</span></span>
