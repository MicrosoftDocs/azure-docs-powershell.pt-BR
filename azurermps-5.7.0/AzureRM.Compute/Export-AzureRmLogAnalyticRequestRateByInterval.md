---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: b5e087bf42a2cb7f19980621c6dd0606471374d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430521"
---
# <span data-ttu-id="2391f-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="2391f-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="2391f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2391f-102">SYNOPSIS</span></span>
<span data-ttu-id="2391f-103">Exportar logs que mostram solicitações de API feitas por essa assinatura na janela de tempo determinada para mostrar as atividades de limitação.</span><span class="sxs-lookup"><span data-stu-id="2391f-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2391f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2391f-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval [-FromTime] <DateTime> [-GroupByOperationName]
 [-IntervalLength] <IntervalInMins> [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String>
 [-GroupByResourceName] [-ToTime] <DateTime> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2391f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2391f-105">DESCRIPTION</span></span>
<span data-ttu-id="2391f-106">Isso exporta os números agregados de chamadas de API do Microsoft. Compute separadas por êxito, falha ou limitação exibidos em intervalos de tempo.</span><span class="sxs-lookup"><span data-stu-id="2391f-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="2391f-107">Os logs podem ser agrupados por três parâmetros: GroupByOperationName, GroupByThrottlePolicy ou GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="2391f-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="2391f-108">Observe que esse cmdlet coleta somente logs do CRP.</span><span class="sxs-lookup"><span data-stu-id="2391f-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="2391f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2391f-109">EXAMPLES</span></span>

### <span data-ttu-id="2391f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2391f-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="2391f-111">Esse comando armazena os números agregados do Microsoft. Compute chamadas de API separadas por sucesso, falha ou limitado entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI de SAS fornecido, agregados pelo nome da operação.</span><span class="sxs-lookup"><span data-stu-id="2391f-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="2391f-112">OS</span><span class="sxs-lookup"><span data-stu-id="2391f-112">PARAMETERS</span></span>

### <span data-ttu-id="2391f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2391f-113">-AsJob</span></span>
<span data-ttu-id="2391f-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2391f-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="2391f-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="2391f-116">URI da SAS do contêiner de blob do log ao qual a API LogAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="2391f-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2391f-117">-DefaultProfile</span></span>
<span data-ttu-id="2391f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2391f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2391f-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="2391f-119">-FromTime</span></span>
<span data-ttu-id="2391f-120">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="2391f-120">From time of the query</span></span>

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

### <span data-ttu-id="2391f-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="2391f-121">-GroupByOperationName</span></span>
<span data-ttu-id="2391f-122">Resultado da consulta de grupo por nome de operação.</span><span class="sxs-lookup"><span data-stu-id="2391f-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="2391f-123">-GroupByResourceName</span></span>
<span data-ttu-id="2391f-124">Resultado da consulta de grupo por nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2391f-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="2391f-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="2391f-126">Resultado da consulta de grupo por política de limitação aplicada.</span><span class="sxs-lookup"><span data-stu-id="2391f-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="2391f-127">-IntervalLength</span></span>
<span data-ttu-id="2391f-128">Valor de intervalo em minutos usado para criar logs de taxa de chamada LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="2391f-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-129">-Local</span><span class="sxs-lookup"><span data-stu-id="2391f-129">-Location</span></span>
<span data-ttu-id="2391f-130">O local no qual o log analítico é consultado.</span><span class="sxs-lookup"><span data-stu-id="2391f-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-131">-Pela hora</span><span class="sxs-lookup"><span data-stu-id="2391f-131">-ToTime</span></span>
<span data-ttu-id="2391f-132">Para a hora da consulta</span><span class="sxs-lookup"><span data-stu-id="2391f-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2391f-133">-Confirm</span></span>
<span data-ttu-id="2391f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2391f-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2391f-135">-WhatIf</span></span>
<span data-ttu-id="2391f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2391f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2391f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2391f-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2391f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2391f-138">CommonParameters</span></span>
<span data-ttu-id="2391f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2391f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2391f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2391f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2391f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2391f-141">INPUTS</span></span>

### <span data-ttu-id="2391f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2391f-142">System.String</span></span>

## <span data-ttu-id="2391f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2391f-143">OUTPUTS</span></span>

### <span data-ttu-id="2391f-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="2391f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="2391f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2391f-145">NOTES</span></span>

## <span data-ttu-id="2391f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2391f-146">RELATED LINKS</span></span>
