---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 64a7835f1401e8b256e6f549203baaf8e8191606
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599856"
---
# <span data-ttu-id="39d64-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="39d64-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="39d64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39d64-102">SYNOPSIS</span></span>
<span data-ttu-id="39d64-103">Retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="39d64-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="39d64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39d64-104">SYNTAX</span></span>

### <span data-ttu-id="39d64-105">ByWorkspaceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="39d64-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d64-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="39d64-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39d64-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39d64-107">DESCRIPTION</span></span>
<span data-ttu-id="39d64-108">O cmdlet **Invoke-AzOperationalInsightsQuery** retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="39d64-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="39d64-109">Você pode acessar o status da pesquisa na propriedade Metadata do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="39d64-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="39d64-110">Se o status estiver pendente, a pesquisa não foi concluída e os resultados serão do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="39d64-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="39d64-111">Você pode recuperar os resultados da pesquisa a partir da propriedade Value do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="39d64-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="39d64-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39d64-112">EXAMPLES</span></span>

### <span data-ttu-id="39d64-113">Exemplo 1: obter resultados de pesquisa usando uma consulta</span><span class="sxs-lookup"><span data-stu-id="39d64-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="39d64-114">Uma vez invocado, $queryResults. resultados conterá todas as linhas resultantes da sua consulta.</span><span class="sxs-lookup"><span data-stu-id="39d64-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="39d64-115">Exemplo 2: converter $results. Resultado IEnumberable a uma matriz</span><span class="sxs-lookup"><span data-stu-id="39d64-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="39d64-116">Algumas consultas podem resultar em um retorno de conjuntos de dados muito grandes.</span><span class="sxs-lookup"><span data-stu-id="39d64-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="39d64-117">Por isso, o comportamento padrão do cmdlet é retornar um IEnumerable para reduzir os custos de memória.</span><span class="sxs-lookup"><span data-stu-id="39d64-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="39d64-118">Se preferir ter uma matriz de resultados, você pode usar o método de extensão LINQ Enumerable. ToArray () para converter o IEnumerable em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="39d64-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="39d64-119">Exemplo 3: obter resultados de pesquisa usando uma consulta em um período específico</span><span class="sxs-lookup"><span data-stu-id="39d64-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="39d64-120">Os resultados dessa consulta serão limitados às últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="39d64-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="39d64-121">Exemplo 4: incluir estatísticas de renderização & no resultado da consulta</span><span class="sxs-lookup"><span data-stu-id="39d64-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="39d64-122">Consulte [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) para obter detalhes sobre as informações de renderização e estatística.</span><span class="sxs-lookup"><span data-stu-id="39d64-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="39d64-123">OS</span><span class="sxs-lookup"><span data-stu-id="39d64-123">PARAMETERS</span></span>

### <span data-ttu-id="39d64-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39d64-124">-AsJob</span></span>
<span data-ttu-id="39d64-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="39d64-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39d64-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d64-126">-DefaultProfile</span></span>
<span data-ttu-id="39d64-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39d64-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39d64-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="39d64-128">-IncludeRender</span></span>
<span data-ttu-id="39d64-129">Se especificado, as informações de renderização para consultas métricas serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="39d64-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="39d64-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="39d64-130">-IncludeStatistics</span></span>
<span data-ttu-id="39d64-131">Se especificado, as estatísticas da consulta serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="39d64-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="39d64-132">-Consulta</span><span class="sxs-lookup"><span data-stu-id="39d64-132">-Query</span></span>
<span data-ttu-id="39d64-133">A consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="39d64-133">The query to execute.</span></span>

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

### <span data-ttu-id="39d64-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="39d64-134">-Timespan</span></span>
<span data-ttu-id="39d64-135">O TimeSpan ao qual o Query foi associado.</span><span class="sxs-lookup"><span data-stu-id="39d64-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="39d64-136">-Wait</span><span class="sxs-lookup"><span data-stu-id="39d64-136">-Wait</span></span>
<span data-ttu-id="39d64-137">Coloca um limite superior na quantidade de tempo que o servidor levará processando a consulta.</span><span class="sxs-lookup"><span data-stu-id="39d64-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="39d64-138">Vejam https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="39d64-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="39d64-139">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="39d64-139">-Workspace</span></span>
<span data-ttu-id="39d64-140">O espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="39d64-140">The workspace</span></span>

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

### <span data-ttu-id="39d64-141">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="39d64-141">-WorkspaceId</span></span>
<span data-ttu-id="39d64-142">A ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="39d64-142">The workspace ID.</span></span>

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

### <span data-ttu-id="39d64-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d64-143">CommonParameters</span></span>
<span data-ttu-id="39d64-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d64-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d64-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d64-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d64-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39d64-146">INPUTS</span></span>

### <span data-ttu-id="39d64-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="39d64-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="39d64-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39d64-148">OUTPUTS</span></span>

### <span data-ttu-id="39d64-149">Microsoft. Azure. Commands. OperationalInsights. Models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="39d64-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="39d64-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39d64-150">NOTES</span></span>

## <span data-ttu-id="39d64-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39d64-151">RELATED LINKS</span></span>
