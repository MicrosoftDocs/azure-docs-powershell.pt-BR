---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: bdba6d4da6df49d1975e2cfd1cc6e47f6ce6d776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892938"
---
# <span data-ttu-id="e54c0-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="e54c0-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="e54c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e54c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e54c0-103">Retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="e54c0-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="e54c0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e54c0-104">SYNTAX</span></span>

### <span data-ttu-id="e54c0-105">ByWorkspaceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e54c0-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e54c0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e54c0-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e54c0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e54c0-107">DESCRIPTION</span></span>
<span data-ttu-id="e54c0-108">O cmdlet **Invoke-AzOperationalInsightsQuery** retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="e54c0-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="e54c0-109">Você pode acessar o status da pesquisa na propriedade Metadados do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="e54c0-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="e54c0-110">Se o status estiver Pendente, a pesquisa não foi concluída e os resultados serão do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="e54c0-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="e54c0-111">Você pode recuperar os resultados da pesquisa da propriedade Value do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="e54c0-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="e54c0-112">Verifique os detalhes dos limites gerais de consulta aqui: https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language .</span><span class="sxs-lookup"><span data-stu-id="e54c0-112">Please check detail of general query limits here: https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="e54c0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e54c0-113">EXAMPLES</span></span>

### <span data-ttu-id="e54c0-114">Exemplo 1: Obter resultados de pesquisa usando uma consulta</span><span class="sxs-lookup"><span data-stu-id="e54c0-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="e54c0-115">Uma vez invocada, $queryResults.Results conterá todas as linhas resultantes de sua consulta.</span><span class="sxs-lookup"><span data-stu-id="e54c0-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="e54c0-116">Exemplo 2: Converter $results. Resultado IEnumerable para uma matriz</span><span class="sxs-lookup"><span data-stu-id="e54c0-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="e54c0-117">Algumas consultas podem resultar em conjuntos de dados muito grandes sendo retornados.</span><span class="sxs-lookup"><span data-stu-id="e54c0-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="e54c0-118">Por isso, o comportamento padrão do cmdlet é retornar um IEnumerable para reduzir os custos de memória.</span><span class="sxs-lookup"><span data-stu-id="e54c0-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="e54c0-119">Se preferir ter uma matriz de resultados, use o método de extensão ENUMERABLE.ToArray() LINQ para converter o IEnumerable em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="e54c0-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="e54c0-120">Exemplo 3: Obter resultados de pesquisa usando uma consulta em um período de tempo específico</span><span class="sxs-lookup"><span data-stu-id="e54c0-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="e54c0-121">Os resultados dessa consulta serão limitados às últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="e54c0-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="e54c0-122">Exemplo 4: incluir estatísticas & renderização no resultado da consulta</span><span class="sxs-lookup"><span data-stu-id="e54c0-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="e54c0-123">Confira [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) detalhes sobre as informações de renderização e estatísticas.</span><span class="sxs-lookup"><span data-stu-id="e54c0-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="e54c0-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e54c0-124">PARAMETERS</span></span>

### <span data-ttu-id="e54c0-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e54c0-125">-AsJob</span></span>
<span data-ttu-id="e54c0-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e54c0-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e54c0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54c0-127">-DefaultProfile</span></span>
<span data-ttu-id="e54c0-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e54c0-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e54c0-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="e54c0-129">-IncludeRender</span></span>
<span data-ttu-id="e54c0-130">Se especificado, as informações de renderização para consultas métricas serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="e54c0-130">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="e54c0-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="e54c0-131">-IncludeStatistics</span></span>
<span data-ttu-id="e54c0-132">Se especificado, as estatísticas de consulta serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="e54c0-132">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="e54c0-133">-Query</span><span class="sxs-lookup"><span data-stu-id="e54c0-133">-Query</span></span>
<span data-ttu-id="e54c0-134">A consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="e54c0-134">The query to execute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54c0-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="e54c0-135">-Timespan</span></span>
<span data-ttu-id="e54c0-136">O tempo limite para delimitar a consulta.</span><span class="sxs-lookup"><span data-stu-id="e54c0-136">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54c0-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="e54c0-137">-Wait</span></span>
<span data-ttu-id="e54c0-138">Coloca um limite superior na quantidade de tempo que o servidor gastará processando a consulta.</span><span class="sxs-lookup"><span data-stu-id="e54c0-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="e54c0-139">Consulte: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="e54c0-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54c0-140">-Workspace</span><span class="sxs-lookup"><span data-stu-id="e54c0-140">-Workspace</span></span>
<span data-ttu-id="e54c0-141">O espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e54c0-141">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e54c0-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="e54c0-142">-WorkspaceId</span></span>
<span data-ttu-id="e54c0-143">A ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e54c0-143">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54c0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54c0-144">CommonParameters</span></span>
<span data-ttu-id="e54c0-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e54c0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54c0-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e54c0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54c0-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e54c0-147">INPUTS</span></span>

### <span data-ttu-id="e54c0-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e54c0-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e54c0-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e54c0-149">OUTPUTS</span></span>

### <span data-ttu-id="e54c0-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="e54c0-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="e54c0-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="e54c0-151">NOTES</span></span>

## <span data-ttu-id="e54c0-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e54c0-152">RELATED LINKS</span></span>
