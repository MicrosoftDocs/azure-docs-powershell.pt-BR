---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116952"
---
# <span data-ttu-id="69753-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="69753-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="69753-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69753-102">SYNOPSIS</span></span>
<span data-ttu-id="69753-103">Obtém os detalhes de uso da assinatura do Azure relatados.</span><span class="sxs-lookup"><span data-stu-id="69753-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="69753-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69753-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69753-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="69753-105">DESCRIPTION</span></span>
<span data-ttu-id="69753-106">O **cmdlet Get-UsageAggregates** obtém dados agregados de uso da assinatura do Azure pelas seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="69753-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="69753-107">Horários de início e término de quando o uso foi relatado.</span><span class="sxs-lookup"><span data-stu-id="69753-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="69753-108">Precisão de agregação, diariamente ou por hora.</span><span class="sxs-lookup"><span data-stu-id="69753-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="69753-109">Detalhes do nível de instância para várias instâncias do mesmo recurso.</span><span class="sxs-lookup"><span data-stu-id="69753-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="69753-110">Para obter resultados consistentes, os dados retornados são baseados em quando os detalhes de uso foram relatados pelo recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="69753-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="69753-111">Para obter mais informações, consulte Referência da API REST de Cobrança do Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( na biblioteca do Microsoft Developer https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Network.</span><span class="sxs-lookup"><span data-stu-id="69753-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="69753-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="69753-112">EXAMPLES</span></span>

### <span data-ttu-id="69753-113">Exemplo 1: Recuperar dados da assinatura</span><span class="sxs-lookup"><span data-stu-id="69753-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="69753-114">Esse comando recupera os dados de uso relatados da assinatura entre 02/05/2015 e 05/05/2015.</span><span class="sxs-lookup"><span data-stu-id="69753-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="69753-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69753-115">PARAMETERS</span></span>

### <span data-ttu-id="69753-116">-AggregationArularity</span><span class="sxs-lookup"><span data-stu-id="69753-116">-AggregationGranularity</span></span>
<span data-ttu-id="69753-117">Especifica a precisão de agregação dos dados.</span><span class="sxs-lookup"><span data-stu-id="69753-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="69753-118">Os valores válidos são: Diário e Hora.</span><span class="sxs-lookup"><span data-stu-id="69753-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="69753-119">O valor padrão é Diário.</span><span class="sxs-lookup"><span data-stu-id="69753-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69753-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="69753-120">-ContinuationToken</span></span>
<span data-ttu-id="69753-121">Especifica o token de continuação que foi recuperado do corpo da resposta na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="69753-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="69753-122">Para um grande conjunto de resultados, as respostas são páginas usando tokens de continuação.</span><span class="sxs-lookup"><span data-stu-id="69753-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="69753-123">O token de continuação serve como um indicador para o progresso.</span><span class="sxs-lookup"><span data-stu-id="69753-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="69753-124">Se você não especificar esse parâmetro, os dados serão recuperados do início do dia ou da hora especificados no *ReportedStartTime.*</span><span class="sxs-lookup"><span data-stu-id="69753-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="69753-125">Recomendamos que você siga o próximo link na resposta à página, embora os dados.</span><span class="sxs-lookup"><span data-stu-id="69753-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="69753-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69753-126">-DefaultProfile</span></span>
<span data-ttu-id="69753-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="69753-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69753-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="69753-128">-ReportedEndTime</span></span>
<span data-ttu-id="69753-129">Especifica a hora de término relatada para quando o uso do recurso foi registrado no sistema de cobrança do Azure.</span><span class="sxs-lookup"><span data-stu-id="69753-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="69753-130">O Azure é um sistema distribuído, abrangendo vários datacenters em todo o mundo, portanto, há um atraso entre quando o recurso foi realmente consumido, que é o tempo de uso do recurso e quando o evento de uso atingiu o sistema de cobrança, que é o tempo relatado pelo uso do recurso.</span><span class="sxs-lookup"><span data-stu-id="69753-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="69753-131">Para obter todos os eventos de uso de uma assinatura que são relatados por um período de tempo, você consulta por hora relatada.</span><span class="sxs-lookup"><span data-stu-id="69753-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="69753-132">Mesmo que você consulte por hora reportada, o cmdlet agrega os dados de resposta pelo tempo de uso do recurso.</span><span class="sxs-lookup"><span data-stu-id="69753-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="69753-133">Os dados de uso de recursos são o pivô útil para analisar os dados.</span><span class="sxs-lookup"><span data-stu-id="69753-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="69753-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="69753-134">-ReportedStartTime</span></span>
<span data-ttu-id="69753-135">Especifica a hora de início relatada para quando o uso do recurso foi registrado no sistema de cobrança do Azure.</span><span class="sxs-lookup"><span data-stu-id="69753-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="69753-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="69753-136">-ShowDetails</span></span>
<span data-ttu-id="69753-137">Indica se esse cmdlet retorna detalhes no nível da instância com os dados de uso.</span><span class="sxs-lookup"><span data-stu-id="69753-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="69753-138">O valor padrão é $True.</span><span class="sxs-lookup"><span data-stu-id="69753-138">The default value is $True.</span></span>
<span data-ttu-id="69753-139">Se $False, o serviço agrega os resultados no lado do servidor e, portanto, retorna menos grupos agregados.</span><span class="sxs-lookup"><span data-stu-id="69753-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="69753-140">Por exemplo, se você estiver executando três sites, por padrão, receberá três itens de linha para consumo de site.</span><span class="sxs-lookup"><span data-stu-id="69753-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="69753-141">No entanto, quando o valor é $False, todos os dados para a mesma **ID** de assinatura, **meterId,** **usageStartTime** e **usageEndTime** são recolhidos em um único item de linha.</span><span class="sxs-lookup"><span data-stu-id="69753-141">However, when the value is $False, all the data for the same **subscriptionId**, **meterId**, **usageStartTime**, and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69753-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69753-142">CommonParameters</span></span>
<span data-ttu-id="69753-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69753-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69753-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69753-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69753-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="69753-145">INPUTS</span></span>

### <span data-ttu-id="69753-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="69753-146">None</span></span>

## <span data-ttu-id="69753-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="69753-147">OUTPUTS</span></span>

### <span data-ttu-id="69753-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="69753-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="69753-149">Notas</span><span class="sxs-lookup"><span data-stu-id="69753-149">NOTES</span></span>

## <span data-ttu-id="69753-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69753-150">RELATED LINKS</span></span>
