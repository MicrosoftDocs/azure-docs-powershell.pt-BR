---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: feae2282f6b989b8d595b2a51cd147975e689174
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887562"
---
# <span data-ttu-id="51f89-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="51f89-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="51f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51f89-102">SYNOPSIS</span></span>
<span data-ttu-id="51f89-103">Exporte logs que mostram solicitações de Api feitas por essa assinatura na janela de tempo determinada para mostrar atividades de throttling.</span><span class="sxs-lookup"><span data-stu-id="51f89-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="51f89-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="51f89-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f89-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="51f89-105">DESCRIPTION</span></span>
<span data-ttu-id="51f89-106">Exporta dados estatísticos sobre as chamadas da assinatura para a API Microsoft.Compute pelo status Sucesso, Falha ou Aceleração, em intervalos de tempo predefinidos.</span><span class="sxs-lookup"><span data-stu-id="51f89-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="51f89-107">Os logs podem ser agrupados ainda mais por cinco parâmetros: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent ou GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="51f89-107">The logs can be further grouped by five parameters: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="51f89-108">Observe que este cmdlet coleta apenas logs do Provedor de Recursos de Computação; Além disso, os dados sobre os tipos de recursos De disco e instantâneo ainda não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="51f89-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="51f89-109">Para uma visão geral da configuração da API do Provedor de Recursos de Computação, consulte https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="51f89-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="51f89-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51f89-110">EXAMPLES</span></span>

### <span data-ttu-id="51f89-111">Exemplo 1: Exportar registros agregados pelo nome da operação</span><span class="sxs-lookup"><span data-stu-id="51f89-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             operationName   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <operationName> 10            10                 0
2/21/2018  7:30:00 PM <operationName> 8             8                  0
2/21/2018  9:00:00 PM <operationName> 9             9                  0

```

<span data-ttu-id="51f89-112">Este comando armazena os números agregados de chamadas da API Microsoft.Compute separadas por Sucesso, Falha ou Acelerada entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado pelo nome da operação.</span><span class="sxs-lookup"><span data-stu-id="51f89-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="51f89-113">Exemplo 2: Exportar registros agregados por id de aplicativo</span><span class="sxs-lookup"><span data-stu-id="51f89-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId

This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             clientApplicationId   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <clientApplicationId> 10            10                 0
2/21/2018  7:30:00 PM <clientApplicationId> 8             8                  0
2/21/2018  9:00:00 PM <clientApplicationId> 9             9                  0

```

<span data-ttu-id="51f89-114">Este comando armazena os números agregados de chamadas da API Microsoft.Compute separadas por Sucesso, Falha ou Acelerada entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado por id de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51f89-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="51f89-115">Exemplo 3: Exportar registros agregados pelo agente do usuário</span><span class="sxs-lookup"><span data-stu-id="51f89-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             userAgent   TotalRequests SuccessfulRequests ThrottledRequests
---------             ---------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <userAgent> 10            10                 0
2/21/2018  7:30:00 PM <userAgent> 8             8                  0
2/21/2018  9:00:00 PM <userAgent> 9             9                  0

```

<span data-ttu-id="51f89-116">Este comando armazena os números agregados de chamadas da API Microsoft.Compute separadas por Sucesso, Falha ou Acelerada entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado pelo agente de usuário.</span><span class="sxs-lookup"><span data-stu-id="51f89-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="51f89-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="51f89-117">PARAMETERS</span></span>

### <span data-ttu-id="51f89-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51f89-118">-AsJob</span></span>
<span data-ttu-id="51f89-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="51f89-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51f89-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="51f89-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="51f89-121">Uri SAS do contêiner de blob de registro em log para o qual a Api LogAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="51f89-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="51f89-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f89-122">-DefaultProfile</span></span>
<span data-ttu-id="51f89-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51f89-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51f89-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="51f89-124">-FromTime</span></span>
<span data-ttu-id="51f89-125">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="51f89-125">From time of the query</span></span>

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

### <span data-ttu-id="51f89-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="51f89-126">-GroupByApplicationId</span></span>
<span data-ttu-id="51f89-127">Resultado da consulta de grupo por ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51f89-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="51f89-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="51f89-128">-GroupByOperationName</span></span>
<span data-ttu-id="51f89-129">Resultado da consulta de grupo por Nome da Operação.</span><span class="sxs-lookup"><span data-stu-id="51f89-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="51f89-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="51f89-130">-GroupByResourceName</span></span>
<span data-ttu-id="51f89-131">Resultado da consulta de grupo pelo Nome do Recurso.</span><span class="sxs-lookup"><span data-stu-id="51f89-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="51f89-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="51f89-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="51f89-133">Resultado da consulta de grupo pela Política de Aceleração aplicada.</span><span class="sxs-lookup"><span data-stu-id="51f89-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="51f89-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="51f89-134">-GroupByUserAgent</span></span>
<span data-ttu-id="51f89-135">Resultado da consulta de grupo por UserAgent.</span><span class="sxs-lookup"><span data-stu-id="51f89-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="51f89-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="51f89-136">-IntervalLength</span></span>
<span data-ttu-id="51f89-137">Valor de intervalo em minutos usado para criar logs de taxa de chamada logAnalytics.</span><span class="sxs-lookup"><span data-stu-id="51f89-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="51f89-138">-Location</span><span class="sxs-lookup"><span data-stu-id="51f89-138">-Location</span></span>
<span data-ttu-id="51f89-139">O local no qual o log é consultado.</span><span class="sxs-lookup"><span data-stu-id="51f89-139">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="51f89-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="51f89-140">-NoWait</span></span>
<span data-ttu-id="51f89-141">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="51f89-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="51f89-142">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="51f89-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="51f89-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="51f89-143">-ToTime</span></span>
<span data-ttu-id="51f89-144">Até a hora da consulta</span><span class="sxs-lookup"><span data-stu-id="51f89-144">To time of the query</span></span>

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

### <span data-ttu-id="51f89-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51f89-145">-Confirm</span></span>
<span data-ttu-id="51f89-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f89-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51f89-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f89-147">-WhatIf</span></span>
<span data-ttu-id="51f89-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51f89-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51f89-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51f89-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51f89-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f89-150">CommonParameters</span></span>
<span data-ttu-id="51f89-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f89-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f89-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51f89-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f89-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51f89-153">INPUTS</span></span>

### <span data-ttu-id="51f89-154">System.String</span><span class="sxs-lookup"><span data-stu-id="51f89-154">System.String</span></span>

## <span data-ttu-id="51f89-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="51f89-155">OUTPUTS</span></span>

### <span data-ttu-id="51f89-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="51f89-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="51f89-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="51f89-157">NOTES</span></span>

## <span data-ttu-id="51f89-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51f89-158">RELATED LINKS</span></span>
