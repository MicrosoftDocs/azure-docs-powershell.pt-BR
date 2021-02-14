---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115918"
---
# <span data-ttu-id="f9b4f-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f9b4f-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="f9b4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b4f-103">Cria um novo objeto IndexingPolicy do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f9b4f-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="f9b4f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9b4f-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9b4f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b4f-106">O **cmdlet New-AzCosmosDBGremlinIndexingPolicy** cria um novo objeto do tipo PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f9b4f-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="f9b4f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9b4f-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b4f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9b4f-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="f9b4f-109">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="f9b4f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f9b4f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9b4f-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b4f-111">-Automático</span><span class="sxs-lookup"><span data-stu-id="f9b4f-111">-Automatic</span></span>
<span data-ttu-id="f9b4f-112">Bool para indicar se a política de indexação é automática</span><span class="sxs-lookup"><span data-stu-id="f9b4f-112">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="f9b4f-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="f9b4f-113">-CompositePath</span></span>
<span data-ttu-id="f9b4f-114">Matriz de matriz de objetos do tipo Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="f9b4f-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="f9b4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b4f-115">-DefaultProfile</span></span>
<span data-ttu-id="f9b4f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b4f-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="f9b4f-117">-ExcludedPath</span></span>
<span data-ttu-id="f9b4f-118">Matriz de cadeias de caracteres que contêm excludedPath(Especifica um caminho em um documento JSON a ser excluído no serviço Azure Db.)  Elementos.</span><span class="sxs-lookup"><span data-stu-id="f9b4f-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="f9b4f-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="f9b4f-119">-IncludedPath</span></span>
<span data-ttu-id="f9b4f-120">Matriz de cadeias de caracteres que contêm includedPath (especifica um caminho em um documento JSON a ser incluído nos elementos do serviço Azure Db.)</span><span class="sxs-lookup"><span data-stu-id="f9b4f-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="f9b4f-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="f9b4f-121">-IndexingMode</span></span>
<span data-ttu-id="f9b4f-122">Indica o modo de indexação.</span><span class="sxs-lookup"><span data-stu-id="f9b4f-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="f9b4f-123">Os valores possíveis incluem: 'Consistente', 'Lento', 'Nenhum'</span><span class="sxs-lookup"><span data-stu-id="f9b4f-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="f9b4f-124">-EspécieSpec</span><span class="sxs-lookup"><span data-stu-id="f9b4f-124">-SpatialSpec</span></span>
<span data-ttu-id="f9b4f-125">Matriz de objetos do tipo Microsoft.Azure.Commands.CosmosDB.PSSárialSpec</span><span class="sxs-lookup"><span data-stu-id="f9b4f-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="f9b4f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b4f-126">CommonParameters</span></span>
<span data-ttu-id="f9b4f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b4f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b4f-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9b4f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b4f-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9b4f-129">INPUTS</span></span>

### <span data-ttu-id="f9b4f-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f9b4f-130">None</span></span>

## <span data-ttu-id="f9b4f-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9b4f-131">OUTPUTS</span></span>

### <span data-ttu-id="f9b4f-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f9b4f-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="f9b4f-133">Notas</span><span class="sxs-lookup"><span data-stu-id="f9b4f-133">NOTES</span></span>

## <span data-ttu-id="f9b4f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9b4f-134">RELATED LINKS</span></span>
