---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117791"
---
# <span data-ttu-id="2612f-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2612f-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="2612f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2612f-102">SYNOPSIS</span></span>
<span data-ttu-id="2612f-103">Cria um novo objeto Sql IndexingPolicy do SqlDb.</span><span class="sxs-lookup"><span data-stu-id="2612f-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="2612f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2612f-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2612f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2612f-105">DESCRIPTION</span></span>
<span data-ttu-id="2612f-106">O **cmdlet New-AzCosmosDBSqlIndexingPolicy** cria um novo objeto do tipo PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="2612f-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="2612f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2612f-107">EXAMPLES</span></span>

### <span data-ttu-id="2612f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2612f-108">Example 1</span></span>
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

## <span data-ttu-id="2612f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2612f-109">PARAMETERS</span></span>

### <span data-ttu-id="2612f-110">-Automático</span><span class="sxs-lookup"><span data-stu-id="2612f-110">-Automatic</span></span>
<span data-ttu-id="2612f-111">Bool para indicar se a política de indexação é automática</span><span class="sxs-lookup"><span data-stu-id="2612f-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="2612f-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="2612f-112">-CompositePath</span></span>
<span data-ttu-id="2612f-113">Matriz de matriz de objetos do tipo Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="2612f-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="2612f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2612f-114">-DefaultProfile</span></span>
<span data-ttu-id="2612f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2612f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2612f-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="2612f-116">-ExcludedPath</span></span>
<span data-ttu-id="2612f-117">Matriz de cadeias de caracteres que contêm excludedPath(Especifica um caminho em um documento JSON a ser excluído no serviço Azure Db.)  Elementos.</span><span class="sxs-lookup"><span data-stu-id="2612f-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="2612f-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="2612f-118">-IncludedPath</span></span>
<span data-ttu-id="2612f-119">Matriz de cadeias de caracteres que contêm includedPath (especifica um caminho em um documento JSON a ser incluído nos elementos do serviço Azure Db.)</span><span class="sxs-lookup"><span data-stu-id="2612f-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="2612f-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="2612f-120">-IndexingMode</span></span>
<span data-ttu-id="2612f-121">indica o modo de indexação.</span><span class="sxs-lookup"><span data-stu-id="2612f-121">indicates the indexing mode.</span></span>
<span data-ttu-id="2612f-122">Os valores possíveis incluem: 'Consistente', 'Lento', 'Nenhum'</span><span class="sxs-lookup"><span data-stu-id="2612f-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="2612f-123">-EspécieSpec</span><span class="sxs-lookup"><span data-stu-id="2612f-123">-SpatialSpec</span></span>
<span data-ttu-id="2612f-124">Matriz de objetos do tipo Microsoft.Azure.Commands.CosmosDB.PSSárialSpec</span><span class="sxs-lookup"><span data-stu-id="2612f-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="2612f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2612f-125">CommonParameters</span></span>
<span data-ttu-id="2612f-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2612f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2612f-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2612f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2612f-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="2612f-128">INPUTS</span></span>

### <span data-ttu-id="2612f-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2612f-129">None</span></span>

## <span data-ttu-id="2612f-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="2612f-130">OUTPUTS</span></span>

### <span data-ttu-id="2612f-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2612f-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="2612f-132">Notas</span><span class="sxs-lookup"><span data-stu-id="2612f-132">NOTES</span></span>

## <span data-ttu-id="2612f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2612f-133">RELATED LINKS</span></span>
