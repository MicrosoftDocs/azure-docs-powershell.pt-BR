---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117301"
---
# <span data-ttu-id="058ac-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="058ac-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="058ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="058ac-102">SYNOPSIS</span></span>
<span data-ttu-id="058ac-103">Retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="058ac-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="058ac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="058ac-104">SYNTAX</span></span>

### <span data-ttu-id="058ac-105">ByWorkspaceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="058ac-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="058ac-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="058ac-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="058ac-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="058ac-107">DESCRIPTION</span></span>
<span data-ttu-id="058ac-108">O cmdlet **Invoke-AzOperationalInsightsQuery** retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="058ac-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="058ac-109">Você pode acessar o status da pesquisa na propriedade Metadados do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="058ac-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="058ac-110">Se o status estiver Pendente, a pesquisa não foi concluída e os resultados serão do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="058ac-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="058ac-111">Você pode recuperar os resultados da pesquisa da propriedade Valor do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="058ac-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="058ac-112">Verifique os detalhes dos limites gerais de consulta aqui: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language .</span><span class="sxs-lookup"><span data-stu-id="058ac-112">Please check detail of general query limits here: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="058ac-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="058ac-113">EXAMPLES</span></span>

### <span data-ttu-id="058ac-114">Exemplo 1: Obter resultados de pesquisa usando uma consulta</span><span class="sxs-lookup"><span data-stu-id="058ac-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="058ac-115">Uma vez revogada, $queryResults.Resultados conterão todas as linhas resultantes da sua consulta.</span><span class="sxs-lookup"><span data-stu-id="058ac-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="058ac-116">Exemplo 2: Converter $results. Resultado imensurável para uma matriz</span><span class="sxs-lookup"><span data-stu-id="058ac-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="058ac-117">Algumas consultas podem resultar na volta de conjuntos de dados muito grandes.</span><span class="sxs-lookup"><span data-stu-id="058ac-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="058ac-118">Por isso, o comportamento padrão do cmdlet é retornar um IEnumerável para reduzir os custos de memória.</span><span class="sxs-lookup"><span data-stu-id="058ac-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="058ac-119">Se preferir ter uma matriz de resultados, você pode usar o método de extensão LINQ Enumerable.ToArray() para converter o IEnumerable em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="058ac-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="058ac-120">Exemplo 3: Obter resultados de pesquisa usando uma consulta em um prazo específico</span><span class="sxs-lookup"><span data-stu-id="058ac-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="058ac-121">Os resultados dessa consulta serão limitados às últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="058ac-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="058ac-122">Exemplo 4: incluir estatísticas & renderização no resultado da consulta</span><span class="sxs-lookup"><span data-stu-id="058ac-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="058ac-123">Veja [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) detalhes sobre as informações de renderização e estatísticas.</span><span class="sxs-lookup"><span data-stu-id="058ac-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="058ac-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="058ac-124">PARAMETERS</span></span>

### <span data-ttu-id="058ac-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="058ac-125">-AsJob</span></span>
<span data-ttu-id="058ac-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="058ac-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="058ac-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058ac-127">-DefaultProfile</span></span>
<span data-ttu-id="058ac-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="058ac-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="058ac-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="058ac-129">-IncludeRender</span></span>
<span data-ttu-id="058ac-130">Se especificado, as informações de renderização de consultas métricas serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="058ac-130">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="058ac-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="058ac-131">-IncludeStatistics</span></span>
<span data-ttu-id="058ac-132">Se especificado, as estatísticas de consulta serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="058ac-132">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="058ac-133">-Consulta</span><span class="sxs-lookup"><span data-stu-id="058ac-133">-Query</span></span>
<span data-ttu-id="058ac-134">A consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="058ac-134">The query to execute.</span></span>

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

### <span data-ttu-id="058ac-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="058ac-135">-Timespan</span></span>
<span data-ttu-id="058ac-136">O período de tempo para o limite da consulta.</span><span class="sxs-lookup"><span data-stu-id="058ac-136">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="058ac-137">-Aguarde</span><span class="sxs-lookup"><span data-stu-id="058ac-137">-Wait</span></span>
<span data-ttu-id="058ac-138">Coloca um limite superior na quantidade de tempo que o servidor vai passar processando a consulta.</span><span class="sxs-lookup"><span data-stu-id="058ac-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="058ac-139">Ver: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="058ac-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="058ac-140">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="058ac-140">-Workspace</span></span>
<span data-ttu-id="058ac-141">O espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="058ac-141">The workspace</span></span>

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

### <span data-ttu-id="058ac-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="058ac-142">-WorkspaceId</span></span>
<span data-ttu-id="058ac-143">A ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="058ac-143">The workspace ID.</span></span>

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

### <span data-ttu-id="058ac-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058ac-144">CommonParameters</span></span>
<span data-ttu-id="058ac-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="058ac-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058ac-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="058ac-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058ac-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="058ac-147">INPUTS</span></span>

### <span data-ttu-id="058ac-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="058ac-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="058ac-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="058ac-149">OUTPUTS</span></span>

### <span data-ttu-id="058ac-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="058ac-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="058ac-151">Notas</span><span class="sxs-lookup"><span data-stu-id="058ac-151">NOTES</span></span>

## <span data-ttu-id="058ac-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="058ac-152">RELATED LINKS</span></span>
