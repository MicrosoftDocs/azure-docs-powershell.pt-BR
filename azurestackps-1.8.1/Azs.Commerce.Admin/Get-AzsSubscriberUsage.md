---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775128"
---
# <span data-ttu-id="89f47-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="89f47-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="89f47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89f47-102">SYNOPSIS</span></span>
<span data-ttu-id="89f47-103">Obter dados de uso de durante o TimeSpan especificado.</span><span class="sxs-lookup"><span data-stu-id="89f47-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="89f47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89f47-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="89f47-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89f47-105">DESCRIPTION</span></span>
<span data-ttu-id="89f47-106">Obter dados de uso de durante o TimeSpan especificado.</span><span class="sxs-lookup"><span data-stu-id="89f47-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="89f47-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89f47-107">EXAMPLES</span></span>

### <span data-ttu-id="89f47-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="89f47-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="89f47-109">Obter dados de uso das últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="89f47-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="89f47-110">OS</span><span class="sxs-lookup"><span data-stu-id="89f47-110">PARAMETERS</span></span>

### <span data-ttu-id="89f47-111">-Subscriberid</span><span class="sxs-lookup"><span data-stu-id="89f47-111">-SubscriberId</span></span>
<span data-ttu-id="89f47-112">O identificador de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="89f47-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="89f47-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="89f47-113">-ReportedStartTime</span></span>
<span data-ttu-id="89f47-114">A hora de início reportada (inclusive).</span><span class="sxs-lookup"><span data-stu-id="89f47-114">The reported start time (inclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f47-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="89f47-115">-AggregationGranularity</span></span>
<span data-ttu-id="89f47-116">A granularidade da agregação.</span><span class="sxs-lookup"><span data-stu-id="89f47-116">The aggregation granularity.</span></span>

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

### <span data-ttu-id="89f47-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="89f47-117">-Skip</span></span>
<span data-ttu-id="89f47-118">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="89f47-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="89f47-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="89f47-119">-ReportedEndTime</span></span>
<span data-ttu-id="89f47-120">A hora de término (exclusivo) informada.</span><span class="sxs-lookup"><span data-stu-id="89f47-120">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f47-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="89f47-121">-ContinuationToken</span></span>
<span data-ttu-id="89f47-122">O token de continuação.</span><span class="sxs-lookup"><span data-stu-id="89f47-122">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f47-123">-Início</span><span class="sxs-lookup"><span data-stu-id="89f47-123">-Top</span></span>
<span data-ttu-id="89f47-124">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="89f47-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="89f47-125">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="89f47-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f47-126">CommonParameters</span></span>
<span data-ttu-id="89f47-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89f47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f47-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f47-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f47-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89f47-129">INPUTS</span></span>

## <span data-ttu-id="89f47-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89f47-130">OUTPUTS</span></span>

### <span data-ttu-id="89f47-131">Microsoft. AzureStack. Management. Commerce. admin. Models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="89f47-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="89f47-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89f47-132">NOTES</span></span>

## <span data-ttu-id="89f47-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89f47-133">RELATED LINKS</span></span>
