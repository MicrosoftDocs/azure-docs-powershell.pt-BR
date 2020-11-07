---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943630"
---
# <span data-ttu-id="1ea02-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="1ea02-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="1ea02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ea02-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea02-103">Cria um novo objeto CosmosDB SQL IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="1ea02-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="1ea02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ea02-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ea02-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ea02-105">DESCRIPTION</span></span>
<span data-ttu-id="1ea02-106">O cmdlet **New-AzCosmosDBSqlIndexingPolicy** cria um novo objeto do tipo PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="1ea02-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="1ea02-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ea02-107">EXAMPLES</span></span>

### <span data-ttu-id="1ea02-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ea02-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="1ea02-109">OS</span><span class="sxs-lookup"><span data-stu-id="1ea02-109">PARAMETERS</span></span>

### <span data-ttu-id="1ea02-110">-Automática</span><span class="sxs-lookup"><span data-stu-id="1ea02-110">-Automatic</span></span>
<span data-ttu-id="1ea02-111">Bool para indicar se a política de indexação é automática</span><span class="sxs-lookup"><span data-stu-id="1ea02-111">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea02-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="1ea02-112">-CompositePath</span></span>
<span data-ttu-id="1ea02-113">Matriz da matriz de objetos do tipo Microsoft. Azure. Commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="1ea02-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea02-114">-DefaultProfile</span></span>
<span data-ttu-id="1ea02-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea02-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea02-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="1ea02-116">-ExcludedPath</span></span>
<span data-ttu-id="1ea02-117">Matriz de cadeias de caracteres que contém excludedPath (especifica um caminho dentro de um documento JSON a ser excluído no serviço do Azure Cosmos DB.)  elementos.</span><span class="sxs-lookup"><span data-stu-id="1ea02-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea02-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="1ea02-118">-IncludedPath</span></span>
<span data-ttu-id="1ea02-119">Matriz de cadeias de caracteres que contém includedPath (um caminho dentro de um documento JSON a ser incluído nos elementos do serviço de BD do cosmos do Azure.).</span><span class="sxs-lookup"><span data-stu-id="1ea02-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea02-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="1ea02-120">-IndexingMode</span></span>
<span data-ttu-id="1ea02-121">indica o modo de indexação.</span><span class="sxs-lookup"><span data-stu-id="1ea02-121">indicates the indexing mode.</span></span>
<span data-ttu-id="1ea02-122">Os valores possíveis incluem: ' consistente ', ' Lazy ', ' nenhum '</span><span class="sxs-lookup"><span data-stu-id="1ea02-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea02-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="1ea02-123">-SpatialSpec</span></span>
<span data-ttu-id="1ea02-124">Matriz de objetos do tipo Microsoft. Azure. Commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="1ea02-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea02-125">CommonParameters</span></span>
<span data-ttu-id="1ea02-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ea02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea02-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ea02-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea02-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ea02-128">INPUTS</span></span>

### <span data-ttu-id="1ea02-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1ea02-129">None</span></span>

## <span data-ttu-id="1ea02-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ea02-130">OUTPUTS</span></span>

### <span data-ttu-id="1ea02-131">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="1ea02-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="1ea02-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ea02-132">NOTES</span></span>

## <span data-ttu-id="1ea02-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ea02-133">RELATED LINKS</span></span>
