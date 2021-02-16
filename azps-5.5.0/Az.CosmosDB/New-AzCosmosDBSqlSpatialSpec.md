---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117789"
---
# <span data-ttu-id="f6f97-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="f6f97-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="f6f97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6f97-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f97-103">Cria um novo objeto do tipo PSSpatialSpec.</span><span class="sxs-lookup"><span data-stu-id="f6f97-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="f6f97-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f6f97-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="f6f97-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6f97-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6f97-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6f97-106">DESCRIPTION</span></span>
<span data-ttu-id="f6f97-107">Cria o objeto correspondente ao Sistema Desespécie da API sql.</span><span class="sxs-lookup"><span data-stu-id="f6f97-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="f6f97-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6f97-108">EXAMPLES</span></span>

### <span data-ttu-id="f6f97-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6f97-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="f6f97-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6f97-110">PARAMETERS</span></span>

### <span data-ttu-id="f6f97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f97-111">-DefaultProfile</span></span>
<span data-ttu-id="f6f97-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6f97-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f97-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f6f97-113">-Path</span></span>
<span data-ttu-id="f6f97-114">Caminho no documento JSON para indexar.</span><span class="sxs-lookup"><span data-stu-id="f6f97-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="f6f97-115">-Tipo</span><span class="sxs-lookup"><span data-stu-id="f6f97-115">-Type</span></span>
<span data-ttu-id="f6f97-116">Matriz de cadeias de caracteres com valores aceitáveis: Point, LineString, Polígono, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="f6f97-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="f6f97-117">Represente os caminhos de um tipo de espaço espaço.</span><span class="sxs-lookup"><span data-stu-id="f6f97-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="f6f97-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f97-118">CommonParameters</span></span>
<span data-ttu-id="f6f97-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f97-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f97-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6f97-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f97-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="f6f97-121">INPUTS</span></span>

### <span data-ttu-id="f6f97-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f6f97-122">None</span></span>

## <span data-ttu-id="f6f97-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="f6f97-123">OUTPUTS</span></span>

### <span data-ttu-id="f6f97-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSárialSpec</span><span class="sxs-lookup"><span data-stu-id="f6f97-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="f6f97-125">Notas</span><span class="sxs-lookup"><span data-stu-id="f6f97-125">NOTES</span></span>

## <span data-ttu-id="f6f97-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6f97-126">RELATED LINKS</span></span>
