---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: e3bfdd771413f17d4dd560a350d45fdb3f47c5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428139"
---
# <span data-ttu-id="d7470-101">Invoke-AzureRmOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="d7470-101">Invoke-AzureRmOperationalInsightsQuery</span></span>

## <span data-ttu-id="d7470-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7470-102">SYNOPSIS</span></span>
<span data-ttu-id="d7470-103">Retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="d7470-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7470-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7470-104">SYNTAX</span></span>

### <span data-ttu-id="d7470-105">ByWorkspaceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="d7470-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7470-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d7470-106">ByWorkspaceObject</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7470-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7470-107">DESCRIPTION</span></span>
<span data-ttu-id="d7470-108">O cmdlet **Invoke-AzureRmOperationalInsightsQuery** retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="d7470-108">The **Invoke-AzureRmOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="d7470-109">Você pode acessar o status da pesquisa na propriedade Metadata do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="d7470-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="d7470-110">Se o status estiver pendente, a pesquisa não foi concluída e os resultados serão do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="d7470-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="d7470-111">Você pode recuperar os resultados da pesquisa a partir da propriedade Value do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="d7470-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="d7470-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7470-112">EXAMPLES</span></span>

### <span data-ttu-id="d7470-113">Exemplo 1: obter resultados de pesquisa usando uma consulta</span><span class="sxs-lookup"><span data-stu-id="d7470-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="d7470-114">Uma vez invocado, $queryResults. resultados conterá todas as linhas resultantes da sua consulta.</span><span class="sxs-lookup"><span data-stu-id="d7470-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="d7470-115">Exemplo 2: converter $results. Resultado IEnumberable a uma matriz</span><span class="sxs-lookup"><span data-stu-id="d7470-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="d7470-116">Algumas consultas podem resultar em um retorno de conjuntos de dados muito grandes.</span><span class="sxs-lookup"><span data-stu-id="d7470-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="d7470-117">Por isso, o comportamento padrão do cmdlet é retornar um IEnumerable para reduzir os custos de memória.</span><span class="sxs-lookup"><span data-stu-id="d7470-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="d7470-118">Se preferir ter uma matriz de resultados, você pode usar o método de extensão LINQ Enumerable. ToArray () para converter o IEnumerable em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="d7470-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="d7470-119">Exemplo 3: obter resultados de pesquisa usando uma consulta em um período específico</span><span class="sxs-lookup"><span data-stu-id="d7470-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="d7470-120">Os resultados dessa consulta serão limitados às últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="d7470-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="d7470-121">Exemplo 4: incluir estatísticas de renderização & no resultado da consulta</span><span class="sxs-lookup"><span data-stu-id="d7470-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="d7470-122">Consulte [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) para obter detalhes sobre as informações de renderização e estatística.</span><span class="sxs-lookup"><span data-stu-id="d7470-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="d7470-123">OS</span><span class="sxs-lookup"><span data-stu-id="d7470-123">PARAMETERS</span></span>

### <span data-ttu-id="d7470-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7470-124">-AsJob</span></span>
<span data-ttu-id="d7470-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7470-125">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="d7470-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7470-126">-DefaultProfile</span></span>
<span data-ttu-id="d7470-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7470-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7470-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="d7470-128">-IncludeRender</span></span>
<span data-ttu-id="d7470-129">Se especificado, as informações de renderização para consultas métricas serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="d7470-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="d7470-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="d7470-130">-IncludeStatistics</span></span>
<span data-ttu-id="d7470-131">Se especificado, as estatísticas da consulta serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="d7470-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="d7470-132">-Consulta</span><span class="sxs-lookup"><span data-stu-id="d7470-132">-Query</span></span>
<span data-ttu-id="d7470-133">A consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="d7470-133">The query to execute.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7470-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="d7470-134">-Timespan</span></span>
<span data-ttu-id="d7470-135">O TimeSpan ao qual o Query foi associado.</span><span class="sxs-lookup"><span data-stu-id="d7470-135">The timespan to bound the query by.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7470-136">-Wait</span><span class="sxs-lookup"><span data-stu-id="d7470-136">-Wait</span></span>
<span data-ttu-id="d7470-137">Coloca um limite superior na quantidade de tempo que o servidor levará processando a consulta.</span><span class="sxs-lookup"><span data-stu-id="d7470-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="d7470-138">Vejam https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="d7470-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7470-139">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d7470-139">-Workspace</span></span>
<span data-ttu-id="d7470-140">O espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d7470-140">The workspace</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7470-141">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="d7470-141">-WorkspaceId</span></span>
<span data-ttu-id="d7470-142">A ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d7470-142">The workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7470-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7470-143">CommonParameters</span></span>
<span data-ttu-id="d7470-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7470-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7470-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7470-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7470-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7470-146">INPUTS</span></span>

### <span data-ttu-id="d7470-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d7470-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="d7470-148">Se canalizado, a ID do espaço de trabalho será extraída da PSWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d7470-148">If piped in, the workspace ID will be extracted from the PSWorkspace.</span></span> <span data-ttu-id="d7470-149">Caso contrário, você pode usar o parâmetro workspaceid para especificar manualmente a ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d7470-149">Otherwise you can use the workspaceId parameter to specify the workspace ID manually.</span></span>

## <span data-ttu-id="d7470-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7470-150">OUTPUTS</span></span>

### <span data-ttu-id="d7470-151">Microsoft. Azure. Commands. OperationalInsights. Models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="d7470-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>
<span data-ttu-id="d7470-152">O ***PSQueryResponse*** contém os resultados, renderizar as estatísticas & da consulta.</span><span class="sxs-lookup"><span data-stu-id="d7470-152">The ***PSQueryResponse*** contains the Results, Render & Statistics of the query.</span></span>

## <span data-ttu-id="d7470-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7470-153">NOTES</span></span>

## <span data-ttu-id="d7470-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7470-154">RELATED LINKS</span></span>

