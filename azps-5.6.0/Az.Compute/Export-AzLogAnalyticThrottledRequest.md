---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 02d78a36bcd2afc6eef037a0b043c5db89d37f0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887561"
---
# <span data-ttu-id="4de45-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="4de45-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="4de45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de45-102">SYNOPSIS</span></span>
<span data-ttu-id="4de45-103">Exportar logs que mostram o total de solicitações de Api aceleradas para essa assinatura na janela de tempo determinado.</span><span class="sxs-lookup"><span data-stu-id="4de45-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="4de45-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4de45-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de45-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4de45-105">DESCRIPTION</span></span>
<span data-ttu-id="4de45-106">Isso exporta o número total de chamadas de API Microsoft.Compute aceleradas.</span><span class="sxs-lookup"><span data-stu-id="4de45-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="4de45-107">Os logs podem ser agregados ainda mais por cinco opções: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent ou GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="4de45-107">The logs can be further aggregated by five options: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="4de45-108">Observe que este cmdlet coleta apenas logs CRP.</span><span class="sxs-lookup"><span data-stu-id="4de45-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="4de45-109">Para uma visão geral da configuração da API do Provedor de Recursos de Computação, consulte https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="4de45-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="4de45-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4de45-110">EXAMPLES</span></span>

### <span data-ttu-id="4de45-111">Exemplo 1: Exportar registros agregados pelo nome da operação</span><span class="sxs-lookup"><span data-stu-id="4de45-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="4de45-112">Este comando armazena o total de chamadas da API Microsoft.Compute controladas entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado pelo nome da operação.</span><span class="sxs-lookup"><span data-stu-id="4de45-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="4de45-113">Exemplo 2: Exportar registros agregados por id de aplicativo</span><span class="sxs-lookup"><span data-stu-id="4de45-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="4de45-114">Este comando armazena o total de chamadas da API Microsoft.Compute controladas entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado por id de aplicação.</span><span class="sxs-lookup"><span data-stu-id="4de45-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="4de45-115">Exemplo 3: Exportar registros agregados pelo agente do usuário</span><span class="sxs-lookup"><span data-stu-id="4de45-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="4de45-116">Este comando armazena o total de chamadas da API Microsoft.Compute aceleradas entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado pelo agente de usuário.</span><span class="sxs-lookup"><span data-stu-id="4de45-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="4de45-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4de45-117">PARAMETERS</span></span>

### <span data-ttu-id="4de45-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4de45-118">-AsJob</span></span>
<span data-ttu-id="4de45-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4de45-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4de45-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="4de45-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="4de45-121">Uri SAS do contêiner de blob de registro em log para o qual a Api LogAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="4de45-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="4de45-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de45-122">-DefaultProfile</span></span>
<span data-ttu-id="4de45-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4de45-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4de45-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="4de45-124">-FromTime</span></span>
<span data-ttu-id="4de45-125">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="4de45-125">From time of the query</span></span>

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

### <span data-ttu-id="4de45-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="4de45-126">-GroupByApplicationId</span></span>
<span data-ttu-id="4de45-127">Resultado da consulta de grupo por ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4de45-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="4de45-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="4de45-128">-GroupByOperationName</span></span>
<span data-ttu-id="4de45-129">Resultado da consulta de grupo por Nome da Operação.</span><span class="sxs-lookup"><span data-stu-id="4de45-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="4de45-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="4de45-130">-GroupByResourceName</span></span>
<span data-ttu-id="4de45-131">Resultado da consulta de grupo pelo Nome do Recurso.</span><span class="sxs-lookup"><span data-stu-id="4de45-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="4de45-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="4de45-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="4de45-133">Resultado da consulta de grupo pela Política de Aceleração aplicada.</span><span class="sxs-lookup"><span data-stu-id="4de45-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="4de45-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="4de45-134">-GroupByUserAgent</span></span>
<span data-ttu-id="4de45-135">Resultado da consulta de grupo por UserAgent.</span><span class="sxs-lookup"><span data-stu-id="4de45-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="4de45-136">-Location</span><span class="sxs-lookup"><span data-stu-id="4de45-136">-Location</span></span>
<span data-ttu-id="4de45-137">O local no qual o log é consultado.</span><span class="sxs-lookup"><span data-stu-id="4de45-137">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="4de45-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4de45-138">-NoWait</span></span>
<span data-ttu-id="4de45-139">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4de45-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4de45-140">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="4de45-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4de45-141">-ToTime</span><span class="sxs-lookup"><span data-stu-id="4de45-141">-ToTime</span></span>
<span data-ttu-id="4de45-142">Até a hora da consulta</span><span class="sxs-lookup"><span data-stu-id="4de45-142">To time of the query</span></span>

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

### <span data-ttu-id="4de45-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4de45-143">-Confirm</span></span>
<span data-ttu-id="4de45-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4de45-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de45-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de45-145">-WhatIf</span></span>
<span data-ttu-id="4de45-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4de45-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de45-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4de45-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de45-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de45-148">CommonParameters</span></span>
<span data-ttu-id="4de45-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de45-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de45-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4de45-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de45-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4de45-151">INPUTS</span></span>

### <span data-ttu-id="4de45-152">System.String</span><span class="sxs-lookup"><span data-stu-id="4de45-152">System.String</span></span>

## <span data-ttu-id="4de45-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4de45-153">OUTPUTS</span></span>

### <span data-ttu-id="4de45-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="4de45-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="4de45-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="4de45-155">NOTES</span></span>

## <span data-ttu-id="4de45-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4de45-156">RELATED LINKS</span></span>
