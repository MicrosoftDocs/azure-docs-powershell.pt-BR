---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: f6bef7bc90f63ec5a421c0b78a87ea5ec8618053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601365"
---
# <span data-ttu-id="dcc02-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="dcc02-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="dcc02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcc02-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc02-103">Exportar logs que mostram solicitações de API feitas por essa assinatura na janela de tempo determinada para mostrar as atividades de limitação.</span><span class="sxs-lookup"><span data-stu-id="dcc02-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="dcc02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcc02-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcc02-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcc02-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc02-106">Exporta dados estatísticos sobre as chamadas da assinatura para a API Microsoft. Compute por êxito, falha ou status limitado em intervalos de tempo predefinidos.</span><span class="sxs-lookup"><span data-stu-id="dcc02-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="dcc02-107">Os logs podem ser agrupados por três parâmetros: GroupByOperationName, GroupByThrottlePolicy ou GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="dcc02-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="dcc02-108">Observe que esse cmdlet coleta apenas logs do provedor de recursos de computação; Além disso, os dados sobre os tipos de recursos de disco e instantâneo ainda não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dcc02-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="dcc02-109">Para obter uma visão geral da limitação da API do provedor de recursos de computação, consulte https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="dcc02-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="dcc02-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcc02-110">EXAMPLES</span></span>

### <span data-ttu-id="dcc02-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcc02-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="dcc02-112">Esse comando armazena os números agregados do Microsoft. Compute chamadas de API separadas por sucesso, falha ou limitado entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI de SAS fornecido, agregados pelo nome da operação.</span><span class="sxs-lookup"><span data-stu-id="dcc02-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="dcc02-113">OS</span><span class="sxs-lookup"><span data-stu-id="dcc02-113">PARAMETERS</span></span>

### <span data-ttu-id="dcc02-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcc02-114">-AsJob</span></span>
<span data-ttu-id="dcc02-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dcc02-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="dcc02-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="dcc02-117">URI da SAS do contêiner de blob do log ao qual a API LogAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="dcc02-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc02-118">-DefaultProfile</span></span>
<span data-ttu-id="dcc02-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc02-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcc02-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="dcc02-120">-FromTime</span></span>
<span data-ttu-id="dcc02-121">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="dcc02-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="dcc02-122">-GroupByOperationName</span></span>
<span data-ttu-id="dcc02-123">Resultado da consulta de grupo por nome de operação.</span><span class="sxs-lookup"><span data-stu-id="dcc02-123">Group query result by Operation Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="dcc02-124">-GroupByResourceName</span></span>
<span data-ttu-id="dcc02-125">Resultado da consulta de grupo por nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dcc02-125">Group query result by Resource Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="dcc02-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="dcc02-127">Resultado da consulta de grupo por política de limitação aplicada.</span><span class="sxs-lookup"><span data-stu-id="dcc02-127">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="dcc02-128">-IntervalLength</span></span>
<span data-ttu-id="dcc02-129">Valor de intervalo em minutos usado para criar logs de taxa de chamada LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="dcc02-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-130">-Local</span><span class="sxs-lookup"><span data-stu-id="dcc02-130">-Location</span></span>
<span data-ttu-id="dcc02-131">O local no qual o log analítico é consultado.</span><span class="sxs-lookup"><span data-stu-id="dcc02-131">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-132">-Pela hora</span><span class="sxs-lookup"><span data-stu-id="dcc02-132">-ToTime</span></span>
<span data-ttu-id="dcc02-133">Para a hora da consulta</span><span class="sxs-lookup"><span data-stu-id="dcc02-133">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dcc02-134">-Confirm</span></span>
<span data-ttu-id="dcc02-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcc02-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc02-136">-WhatIf</span></span>
<span data-ttu-id="dcc02-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dcc02-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc02-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dcc02-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc02-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc02-139">CommonParameters</span></span>
<span data-ttu-id="dcc02-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc02-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc02-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc02-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc02-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcc02-142">INPUTS</span></span>

### <span data-ttu-id="dcc02-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc02-143">System.String</span></span>

## <span data-ttu-id="dcc02-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcc02-144">OUTPUTS</span></span>

### <span data-ttu-id="dcc02-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="dcc02-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="dcc02-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcc02-146">NOTES</span></span>

## <span data-ttu-id="dcc02-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcc02-147">RELATED LINKS</span></span>
