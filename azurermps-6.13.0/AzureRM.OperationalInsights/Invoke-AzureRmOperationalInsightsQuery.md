---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: 6672bb6f788b06896fdfe9cde44c68639077e5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429406"
---
# <span data-ttu-id="27c6c-101">Invoke-AzureRmOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="27c6c-101">Invoke-AzureRmOperationalInsightsQuery</span></span>

## <span data-ttu-id="27c6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="27c6c-103">Retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="27c6c-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27c6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27c6c-104">SYNTAX</span></span>

### <span data-ttu-id="27c6c-105">ByWorkspaceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="27c6c-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27c6c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="27c6c-106">ByWorkspaceObject</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27c6c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27c6c-107">DESCRIPTION</span></span>
<span data-ttu-id="27c6c-108">O cmdlet **Invoke-AzureRmOperationalInsightsQuery** retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="27c6c-108">The **Invoke-AzureRmOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="27c6c-109">Você pode acessar o status da pesquisa na propriedade Metadata do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="27c6c-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="27c6c-110">Se o status estiver pendente, a pesquisa não foi concluída e os resultados serão do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="27c6c-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="27c6c-111">Você pode recuperar os resultados da pesquisa a partir da propriedade Value do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="27c6c-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="27c6c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27c6c-112">EXAMPLES</span></span>

### <span data-ttu-id="27c6c-113">Exemplo 1: obter resultados de pesquisa usando uma consulta</span><span class="sxs-lookup"><span data-stu-id="27c6c-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="27c6c-114">Uma vez invocado, $queryResults. resultados conterá todas as linhas resultantes da sua consulta.</span><span class="sxs-lookup"><span data-stu-id="27c6c-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="27c6c-115">Exemplo 2: converter $results. Resultado IEnumberable a uma matriz</span><span class="sxs-lookup"><span data-stu-id="27c6c-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="27c6c-116">Algumas consultas podem resultar em um retorno de conjuntos de dados muito grandes.</span><span class="sxs-lookup"><span data-stu-id="27c6c-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="27c6c-117">Por isso, o comportamento padrão do cmdlet é retornar um IEnumerable para reduzir os custos de memória.</span><span class="sxs-lookup"><span data-stu-id="27c6c-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="27c6c-118">Se preferir ter uma matriz de resultados, você pode usar o método de extensão LINQ Enumerable. ToArray () para converter o IEnumerable em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="27c6c-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="27c6c-119">Exemplo 3: obter resultados de pesquisa usando uma consulta em um período específico</span><span class="sxs-lookup"><span data-stu-id="27c6c-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="27c6c-120">Os resultados dessa consulta serão limitados às últimas 24 horas.</span><span class="sxs-lookup"><span data-stu-id="27c6c-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="27c6c-121">Exemplo 4: incluir estatísticas de renderização & no resultado da consulta</span><span class="sxs-lookup"><span data-stu-id="27c6c-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="27c6c-122">Consulte [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) para obter detalhes sobre as informações de renderização e estatística.</span><span class="sxs-lookup"><span data-stu-id="27c6c-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="27c6c-123">OS</span><span class="sxs-lookup"><span data-stu-id="27c6c-123">PARAMETERS</span></span>

### <span data-ttu-id="27c6c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27c6c-124">-AsJob</span></span>
<span data-ttu-id="27c6c-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="27c6c-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27c6c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c6c-126">-DefaultProfile</span></span>
<span data-ttu-id="27c6c-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27c6c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c6c-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="27c6c-128">-IncludeRender</span></span>
<span data-ttu-id="27c6c-129">Se especificado, as informações de renderização para consultas métricas serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="27c6c-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="27c6c-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="27c6c-130">-IncludeStatistics</span></span>
<span data-ttu-id="27c6c-131">Se especificado, as estatísticas da consulta serão incluídas na resposta.</span><span class="sxs-lookup"><span data-stu-id="27c6c-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="27c6c-132">-Consulta</span><span class="sxs-lookup"><span data-stu-id="27c6c-132">-Query</span></span>
<span data-ttu-id="27c6c-133">A consulta a ser executada.</span><span class="sxs-lookup"><span data-stu-id="27c6c-133">The query to execute.</span></span>

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

### <span data-ttu-id="27c6c-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="27c6c-134">-Timespan</span></span>
<span data-ttu-id="27c6c-135">O TimeSpan ao qual o Query foi associado.</span><span class="sxs-lookup"><span data-stu-id="27c6c-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="27c6c-136">-Wait</span><span class="sxs-lookup"><span data-stu-id="27c6c-136">-Wait</span></span>
<span data-ttu-id="27c6c-137">Coloca um limite superior na quantidade de tempo que o servidor levará processando a consulta.</span><span class="sxs-lookup"><span data-stu-id="27c6c-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="27c6c-138">Vejam https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="27c6c-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="27c6c-139">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="27c6c-139">-Workspace</span></span>
<span data-ttu-id="27c6c-140">O espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="27c6c-140">The workspace</span></span>

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

### <span data-ttu-id="27c6c-141">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="27c6c-141">-WorkspaceId</span></span>
<span data-ttu-id="27c6c-142">A ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="27c6c-142">The workspace ID.</span></span>

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

### <span data-ttu-id="27c6c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c6c-143">CommonParameters</span></span>
<span data-ttu-id="27c6c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c6c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c6c-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27c6c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c6c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27c6c-146">INPUTS</span></span>

### <span data-ttu-id="27c6c-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="27c6c-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="27c6c-148">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="27c6c-148">Parameters: Workspace (ByValue)</span></span>

## <span data-ttu-id="27c6c-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27c6c-149">OUTPUTS</span></span>

### <span data-ttu-id="27c6c-150">Microsoft. Azure. Commands. OperationalInsights. Models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="27c6c-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="27c6c-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27c6c-151">NOTES</span></span>

## <span data-ttu-id="27c6c-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27c6c-152">RELATED LINKS</span></span>
