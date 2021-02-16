---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 97f921fab8e258d5fbde44a6c148f61da2730999
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117871"
---
# <span data-ttu-id="bf654-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="bf654-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="bf654-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf654-102">SYNOPSIS</span></span>
<span data-ttu-id="bf654-103">Exporte logs que mostram o total de solicitações de Api aceleradas para esta assinatura na janela de tempo determinada.</span><span class="sxs-lookup"><span data-stu-id="bf654-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="bf654-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf654-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf654-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf654-105">DESCRIPTION</span></span>
<span data-ttu-id="bf654-106">Isso exporta o número total de chamadas de API de Computação da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bf654-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="bf654-107">Os logs podem ser agregados ainda mais por três opções: GroupByOperationName, GroupByThrottlePolicy ou GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="bf654-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="bf654-108">Observe que esse cmdlet coleta apenas logs CRP.</span><span class="sxs-lookup"><span data-stu-id="bf654-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="bf654-109">Para ter uma visão geral da throttling da API do Provedor de Recursos de Computação, consulte https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="bf654-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="bf654-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bf654-110">EXAMPLES</span></span>

### <span data-ttu-id="bf654-111">Exemplo 1: Exportar registros agregados por nome da operação</span><span class="sxs-lookup"><span data-stu-id="bf654-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="bf654-112">Esse comando armazena o total de chamadas de API de Computação da Microsoft entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado por nome de operação.</span><span class="sxs-lookup"><span data-stu-id="bf654-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="bf654-113">Exemplo 2: Exportar registros agregados por ID do aplicativo</span><span class="sxs-lookup"><span data-stu-id="bf654-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="bf654-114">Esse comando armazena o total de chamadas de API de Computação da Microsoft entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado por ID de appliction.</span><span class="sxs-lookup"><span data-stu-id="bf654-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="bf654-115">Exemplo 3: Exportar registros agregados por agente do usuário</span><span class="sxs-lookup"><span data-stu-id="bf654-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="bf654-116">Esse comando armazena o total de chamadas de API de Computação da Microsoft entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado por agente de usuário.</span><span class="sxs-lookup"><span data-stu-id="bf654-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="bf654-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf654-117">PARAMETERS</span></span>

### <span data-ttu-id="bf654-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf654-118">-AsJob</span></span>
<span data-ttu-id="bf654-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bf654-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf654-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="bf654-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="bf654-121">Uri do SAS do contêiner de blob de log para o qual a Api logAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="bf654-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="bf654-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf654-122">-DefaultProfile</span></span>
<span data-ttu-id="bf654-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf654-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf654-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="bf654-124">-FromTime</span></span>
<span data-ttu-id="bf654-125">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="bf654-125">From time of the query</span></span>

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

### <span data-ttu-id="bf654-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="bf654-126">-GroupByApplicationId</span></span>
<span data-ttu-id="bf654-127">Resultado da consulta de grupo por ID do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bf654-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="bf654-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="bf654-128">-GroupByOperationName</span></span>
<span data-ttu-id="bf654-129">Resultado da consulta de grupo por Nome da Operação.</span><span class="sxs-lookup"><span data-stu-id="bf654-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="bf654-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="bf654-130">-GroupByResourceName</span></span>
<span data-ttu-id="bf654-131">Resultado da consulta de grupo por Nome do Recurso.</span><span class="sxs-lookup"><span data-stu-id="bf654-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="bf654-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="bf654-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="bf654-133">Resultado da consulta de grupo pela Política de Aceleração aplicada.</span><span class="sxs-lookup"><span data-stu-id="bf654-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="bf654-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="bf654-134">-GroupByUserAgent</span></span>
<span data-ttu-id="bf654-135">Resultado da consulta de grupo pelo UserAgent.</span><span class="sxs-lookup"><span data-stu-id="bf654-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="bf654-136">-Local</span><span class="sxs-lookup"><span data-stu-id="bf654-136">-Location</span></span>
<span data-ttu-id="bf654-137">O local no qual o log é consultado.</span><span class="sxs-lookup"><span data-stu-id="bf654-137">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="bf654-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bf654-138">-NoWait</span></span>
<span data-ttu-id="bf654-139">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="bf654-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bf654-140">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="bf654-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bf654-141">-ToTime</span><span class="sxs-lookup"><span data-stu-id="bf654-141">-ToTime</span></span>
<span data-ttu-id="bf654-142">Para o horário da consulta</span><span class="sxs-lookup"><span data-stu-id="bf654-142">To time of the query</span></span>

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

### <span data-ttu-id="bf654-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bf654-143">-Confirm</span></span>
<span data-ttu-id="bf654-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf654-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf654-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf654-145">-WhatIf</span></span>
<span data-ttu-id="bf654-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bf654-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf654-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf654-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf654-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf654-148">CommonParameters</span></span>
<span data-ttu-id="bf654-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf654-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf654-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf654-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf654-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="bf654-151">INPUTS</span></span>

### <span data-ttu-id="bf654-152">System.String</span><span class="sxs-lookup"><span data-stu-id="bf654-152">System.String</span></span>

## <span data-ttu-id="bf654-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="bf654-153">OUTPUTS</span></span>

### <span data-ttu-id="bf654-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="bf654-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="bf654-155">Notas</span><span class="sxs-lookup"><span data-stu-id="bf654-155">NOTES</span></span>

## <span data-ttu-id="bf654-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf654-156">RELATED LINKS</span></span>
