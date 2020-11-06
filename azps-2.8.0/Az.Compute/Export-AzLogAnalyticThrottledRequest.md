---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: f4d9f8e6bb9c5592d9558aa03cfba6cd88bd38fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597491"
---
# <span data-ttu-id="a9852-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="a9852-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="a9852-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9852-102">SYNOPSIS</span></span>
<span data-ttu-id="a9852-103">Exportar logs que mostram solicitações de API limitada total para esta assinatura na janela de tempo específica.</span><span class="sxs-lookup"><span data-stu-id="a9852-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="a9852-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9852-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9852-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9852-105">DESCRIPTION</span></span>
<span data-ttu-id="a9852-106">Isso exporta o número total de chamadas de API do Microsoft. Compute limitadas.</span><span class="sxs-lookup"><span data-stu-id="a9852-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="a9852-107">Os logs podem ser ainda mais agregados por três opções: GroupByOperationName, GroupByThrottlePolicy ou GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="a9852-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="a9852-108">Observe que esse cmdlet coleta somente logs do CRP.</span><span class="sxs-lookup"><span data-stu-id="a9852-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="a9852-109">Para obter uma visão geral da limitação da API do provedor de recursos de computação, consulte https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="a9852-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="a9852-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9852-110">EXAMPLES</span></span>

### <span data-ttu-id="a9852-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9852-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="a9852-112">Esse comando armazena o total de chamadas de API limitadas do Microsoft. Compute entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI da SAS fornecido, agregados pelo nome da operação.</span><span class="sxs-lookup"><span data-stu-id="a9852-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="a9852-113">OS</span><span class="sxs-lookup"><span data-stu-id="a9852-113">PARAMETERS</span></span>

### <span data-ttu-id="a9852-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9852-114">-AsJob</span></span>
<span data-ttu-id="a9852-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a9852-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9852-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="a9852-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="a9852-117">URI da SAS do contêiner de blob do log ao qual a API LogAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="a9852-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="a9852-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9852-118">-DefaultProfile</span></span>
<span data-ttu-id="a9852-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9852-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9852-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="a9852-120">-FromTime</span></span>
<span data-ttu-id="a9852-121">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="a9852-121">From time of the query</span></span>

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

### <span data-ttu-id="a9852-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="a9852-122">-GroupByOperationName</span></span>
<span data-ttu-id="a9852-123">Resultado da consulta de grupo por nome de operação.</span><span class="sxs-lookup"><span data-stu-id="a9852-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="a9852-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="a9852-124">-GroupByResourceName</span></span>
<span data-ttu-id="a9852-125">Resultado da consulta de grupo por nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a9852-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="a9852-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="a9852-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="a9852-127">Resultado da consulta de grupo por política de limitação aplicada.</span><span class="sxs-lookup"><span data-stu-id="a9852-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="a9852-128">-Local</span><span class="sxs-lookup"><span data-stu-id="a9852-128">-Location</span></span>
<span data-ttu-id="a9852-129">O local no qual o log analítico é consultado.</span><span class="sxs-lookup"><span data-stu-id="a9852-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="a9852-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a9852-130">-NoWait</span></span>
<span data-ttu-id="a9852-131">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a9852-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a9852-132">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="a9852-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a9852-133">-Pela hora</span><span class="sxs-lookup"><span data-stu-id="a9852-133">-ToTime</span></span>
<span data-ttu-id="a9852-134">Para a hora da consulta</span><span class="sxs-lookup"><span data-stu-id="a9852-134">To time of the query</span></span>

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

### <span data-ttu-id="a9852-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9852-135">-Confirm</span></span>
<span data-ttu-id="a9852-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9852-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9852-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9852-137">-WhatIf</span></span>
<span data-ttu-id="a9852-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9852-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9852-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9852-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9852-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9852-140">CommonParameters</span></span>
<span data-ttu-id="a9852-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9852-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9852-142">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9852-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9852-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9852-143">INPUTS</span></span>

### <span data-ttu-id="a9852-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a9852-144">System.String</span></span>

## <span data-ttu-id="a9852-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9852-145">OUTPUTS</span></span>

### <span data-ttu-id="a9852-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="a9852-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="a9852-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9852-147">NOTES</span></span>

## <span data-ttu-id="a9852-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9852-148">RELATED LINKS</span></span>
