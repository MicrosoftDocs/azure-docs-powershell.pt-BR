---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: a8deadf4760950eebbec22626bca475439ab0b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430520"
---
# <span data-ttu-id="a4ba0-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="a4ba0-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="a4ba0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ba0-103">Exportar logs que mostram solicitações de API limitada total para esta assinatura na janela de tempo específica.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4ba0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4ba0-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4ba0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ba0-106">Isso exporta o número total de chamadas de API do Microsoft. Compute limitadas.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="a4ba0-107">Os logs podem ser ainda mais agregados por três opções: GroupByOperationName, GroupByThrottlePolicy ou GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="a4ba0-108">Observe que esse cmdlet coleta somente logs do CRP.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="a4ba0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4ba0-109">EXAMPLES</span></span>

### <span data-ttu-id="a4ba0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4ba0-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="a4ba0-111">Esse comando armazena o total de chamadas de API limitadas do Microsoft. Compute entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI da SAS fornecido, agregados pelo nome da operação.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="a4ba0-112">OS</span><span class="sxs-lookup"><span data-stu-id="a4ba0-112">PARAMETERS</span></span>

### <span data-ttu-id="a4ba0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4ba0-113">-AsJob</span></span>
<span data-ttu-id="a4ba0-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a4ba0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4ba0-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="a4ba0-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="a4ba0-116">URI da SAS do contêiner de blob do log ao qual a API LogAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="a4ba0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ba0-117">-DefaultProfile</span></span>
<span data-ttu-id="a4ba0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ba0-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="a4ba0-119">-FromTime</span></span>
<span data-ttu-id="a4ba0-120">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="a4ba0-120">From time of the query</span></span>

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

### <span data-ttu-id="a4ba0-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="a4ba0-121">-GroupByOperationName</span></span>
<span data-ttu-id="a4ba0-122">Resultado da consulta de grupo por nome de operação.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="a4ba0-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="a4ba0-123">-GroupByResourceName</span></span>
<span data-ttu-id="a4ba0-124">Resultado da consulta de grupo por nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="a4ba0-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="a4ba0-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="a4ba0-126">Resultado da consulta de grupo por política de limitação aplicada.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="a4ba0-127">-Local</span><span class="sxs-lookup"><span data-stu-id="a4ba0-127">-Location</span></span>
<span data-ttu-id="a4ba0-128">O local no qual o log analítico é consultado.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="a4ba0-129">-Pela hora</span><span class="sxs-lookup"><span data-stu-id="a4ba0-129">-ToTime</span></span>
<span data-ttu-id="a4ba0-130">Para a hora da consulta</span><span class="sxs-lookup"><span data-stu-id="a4ba0-130">To time of the query</span></span>

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

### <span data-ttu-id="a4ba0-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a4ba0-131">-Confirm</span></span>
<span data-ttu-id="a4ba0-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ba0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ba0-133">-WhatIf</span></span>
<span data-ttu-id="a4ba0-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ba0-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ba0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ba0-136">CommonParameters</span></span>
<span data-ttu-id="a4ba0-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ba0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ba0-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ba0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ba0-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4ba0-139">INPUTS</span></span>

### <span data-ttu-id="a4ba0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a4ba0-140">System.String</span></span>

## <span data-ttu-id="a4ba0-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4ba0-141">OUTPUTS</span></span>

### <span data-ttu-id="a4ba0-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="a4ba0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="a4ba0-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4ba0-143">NOTES</span></span>

## <span data-ttu-id="a4ba0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4ba0-144">RELATED LINKS</span></span>
