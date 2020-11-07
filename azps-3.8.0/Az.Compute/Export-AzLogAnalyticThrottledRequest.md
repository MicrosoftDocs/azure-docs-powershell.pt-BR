---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944645"
---
# <span data-ttu-id="04dbd-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="04dbd-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="04dbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="04dbd-103">Exportar logs que mostram solicitações de API limitada total para esta assinatura na janela de tempo específica.</span><span class="sxs-lookup"><span data-stu-id="04dbd-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="04dbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04dbd-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04dbd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="04dbd-106">Isso exporta o número total de chamadas de API do Microsoft. Compute limitadas.</span><span class="sxs-lookup"><span data-stu-id="04dbd-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="04dbd-107">Os logs podem ser ainda mais agregados por três opções: GroupByOperationName, GroupByThrottlePolicy ou GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="04dbd-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="04dbd-108">Observe que esse cmdlet coleta somente logs do CRP.</span><span class="sxs-lookup"><span data-stu-id="04dbd-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="04dbd-109">Para obter uma visão geral da limitação da API do provedor de recursos de computação, consulte https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="04dbd-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="04dbd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04dbd-110">EXAMPLES</span></span>

### <span data-ttu-id="04dbd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04dbd-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="04dbd-112">Esse comando armazena o total de chamadas de API limitadas do Microsoft. Compute entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI da SAS fornecido, agregados pelo nome da operação.</span><span class="sxs-lookup"><span data-stu-id="04dbd-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="04dbd-113">OS</span><span class="sxs-lookup"><span data-stu-id="04dbd-113">PARAMETERS</span></span>

### <span data-ttu-id="04dbd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04dbd-114">-AsJob</span></span>
<span data-ttu-id="04dbd-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="04dbd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04dbd-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="04dbd-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="04dbd-117">URI da SAS do contêiner de blob do log ao qual a API LogAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="04dbd-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="04dbd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04dbd-118">-DefaultProfile</span></span>
<span data-ttu-id="04dbd-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04dbd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04dbd-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="04dbd-120">-FromTime</span></span>
<span data-ttu-id="04dbd-121">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="04dbd-121">From time of the query</span></span>

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

### <span data-ttu-id="04dbd-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="04dbd-122">-GroupByOperationName</span></span>
<span data-ttu-id="04dbd-123">Resultado da consulta de grupo por nome de operação.</span><span class="sxs-lookup"><span data-stu-id="04dbd-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="04dbd-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="04dbd-124">-GroupByResourceName</span></span>
<span data-ttu-id="04dbd-125">Resultado da consulta de grupo por nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="04dbd-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="04dbd-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="04dbd-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="04dbd-127">Resultado da consulta de grupo por política de limitação aplicada.</span><span class="sxs-lookup"><span data-stu-id="04dbd-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="04dbd-128">-Local</span><span class="sxs-lookup"><span data-stu-id="04dbd-128">-Location</span></span>
<span data-ttu-id="04dbd-129">O local no qual o log analítico é consultado.</span><span class="sxs-lookup"><span data-stu-id="04dbd-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="04dbd-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="04dbd-130">-NoWait</span></span>
<span data-ttu-id="04dbd-131">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="04dbd-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="04dbd-132">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="04dbd-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="04dbd-133">-Pela hora</span><span class="sxs-lookup"><span data-stu-id="04dbd-133">-ToTime</span></span>
<span data-ttu-id="04dbd-134">Para a hora da consulta</span><span class="sxs-lookup"><span data-stu-id="04dbd-134">To time of the query</span></span>

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

### <span data-ttu-id="04dbd-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04dbd-135">-Confirm</span></span>
<span data-ttu-id="04dbd-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04dbd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04dbd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04dbd-137">-WhatIf</span></span>
<span data-ttu-id="04dbd-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04dbd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04dbd-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04dbd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04dbd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04dbd-140">CommonParameters</span></span>
<span data-ttu-id="04dbd-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04dbd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04dbd-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04dbd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04dbd-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04dbd-143">INPUTS</span></span>

### <span data-ttu-id="04dbd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="04dbd-144">System.String</span></span>

## <span data-ttu-id="04dbd-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04dbd-145">OUTPUTS</span></span>

### <span data-ttu-id="04dbd-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="04dbd-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="04dbd-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04dbd-147">NOTES</span></span>

## <span data-ttu-id="04dbd-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04dbd-148">RELATED LINKS</span></span>
