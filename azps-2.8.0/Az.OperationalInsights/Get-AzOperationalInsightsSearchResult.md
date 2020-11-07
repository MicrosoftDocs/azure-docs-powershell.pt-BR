---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
ms.openlocfilehash: 47a8edf304ebc5481073151c180c01a65259149c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772896"
---
# <span data-ttu-id="bb083-101">Get-AzOperationalInsightsSearchResult</span><span class="sxs-lookup"><span data-stu-id="bb083-101">Get-AzOperationalInsightsSearchResult</span></span>

## <span data-ttu-id="bb083-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb083-102">SYNOPSIS</span></span>
<span data-ttu-id="bb083-103">Retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="bb083-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="bb083-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb083-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String> [[-Top] <Int64>]
 [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>] [[-Start] <DateTime>]
 [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb083-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb083-105">DESCRIPTION</span></span>
<span data-ttu-id="bb083-106">O cmdlet **Get-AzOperationalInsightsSearchResult** retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="bb083-106">The **Get-AzOperationalInsightsSearchResult** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="bb083-107">Você pode acessar o status da pesquisa na propriedade Metadata do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="bb083-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="bb083-108">Se o status estiver pendente, a pesquisa não foi concluída e os resultados serão do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="bb083-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="bb083-109">Você pode recuperar os resultados da pesquisa a partir da propriedade Value do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="bb083-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="bb083-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb083-110">EXAMPLES</span></span>

### <span data-ttu-id="bb083-111">Exemplo 1: obter resultados de pesquisa usando uma consulta</span><span class="sxs-lookup"><span data-stu-id="bb083-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="bb083-112">Esse comando obtém todos os resultados da pesquisa usando uma consulta.</span><span class="sxs-lookup"><span data-stu-id="bb083-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="bb083-113">Exemplo 2: obter resultados de pesquisa usando uma ID</span><span class="sxs-lookup"><span data-stu-id="bb083-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="bb083-114">Esse comando obtém os resultados da pesquisa usando uma ID.</span><span class="sxs-lookup"><span data-stu-id="bb083-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="bb083-115">Exemplo 3: Aguarde até a conclusão da pesquisa antes de exibir os resultados</span><span class="sxs-lookup"><span data-stu-id="bb083-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="bb083-116">Esse script inicia uma pesquisa e aguarda até que ela seja concluída antes de exibir os resultados.</span><span class="sxs-lookup"><span data-stu-id="bb083-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="bb083-117">OS</span><span class="sxs-lookup"><span data-stu-id="bb083-117">PARAMETERS</span></span>

### <span data-ttu-id="bb083-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb083-118">-DefaultProfile</span></span>
<span data-ttu-id="bb083-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bb083-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb083-120">-End</span><span class="sxs-lookup"><span data-stu-id="bb083-120">-End</span></span>
<span data-ttu-id="bb083-121">Final do intervalo de tempo consultado.</span><span class="sxs-lookup"><span data-stu-id="bb083-121">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb083-122">-ID</span><span class="sxs-lookup"><span data-stu-id="bb083-122">-Id</span></span>
<span data-ttu-id="bb083-123">Se for fornecida uma ID, os resultados da pesquisa para essa ID serão recuperados usando os parâmetros de consulta originais.</span><span class="sxs-lookup"><span data-stu-id="bb083-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb083-124">-Realce</span><span class="sxs-lookup"><span data-stu-id="bb083-124">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb083-125">-Realce</span><span class="sxs-lookup"><span data-stu-id="bb083-125">-PreHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb083-126">-Consulta</span><span class="sxs-lookup"><span data-stu-id="bb083-126">-Query</span></span>
<span data-ttu-id="bb083-127">A consulta de pesquisa que será executada.</span><span class="sxs-lookup"><span data-stu-id="bb083-127">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb083-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb083-128">-ResourceGroupName</span></span>
<span data-ttu-id="bb083-129">O nome do grupo de recursos que contém o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb083-129">The name of the resource group that contains the workspace.</span></span>

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

### <span data-ttu-id="bb083-130">-Início</span><span class="sxs-lookup"><span data-stu-id="bb083-130">-Start</span></span>
<span data-ttu-id="bb083-131">Início do intervalo de tempo consultado.</span><span class="sxs-lookup"><span data-stu-id="bb083-131">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb083-132">-Início</span><span class="sxs-lookup"><span data-stu-id="bb083-132">-Top</span></span>
<span data-ttu-id="bb083-133">O número máximo de resultados a serem retornados, limitados a 5000.</span><span class="sxs-lookup"><span data-stu-id="bb083-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb083-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bb083-134">-WorkspaceName</span></span>
<span data-ttu-id="bb083-135">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb083-135">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb083-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb083-136">CommonParameters</span></span>
<span data-ttu-id="bb083-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb083-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb083-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb083-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb083-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb083-139">INPUTS</span></span>

### <span data-ttu-id="bb083-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bb083-140">System.String</span></span>

### <span data-ttu-id="bb083-141">System. Int64</span><span class="sxs-lookup"><span data-stu-id="bb083-141">System.Int64</span></span>

### <span data-ttu-id="bb083-142">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb083-142">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bb083-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb083-143">OUTPUTS</span></span>

### <span data-ttu-id="bb083-144">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="bb083-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="bb083-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb083-145">NOTES</span></span>

## <span data-ttu-id="bb083-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb083-146">RELATED LINKS</span></span>

[<span data-ttu-id="bb083-147">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="bb083-147">Get-AzOperationalInsightsSavedSearchResult</span></span>](./Get-AzOperationalInsightsSavedSearchResult.md)


