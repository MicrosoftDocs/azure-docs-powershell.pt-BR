---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 2719f875d4a21f47b05b55b7880e4654237baafd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117872"
---
# <span data-ttu-id="5b10a-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="5b10a-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="5b10a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b10a-102">SYNOPSIS</span></span>
<span data-ttu-id="5b10a-103">Exporte logs que mostram as solicitações de Api feitas por essa assinatura na janela de tempo determinada para mostrar atividades de ônus.</span><span class="sxs-lookup"><span data-stu-id="5b10a-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="5b10a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b10a-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b10a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b10a-105">DESCRIPTION</span></span>
<span data-ttu-id="5b10a-106">Exporta dados estatísticos sobre as chamadas da assinatura para a API Microsoft.Compute por status bem-sucedido, de falha ou de aceleração, em intervalos de tempo predefinidos.</span><span class="sxs-lookup"><span data-stu-id="5b10a-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="5b10a-107">Os logs podem ser ainda mais agrupados por três parâmetros: GroupByOperationName, GroupByThrottlePolicy ou GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="5b10a-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="5b10a-108">Observe que esse cmdlet coleta apenas logs do Provedor de Recursos de Computação; além disso, os dados sobre os tipos de recursos de Disco e Instantâneo ainda não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5b10a-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="5b10a-109">Para ter uma visão geral da throttling da API do Provedor de Recursos de Computação, consulte https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="5b10a-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="5b10a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b10a-110">EXAMPLES</span></span>

### <span data-ttu-id="5b10a-111">Exemplo 1: Exportar registros agregados por nome da operação</span><span class="sxs-lookup"><span data-stu-id="5b10a-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="5b10a-112">Esse comando armazena os números agregados de chamadas da API Microsoft.Compute separadas por Sucesso, Falha ou Ressalto entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI SAS determinado, agregado por nome de operação.</span><span class="sxs-lookup"><span data-stu-id="5b10a-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="5b10a-113">Exemplo 2: Exportar registros agregados por ID do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5b10a-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId
```

<span data-ttu-id="5b10a-114">Esse comando armazena os números agregados de chamadas da API Microsoft.Compute separadas por Sucesso, Falha ou Ressalto entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI do SAS determinado, agregado por ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b10a-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="5b10a-115">Exemplo 3: Exportar registros agregados por agente do usuário</span><span class="sxs-lookup"><span data-stu-id="5b10a-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
```

<span data-ttu-id="5b10a-116">Esse comando armazena os números agregados de chamadas da API Microsoft.Compute separadas por Sucesso, Falha ou Ressalto entre 2018-02-20T17:54:14 e 2018-02-22T17:54:17 no URI do SAS determinado, agregado por agente de usuário.</span><span class="sxs-lookup"><span data-stu-id="5b10a-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="5b10a-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b10a-117">PARAMETERS</span></span>

### <span data-ttu-id="5b10a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b10a-118">-AsJob</span></span>
<span data-ttu-id="5b10a-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5b10a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b10a-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="5b10a-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="5b10a-121">Uri do SAS do contêiner de blob de log para o qual a Api logAnalytics grava logs de saída.</span><span class="sxs-lookup"><span data-stu-id="5b10a-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="5b10a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b10a-122">-DefaultProfile</span></span>
<span data-ttu-id="5b10a-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b10a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b10a-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="5b10a-124">-FromTime</span></span>
<span data-ttu-id="5b10a-125">A partir do momento da consulta</span><span class="sxs-lookup"><span data-stu-id="5b10a-125">From time of the query</span></span>

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

### <span data-ttu-id="5b10a-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="5b10a-126">-GroupByApplicationId</span></span>
<span data-ttu-id="5b10a-127">Resultado da consulta de grupo por ID do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b10a-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="5b10a-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="5b10a-128">-GroupByOperationName</span></span>
<span data-ttu-id="5b10a-129">Resultado da consulta de grupo por Nome da Operação.</span><span class="sxs-lookup"><span data-stu-id="5b10a-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="5b10a-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="5b10a-130">-GroupByResourceName</span></span>
<span data-ttu-id="5b10a-131">Resultado da consulta de grupo por Nome do Recurso.</span><span class="sxs-lookup"><span data-stu-id="5b10a-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="5b10a-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="5b10a-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="5b10a-133">Resultado da consulta de grupo pela Política de Aceleração aplicada.</span><span class="sxs-lookup"><span data-stu-id="5b10a-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="5b10a-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="5b10a-134">-GroupByUserAgent</span></span>
<span data-ttu-id="5b10a-135">Resultado da consulta de grupo pelo UserAgent.</span><span class="sxs-lookup"><span data-stu-id="5b10a-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="5b10a-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="5b10a-136">-IntervalLength</span></span>
<span data-ttu-id="5b10a-137">Valor de intervalo em minutos usados para criar logs de taxas de chamadas do LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="5b10a-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="5b10a-138">-Local</span><span class="sxs-lookup"><span data-stu-id="5b10a-138">-Location</span></span>
<span data-ttu-id="5b10a-139">O local no qual o log é consultado.</span><span class="sxs-lookup"><span data-stu-id="5b10a-139">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="5b10a-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5b10a-140">-NoWait</span></span>
<span data-ttu-id="5b10a-141">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5b10a-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5b10a-142">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="5b10a-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5b10a-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="5b10a-143">-ToTime</span></span>
<span data-ttu-id="5b10a-144">Para o horário da consulta</span><span class="sxs-lookup"><span data-stu-id="5b10a-144">To time of the query</span></span>

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

### <span data-ttu-id="5b10a-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5b10a-145">-Confirm</span></span>
<span data-ttu-id="5b10a-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b10a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b10a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b10a-147">-WhatIf</span></span>
<span data-ttu-id="5b10a-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5b10a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b10a-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b10a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b10a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b10a-150">CommonParameters</span></span>
<span data-ttu-id="5b10a-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b10a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b10a-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b10a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b10a-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="5b10a-153">INPUTS</span></span>

### <span data-ttu-id="5b10a-154">System.String</span><span class="sxs-lookup"><span data-stu-id="5b10a-154">System.String</span></span>

## <span data-ttu-id="5b10a-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="5b10a-155">OUTPUTS</span></span>

### <span data-ttu-id="5b10a-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="5b10a-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="5b10a-157">Notas</span><span class="sxs-lookup"><span data-stu-id="5b10a-157">NOTES</span></span>

## <span data-ttu-id="5b10a-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b10a-158">RELATED LINKS</span></span>
