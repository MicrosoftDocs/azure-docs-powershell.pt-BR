---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434050"
---
# <span data-ttu-id="9c7f8-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9c7f8-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="9c7f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7f8-103">Cria um novo objeto do tipo PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="9c7f8-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="9c7f8-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="9c7f8-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="9c7f8-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c7f8-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c7f8-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c7f8-106">DESCRIPTION</span></span>
<span data-ttu-id="9c7f8-107">Cria um objeto correspondente ao SpatialSpec da API SQL.</span><span class="sxs-lookup"><span data-stu-id="9c7f8-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="9c7f8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c7f8-108">EXAMPLES</span></span>

### <span data-ttu-id="9c7f8-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c7f8-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="9c7f8-110">OS</span><span class="sxs-lookup"><span data-stu-id="9c7f8-110">PARAMETERS</span></span>

### <span data-ttu-id="9c7f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c7f8-111">-DefaultProfile</span></span>
<span data-ttu-id="9c7f8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c7f8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c7f8-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9c7f8-113">-Path</span></span>
<span data-ttu-id="9c7f8-114">Caminho no documento JSON para indexação.</span><span class="sxs-lookup"><span data-stu-id="9c7f8-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="9c7f8-115">-Digite</span><span class="sxs-lookup"><span data-stu-id="9c7f8-115">-Type</span></span>
<span data-ttu-id="9c7f8-116">Matriz de cadeias de caracteres com valores aceitáveis: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="9c7f8-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="9c7f8-117">Representar o tipo de caminho espacial.</span><span class="sxs-lookup"><span data-stu-id="9c7f8-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="9c7f8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7f8-118">CommonParameters</span></span>
<span data-ttu-id="9c7f8-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c7f8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7f8-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c7f8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7f8-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c7f8-121">INPUTS</span></span>

### <span data-ttu-id="9c7f8-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9c7f8-122">None</span></span>

## <span data-ttu-id="9c7f8-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c7f8-123">OUTPUTS</span></span>

### <span data-ttu-id="9c7f8-124">Microsoft. Azure. Commands. CosmosDB. Models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9c7f8-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="9c7f8-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c7f8-125">NOTES</span></span>

## <span data-ttu-id="9c7f8-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c7f8-126">RELATED LINKS</span></span>
