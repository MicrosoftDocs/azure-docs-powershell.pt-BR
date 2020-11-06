---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: 97f68475ab935df66b67f0cab92466e68732a735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428578"
---
# <span data-ttu-id="c8cc1-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="c8cc1-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="c8cc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="c8cc1-103">Exportar logs que mostram solicitações de API limitada total para esta assinatura na janela de tempo específica.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8cc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8cc1-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8cc1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="c8cc1-106">Isso exporta o número total de chamadas de API do Microsoft. Compute limitadas.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="c8cc1-107">Os logs podem ser ainda mais agregados por três opções: GroupByOperationName, GroupByThrottlePolicy ou GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="c8cc1-108">Observe que esse cmdlet coleta somente logs do CRP.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="c8cc1-109">Para obter uma visão geral da limitação da API do provedor de recursos de computação, consulte https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="c8cc1-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="c8cc1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8cc1-110">EXAMPLES</span></span>

### <span data-ttu-id="c8cc1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8cc1-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="c8cc1-112">Esse comando armazena o total de chamadas de API limitadas do Microsoft. Compute entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI da SAS fornecido, agregados pelo nome da operação.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="c8cc1-113">OS</span><span class="sxs-lookup"><span data-stu-id="c8cc1-113">PARAMETERS</span></span>

### <span data-ttu-id="c8cc1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8cc1-114">-AsJob</span></span>
<span data-ttu-id="c8cc1-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8cc1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8cc1-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="c8cc1-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="c8cc1-117">URI da SAS do contêiner de blob do log ao qual a API LogAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8cc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8cc1-118">-DefaultProfile</span></span>
<span data-ttu-id="c8cc1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8cc1-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="c8cc1-120">-FromTime</span></span>
<span data-ttu-id="c8cc1-121">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="c8cc1-121">From time of the query</span></span>

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

### <span data-ttu-id="c8cc1-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="c8cc1-122">-GroupByOperationName</span></span>
<span data-ttu-id="c8cc1-123">Resultado da consulta de grupo por nome de operação.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="c8cc1-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="c8cc1-124">-GroupByResourceName</span></span>
<span data-ttu-id="c8cc1-125">Resultado da consulta de grupo por nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="c8cc1-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="c8cc1-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="c8cc1-127">Resultado da consulta de grupo por política de limitação aplicada.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="c8cc1-128">-Local</span><span class="sxs-lookup"><span data-stu-id="c8cc1-128">-Location</span></span>
<span data-ttu-id="c8cc1-129">O local no qual o log analítico é consultado.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-129">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cc1-130">-Pela hora</span><span class="sxs-lookup"><span data-stu-id="c8cc1-130">-ToTime</span></span>
<span data-ttu-id="c8cc1-131">Para a hora da consulta</span><span class="sxs-lookup"><span data-stu-id="c8cc1-131">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8cc1-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8cc1-132">-Confirm</span></span>
<span data-ttu-id="c8cc1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8cc1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8cc1-134">-WhatIf</span></span>
<span data-ttu-id="c8cc1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8cc1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8cc1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8cc1-137">CommonParameters</span></span>
<span data-ttu-id="c8cc1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8cc1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8cc1-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8cc1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8cc1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8cc1-140">INPUTS</span></span>

### <span data-ttu-id="c8cc1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c8cc1-141">System.String</span></span>

## <span data-ttu-id="c8cc1-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8cc1-142">OUTPUTS</span></span>

### <span data-ttu-id="c8cc1-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="c8cc1-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="c8cc1-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8cc1-144">NOTES</span></span>

## <span data-ttu-id="c8cc1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8cc1-145">RELATED LINKS</span></span>
