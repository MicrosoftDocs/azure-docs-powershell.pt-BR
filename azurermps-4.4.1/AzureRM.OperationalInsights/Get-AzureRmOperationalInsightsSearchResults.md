---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: 161365ee947a118221fa922ab9e7d05486d3908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609613"
---
# <span data-ttu-id="338ee-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="338ee-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="338ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="338ee-102">SYNOPSIS</span></span>
<span data-ttu-id="338ee-103">Retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="338ee-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="338ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="338ee-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="338ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="338ee-105">DESCRIPTION</span></span>
<span data-ttu-id="338ee-106">O cmdlet **Get-AzureRmOperationalInsightsSearchResults** retorna os resultados da pesquisa com base nos parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="338ee-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="338ee-107">Você pode acessar o status da pesquisa na propriedade Metadata do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="338ee-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="338ee-108">Se o status estiver pendente, a pesquisa não foi concluída e os resultados serão do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="338ee-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="338ee-109">Você pode recuperar os resultados da pesquisa a partir da propriedade Value do objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="338ee-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="338ee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="338ee-110">EXAMPLES</span></span>

### <span data-ttu-id="338ee-111">Exemplo 1: obter resultados de pesquisa usando uma consulta</span><span class="sxs-lookup"><span data-stu-id="338ee-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="338ee-112">Esse comando obtém todos os resultados da pesquisa usando uma consulta.</span><span class="sxs-lookup"><span data-stu-id="338ee-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="338ee-113">Exemplo 2: obter resultados de pesquisa usando uma ID</span><span class="sxs-lookup"><span data-stu-id="338ee-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="338ee-114">Esse comando obtém os resultados da pesquisa usando uma ID.</span><span class="sxs-lookup"><span data-stu-id="338ee-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="338ee-115">Exemplo 3: Aguarde até a conclusão da pesquisa antes de exibir os resultados</span><span class="sxs-lookup"><span data-stu-id="338ee-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="338ee-116">Esse script inicia uma pesquisa e aguarda até que ela seja concluída antes de exibir os resultados.</span><span class="sxs-lookup"><span data-stu-id="338ee-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="338ee-117">OS</span><span class="sxs-lookup"><span data-stu-id="338ee-117">PARAMETERS</span></span>

### <span data-ttu-id="338ee-118">-End</span><span class="sxs-lookup"><span data-stu-id="338ee-118">-End</span></span>
<span data-ttu-id="338ee-119">Final do intervalo de tempo consultado.</span><span class="sxs-lookup"><span data-stu-id="338ee-119">End of the queried time range.</span></span>

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

### <span data-ttu-id="338ee-120">-ID</span><span class="sxs-lookup"><span data-stu-id="338ee-120">-Id</span></span>
<span data-ttu-id="338ee-121">Se for fornecida uma ID, os resultados da pesquisa para essa ID serão recuperados usando os parâmetros de consulta originais.</span><span class="sxs-lookup"><span data-stu-id="338ee-121">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

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

### <span data-ttu-id="338ee-122">-Realce</span><span class="sxs-lookup"><span data-stu-id="338ee-122">-PostHighlight</span></span>
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

### <span data-ttu-id="338ee-123">-Realce</span><span class="sxs-lookup"><span data-stu-id="338ee-123">-PreHighlight</span></span>
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

### <span data-ttu-id="338ee-124">-Consulta</span><span class="sxs-lookup"><span data-stu-id="338ee-124">-Query</span></span>
<span data-ttu-id="338ee-125">A consulta de pesquisa que será executada.</span><span class="sxs-lookup"><span data-stu-id="338ee-125">The search query that will be executed.</span></span>

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

### <span data-ttu-id="338ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="338ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="338ee-127">O nome do grupo de recursos que contém o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="338ee-127">The name of the resource group that contains the workspace.</span></span>

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

### <span data-ttu-id="338ee-128">-Início</span><span class="sxs-lookup"><span data-stu-id="338ee-128">-Start</span></span>
<span data-ttu-id="338ee-129">Início do intervalo de tempo consultado.</span><span class="sxs-lookup"><span data-stu-id="338ee-129">Start of the queried time range.</span></span>

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

### <span data-ttu-id="338ee-130">-Início</span><span class="sxs-lookup"><span data-stu-id="338ee-130">-Top</span></span>
<span data-ttu-id="338ee-131">O número máximo de resultados a serem retornados, limitados a 5000.</span><span class="sxs-lookup"><span data-stu-id="338ee-131">The maximum number of results to be returned, limited to 5000.</span></span>

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

### <span data-ttu-id="338ee-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="338ee-132">-WorkspaceName</span></span>
<span data-ttu-id="338ee-133">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="338ee-133">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="338ee-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338ee-134">-DefaultProfile</span></span>
<span data-ttu-id="338ee-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="338ee-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="338ee-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338ee-136">CommonParameters</span></span>
<span data-ttu-id="338ee-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="338ee-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338ee-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="338ee-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338ee-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="338ee-139">INPUTS</span></span>

## <span data-ttu-id="338ee-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="338ee-140">OUTPUTS</span></span>

### <span data-ttu-id="338ee-141">PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="338ee-141">PSSearchGetSearchResultsResponse</span></span>
<span data-ttu-id="338ee-142">O objeto **PSSearchGetSearchResultsResponse** inclui uma propriedade Value que inclui os registros retornados do formato de pesquisa em JSON e um objeto de metadados que inclui informações sobre os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="338ee-142">The **PSSearchGetSearchResultsResponse** object includes a Value property that includes the records returned from the search in JSON format and a metadata object that includes information about the results of the search.</span></span>

## <span data-ttu-id="338ee-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="338ee-143">NOTES</span></span>

## <span data-ttu-id="338ee-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="338ee-144">RELATED LINKS</span></span>

[<span data-ttu-id="338ee-145">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="338ee-145">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


