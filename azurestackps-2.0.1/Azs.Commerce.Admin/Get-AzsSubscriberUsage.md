---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945344"
---
# <span data-ttu-id="b40bc-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="b40bc-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="b40bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b40bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b40bc-103">Obtém uma coleção de SubscriberUsageAggregates, que são UsageAggregates de usuários.</span><span class="sxs-lookup"><span data-stu-id="b40bc-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="b40bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b40bc-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b40bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b40bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b40bc-106">Obtém uma coleção de SubscriberUsageAggregates, que são UsageAggregates de usuários.</span><span class="sxs-lookup"><span data-stu-id="b40bc-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="b40bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b40bc-107">EXAMPLES</span></span>

### <span data-ttu-id="b40bc-108">Exemplo 1: obter dados de uso agregados por dia</span><span class="sxs-lookup"><span data-stu-id="b40bc-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="b40bc-109">Obtenha os dados de uso do dia inteiro de 30 de dezembro de 2019 (em UTC) para todos os locatários em provedor agregado por dia.</span><span class="sxs-lookup"><span data-stu-id="b40bc-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="b40bc-110">ReportedStartTime e ReportedEndTime devem ser arredondados para dias.</span><span class="sxs-lookup"><span data-stu-id="b40bc-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="b40bc-111">Se chamado como administrador do serviço, isso mostrará efetivamente todos os dados de uso de cada locatário.</span><span class="sxs-lookup"><span data-stu-id="b40bc-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="b40bc-112">Exemplo 2: obter dados de uso agregados por hora</span><span class="sxs-lookup"><span data-stu-id="b40bc-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="b40bc-113">Obtenha os dados de uso entre o 12AM-2AM no dia 30 de dezembro de 2019 (em UTC) agregado por hora.</span><span class="sxs-lookup"><span data-stu-id="b40bc-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="b40bc-114">ReportedStartTime e ReportedEndTime devem ser arredondados para horas.</span><span class="sxs-lookup"><span data-stu-id="b40bc-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="b40bc-115">Da mesma forma, se chamado como administrador do serviço, isso mostrará efetivamente todos os dados de uso de cada locatário.</span><span class="sxs-lookup"><span data-stu-id="b40bc-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="b40bc-116">OS</span><span class="sxs-lookup"><span data-stu-id="b40bc-116">PARAMETERS</span></span>

### <span data-ttu-id="b40bc-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="b40bc-117">-AggregationGranularity</span></span>
<span data-ttu-id="b40bc-118">A granularidade da agregação.</span><span class="sxs-lookup"><span data-stu-id="b40bc-118">The aggregation granularity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b40bc-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b40bc-119">-ContinuationToken</span></span>
<span data-ttu-id="b40bc-120">O token de continuação.</span><span class="sxs-lookup"><span data-stu-id="b40bc-120">The continuation token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b40bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40bc-121">-DefaultProfile</span></span>
<span data-ttu-id="b40bc-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b40bc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b40bc-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="b40bc-123">-ReportedEndTime</span></span>
<span data-ttu-id="b40bc-124">A hora de término (exclusivo) informada.</span><span class="sxs-lookup"><span data-stu-id="b40bc-124">The reported end time (exclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b40bc-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="b40bc-125">-ReportedStartTime</span></span>
<span data-ttu-id="b40bc-126">A hora de início reportada (inclusive).</span><span class="sxs-lookup"><span data-stu-id="b40bc-126">The reported start time (inclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b40bc-127">-Subscriberid</span><span class="sxs-lookup"><span data-stu-id="b40bc-127">-SubscriberId</span></span>
<span data-ttu-id="b40bc-128">O identificador de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="b40bc-128">The tenant subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b40bc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b40bc-129">-SubscriptionId</span></span>
<span data-ttu-id="b40bc-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b40bc-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b40bc-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b40bc-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b40bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40bc-132">CommonParameters</span></span>
<span data-ttu-id="b40bc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40bc-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b40bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40bc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b40bc-135">INPUTS</span></span>

## <span data-ttu-id="b40bc-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b40bc-136">OUTPUTS</span></span>

### <span data-ttu-id="b40bc-137">Microsoft. Azure. PowerShell. cmdlets. Commerce. Models. Api20150601Preview. IUsageAggregate</span><span class="sxs-lookup"><span data-stu-id="b40bc-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="b40bc-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b40bc-138">NOTES</span></span>

## <span data-ttu-id="b40bc-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b40bc-139">RELATED LINKS</span></span>

