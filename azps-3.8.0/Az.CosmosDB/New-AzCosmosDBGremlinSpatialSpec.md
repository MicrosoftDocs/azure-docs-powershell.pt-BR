---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943648"
---
# <span data-ttu-id="f29c5-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f29c5-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="f29c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f29c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f29c5-103">Cria um novo objeto do tipo PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="f29c5-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="f29c5-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f29c5-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="f29c5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f29c5-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f29c5-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f29c5-106">DESCRIPTION</span></span>
<span data-ttu-id="f29c5-107">Cria o objeto correspondente ao SpatialSpec da API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f29c5-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="f29c5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f29c5-108">EXAMPLES</span></span>

### <span data-ttu-id="f29c5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f29c5-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="f29c5-110">OS</span><span class="sxs-lookup"><span data-stu-id="f29c5-110">PARAMETERS</span></span>

### <span data-ttu-id="f29c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29c5-111">-DefaultProfile</span></span>
<span data-ttu-id="f29c5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f29c5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f29c5-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f29c5-113">-Path</span></span>
<span data-ttu-id="f29c5-114">Caminho no documento JSON para indexação.</span><span class="sxs-lookup"><span data-stu-id="f29c5-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="f29c5-115">-Digite</span><span class="sxs-lookup"><span data-stu-id="f29c5-115">-Type</span></span>
<span data-ttu-id="f29c5-116">Matriz de cadeias de caracteres com valores aceitáveis: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="f29c5-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="f29c5-117">Representar o tipo de caminho espacial.</span><span class="sxs-lookup"><span data-stu-id="f29c5-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29c5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29c5-118">CommonParameters</span></span>
<span data-ttu-id="f29c5-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29c5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29c5-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f29c5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29c5-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f29c5-121">INPUTS</span></span>

### <span data-ttu-id="f29c5-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f29c5-122">None</span></span>

## <span data-ttu-id="f29c5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f29c5-123">OUTPUTS</span></span>

### <span data-ttu-id="f29c5-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f29c5-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="f29c5-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f29c5-125">NOTES</span></span>

## <span data-ttu-id="f29c5-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f29c5-126">RELATED LINKS</span></span>
