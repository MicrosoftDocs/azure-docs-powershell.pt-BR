---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112564"
---
# <span data-ttu-id="ae68a-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae68a-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="ae68a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae68a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae68a-103">Cria um novo objeto CosmosDB SQL IndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="ae68a-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="ae68a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae68a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae68a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae68a-105">DESCRIPTION</span></span>
<span data-ttu-id="ae68a-106">O cmdlet **New-AzCosmosDBSqlIndexingPolicy** cria um novo objeto do tipo PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="ae68a-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="ae68a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae68a-107">EXAMPLES</span></span>

### <span data-ttu-id="ae68a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae68a-108">Example 1</span></span>
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

## <span data-ttu-id="ae68a-109">OS</span><span class="sxs-lookup"><span data-stu-id="ae68a-109">PARAMETERS</span></span>

### <span data-ttu-id="ae68a-110">-Automática</span><span class="sxs-lookup"><span data-stu-id="ae68a-110">-Automatic</span></span>
<span data-ttu-id="ae68a-111">Bool para indicar se a política de indexação é automática</span><span class="sxs-lookup"><span data-stu-id="ae68a-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="ae68a-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="ae68a-112">-CompositePath</span></span>
<span data-ttu-id="ae68a-113">Matriz da matriz de objetos do tipo Microsoft. Azure. Commands. CosmosDB. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="ae68a-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="ae68a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae68a-114">-DefaultProfile</span></span>
<span data-ttu-id="ae68a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae68a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae68a-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="ae68a-116">-ExcludedPath</span></span>
<span data-ttu-id="ae68a-117">Matriz de cadeias de caracteres que contém excludedPath (especifica um caminho dentro de um documento JSON a ser excluído no serviço do Azure Cosmos DB.)  elementos.</span><span class="sxs-lookup"><span data-stu-id="ae68a-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="ae68a-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="ae68a-118">-IncludedPath</span></span>
<span data-ttu-id="ae68a-119">Matriz de cadeias de caracteres que contém includedPath (um caminho dentro de um documento JSON a ser incluído nos elementos do serviço de BD do cosmos do Azure.).</span><span class="sxs-lookup"><span data-stu-id="ae68a-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="ae68a-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="ae68a-120">-IndexingMode</span></span>
<span data-ttu-id="ae68a-121">indica o modo de indexação.</span><span class="sxs-lookup"><span data-stu-id="ae68a-121">indicates the indexing mode.</span></span>
<span data-ttu-id="ae68a-122">Os valores possíveis incluem: ' consistente ', ' Lazy ', ' nenhum '</span><span class="sxs-lookup"><span data-stu-id="ae68a-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="ae68a-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ae68a-123">-SpatialSpec</span></span>
<span data-ttu-id="ae68a-124">Matriz de objetos do tipo Microsoft. Azure. Commands. CosmosDB. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ae68a-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="ae68a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae68a-125">CommonParameters</span></span>
<span data-ttu-id="ae68a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae68a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae68a-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae68a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae68a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae68a-128">INPUTS</span></span>

### <span data-ttu-id="ae68a-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ae68a-129">None</span></span>

## <span data-ttu-id="ae68a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae68a-130">OUTPUTS</span></span>

### <span data-ttu-id="ae68a-131">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae68a-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="ae68a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae68a-132">NOTES</span></span>

## <span data-ttu-id="ae68a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae68a-133">RELATED LINKS</span></span>
