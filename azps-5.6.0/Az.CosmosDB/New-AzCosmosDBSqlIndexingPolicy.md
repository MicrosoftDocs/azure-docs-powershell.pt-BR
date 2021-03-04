---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: b3d7591bf5dd83967230f6c96c3ca5b02232e316
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888375"
---
# <span data-ttu-id="22f2a-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="22f2a-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="22f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="22f2a-103">Cria um novo objeto Sql IndexingPolicy do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="22f2a-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="22f2a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="22f2a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22f2a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="22f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="22f2a-106">O cmdlet **New-AzCosmosDBSqlIndexingPolicy** cria um novo objeto do tipo PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="22f2a-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="22f2a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="22f2a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22f2a-108">Example 1</span></span>
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

## <span data-ttu-id="22f2a-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="22f2a-109">PARAMETERS</span></span>

### <span data-ttu-id="22f2a-110">-Automatic</span><span class="sxs-lookup"><span data-stu-id="22f2a-110">-Automatic</span></span>
<span data-ttu-id="22f2a-111">Bool para indicar se a política de indexação é automática</span><span class="sxs-lookup"><span data-stu-id="22f2a-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="22f2a-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="22f2a-112">-CompositePath</span></span>
<span data-ttu-id="22f2a-113">Matriz de matriz de objetos do tipo Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="22f2a-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="22f2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f2a-114">-DefaultProfile</span></span>
<span data-ttu-id="22f2a-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22f2a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22f2a-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="22f2a-116">-ExcludedPath</span></span>
<span data-ttu-id="22f2a-117">Matriz de cadeias de caracteres contendo excludedPath(Especifica um caminho dentro de um documento JSON a ser excluído no serviço db do Azure Cosmos.)  elementos.</span><span class="sxs-lookup"><span data-stu-id="22f2a-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="22f2a-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="22f2a-118">-IncludedPath</span></span>
<span data-ttu-id="22f2a-119">Matriz de cadeias de caracteres que contêm includedPath (Especifica um caminho dentro de um documento JSON a ser incluído nos elementos do serviço DB do Azure Cosmos.)</span><span class="sxs-lookup"><span data-stu-id="22f2a-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="22f2a-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="22f2a-120">-IndexingMode</span></span>
<span data-ttu-id="22f2a-121">indica o modo de indexação.</span><span class="sxs-lookup"><span data-stu-id="22f2a-121">indicates the indexing mode.</span></span>
<span data-ttu-id="22f2a-122">Os valores possíveis incluem: 'Consistente', 'Lazy', 'None'</span><span class="sxs-lookup"><span data-stu-id="22f2a-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="22f2a-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="22f2a-123">-SpatialSpec</span></span>
<span data-ttu-id="22f2a-124">Matriz de objetos do tipo Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="22f2a-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="22f2a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f2a-125">CommonParameters</span></span>
<span data-ttu-id="22f2a-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22f2a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f2a-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22f2a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f2a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22f2a-128">INPUTS</span></span>

### <span data-ttu-id="22f2a-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="22f2a-129">None</span></span>

## <span data-ttu-id="22f2a-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="22f2a-130">OUTPUTS</span></span>

### <span data-ttu-id="22f2a-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="22f2a-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="22f2a-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="22f2a-132">NOTES</span></span>

## <span data-ttu-id="22f2a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22f2a-133">RELATED LINKS</span></span>
