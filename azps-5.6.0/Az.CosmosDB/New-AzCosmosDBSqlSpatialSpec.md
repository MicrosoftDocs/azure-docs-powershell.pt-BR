---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: e22c8931cf70fba970e71b7a2d099cda725287d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892192"
---
# <span data-ttu-id="a2822-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="a2822-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="a2822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2822-102">SYNOPSIS</span></span>
<span data-ttu-id="a2822-103">Cria um novo objeto do tipo PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="a2822-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="a2822-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="a2822-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="a2822-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a2822-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2822-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a2822-106">DESCRIPTION</span></span>
<span data-ttu-id="a2822-107">Cria Objeto correspondente ao SpatialSpec da API sql.</span><span class="sxs-lookup"><span data-stu-id="a2822-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="a2822-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2822-108">EXAMPLES</span></span>

### <span data-ttu-id="a2822-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2822-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="a2822-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a2822-110">PARAMETERS</span></span>

### <span data-ttu-id="a2822-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2822-111">-DefaultProfile</span></span>
<span data-ttu-id="a2822-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2822-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2822-113">-Path</span><span class="sxs-lookup"><span data-stu-id="a2822-113">-Path</span></span>
<span data-ttu-id="a2822-114">Caminho no documento JSON para indexar.</span><span class="sxs-lookup"><span data-stu-id="a2822-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="a2822-115">-Type</span><span class="sxs-lookup"><span data-stu-id="a2822-115">-Type</span></span>
<span data-ttu-id="a2822-116">Matriz de cadeias de caracteres com valores aceitáveis: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="a2822-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="a2822-117">Tipo espacial de caminhos de representação.</span><span class="sxs-lookup"><span data-stu-id="a2822-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="a2822-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2822-118">CommonParameters</span></span>
<span data-ttu-id="a2822-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2822-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2822-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2822-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2822-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2822-121">INPUTS</span></span>

### <span data-ttu-id="a2822-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a2822-122">None</span></span>

## <span data-ttu-id="a2822-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a2822-123">OUTPUTS</span></span>

### <span data-ttu-id="a2822-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="a2822-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="a2822-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="a2822-125">NOTES</span></span>

## <span data-ttu-id="a2822-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2822-126">RELATED LINKS</span></span>
