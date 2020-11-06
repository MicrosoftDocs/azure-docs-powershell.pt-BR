---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.usageaggregates/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
ms.openlocfilehash: 291520e17fa1508f706e7f7773d44bc768b285f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609473"
---
# <span data-ttu-id="f66f6-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="f66f6-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="f66f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f66f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f66f6-103">Obtém os detalhes de uso da assinatura do Azure relatados.</span><span class="sxs-lookup"><span data-stu-id="f66f6-103">Gets the reported Azure subscription usage details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f66f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f66f6-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f66f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f66f6-105">DESCRIPTION</span></span>
<span data-ttu-id="f66f6-106">O cmdlet **Get-UsageAggregates** obtém dados de uso da assinatura do Azure agregados nas seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="f66f6-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 

- <span data-ttu-id="f66f6-107">Horários de início e término de quando o uso foi relatado.</span><span class="sxs-lookup"><span data-stu-id="f66f6-107">Start and end times of when the usage was reported.</span></span>

- <span data-ttu-id="f66f6-108">A precisão da agregação, diária ou por hora.</span><span class="sxs-lookup"><span data-stu-id="f66f6-108">Aggregation precision, either daily or hourly.</span></span>

- <span data-ttu-id="f66f6-109">Detalhe o nível de instância para várias instâncias do mesmo recurso.</span><span class="sxs-lookup"><span data-stu-id="f66f6-109">Instance level detail for multiple instances of the same resource.</span></span>

<span data-ttu-id="f66f6-110">Para resultados consistentes, os dados retornados se baseiam quando os detalhes de uso foram relatados pelo recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="f66f6-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>

<span data-ttu-id="f66f6-111">Para obter mais informações, consulte referência da API REST de cobrança do Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) na biblioteca Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="f66f6-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="f66f6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f66f6-112">EXAMPLES</span></span>

### <span data-ttu-id="f66f6-113">Exemplo 1: recuperar dados de assinatura</span><span class="sxs-lookup"><span data-stu-id="f66f6-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="f66f6-114">Esse comando recupera os dados de uso relatados para a assinatura entre o 5/2/2015 e o 5/5/2015.</span><span class="sxs-lookup"><span data-stu-id="f66f6-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="f66f6-115">OS</span><span class="sxs-lookup"><span data-stu-id="f66f6-115">PARAMETERS</span></span>

### <span data-ttu-id="f66f6-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="f66f6-116">-AggregationGranularity</span></span>
<span data-ttu-id="f66f6-117">Especifica a precisão da agregação dos dados.</span><span class="sxs-lookup"><span data-stu-id="f66f6-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="f66f6-118">Os valores válidos são: diariamente e por hora.</span><span class="sxs-lookup"><span data-stu-id="f66f6-118">Valid values are: Daily and Hourly.</span></span>

<span data-ttu-id="f66f6-119">O valor padrão é diário.</span><span class="sxs-lookup"><span data-stu-id="f66f6-119">The default value is Daily.</span></span>

```yaml
Type: AggregationGranularity
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66f6-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="f66f6-120">-ContinuationToken</span></span>
<span data-ttu-id="f66f6-121">Especifica o token de continuação que foi recuperado do corpo da resposta na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="f66f6-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="f66f6-122">Para um grande conjunto de resultados, as respostas são paginadas usando-se tokens de continuação.</span><span class="sxs-lookup"><span data-stu-id="f66f6-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="f66f6-123">O token de continuação funciona como um indicador para progresso.</span><span class="sxs-lookup"><span data-stu-id="f66f6-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="f66f6-124">Se você não especificar esse parâmetro, os dados serão recuperados do início do dia ou da hora especificado em *ReportedStartTime*.</span><span class="sxs-lookup"><span data-stu-id="f66f6-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="f66f6-125">Recomendamos que você siga o próximo link na página resposta a, apesar dos dados.</span><span class="sxs-lookup"><span data-stu-id="f66f6-125">We recommend that you follow the next link in the response to page though the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66f6-126">-DefaultProfile</span></span>
<span data-ttu-id="f66f6-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f66f6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66f6-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="f66f6-128">-ReportedEndTime</span></span>
<span data-ttu-id="f66f6-129">Especifica a hora de término informada para quando o uso do recurso foi registrado no sistema de cobrança do Azure.</span><span class="sxs-lookup"><span data-stu-id="f66f6-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>

<span data-ttu-id="f66f6-130">O Azure é um sistema distribuído, abrangendo vários datacenters em todo o mundo, portanto há um atraso entre o momento em que o recurso foi realmente consumido, que é o tempo de uso do recurso e quando o evento de uso atinge o sistema de cobrança, que é o tempo informado sobre o uso do recurso.</span><span class="sxs-lookup"><span data-stu-id="f66f6-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="f66f6-131">Para obter todos os eventos de uso de uma assinatura reportada por um período de tempo, você consulta por hora reportada.</span><span class="sxs-lookup"><span data-stu-id="f66f6-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="f66f6-132">Apesar de você consultar por tempo informado, o cmdlet agrega os dados de resposta pelo tempo de uso do recurso.</span><span class="sxs-lookup"><span data-stu-id="f66f6-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="f66f6-133">Os dados de uso dos recursos são o pivô útil para a análise dos dados.</span><span class="sxs-lookup"><span data-stu-id="f66f6-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66f6-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="f66f6-134">-ReportedStartTime</span></span>
<span data-ttu-id="f66f6-135">Especifica a hora de início relatada para quando o uso do recurso foi registrado no sistema de cobrança do Azure.</span><span class="sxs-lookup"><span data-stu-id="f66f6-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66f6-136">-Detalhes do</span><span class="sxs-lookup"><span data-stu-id="f66f6-136">-ShowDetails</span></span>
<span data-ttu-id="f66f6-137">Indica se esse cmdlet retorna detalhes em nível de instância com os dados de uso.</span><span class="sxs-lookup"><span data-stu-id="f66f6-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>

<span data-ttu-id="f66f6-138">O valor padrão é $True.</span><span class="sxs-lookup"><span data-stu-id="f66f6-138">The default value is $True.</span></span>

<span data-ttu-id="f66f6-139">Se $False, o serviço agregará os resultados no lado do servidor e, portanto, retornará menos grupos de agregação.</span><span class="sxs-lookup"><span data-stu-id="f66f6-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="f66f6-140">Por exemplo, se você estiver executando três sites, por padrão, receberá três itens de linha para o consumo de site.</span><span class="sxs-lookup"><span data-stu-id="f66f6-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="f66f6-141">No entanto, quando o valor é $False, todos os dados para o mesmo **SubscriptionId** , **meterid** , **usageStartTime** e **usageEndTime** são recolhidos em um único item de linha.</span><span class="sxs-lookup"><span data-stu-id="f66f6-141">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66f6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66f6-142">CommonParameters</span></span>
<span data-ttu-id="f66f6-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f66f6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66f6-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f66f6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66f6-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f66f6-145">INPUTS</span></span>

### <span data-ttu-id="f66f6-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f66f6-146">None</span></span>
<span data-ttu-id="f66f6-147">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f66f6-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f66f6-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f66f6-148">OUTPUTS</span></span>

### <span data-ttu-id="f66f6-149">Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="f66f6-149">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="f66f6-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f66f6-150">NOTES</span></span>

## <span data-ttu-id="f66f6-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f66f6-151">RELATED LINKS</span></span>

