---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 6c84004ffb267a5bc429bb242d3bc7245775d69b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891497"
---
# <span data-ttu-id="d077a-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="d077a-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="d077a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d077a-102">SYNOPSIS</span></span>
<span data-ttu-id="d077a-103">Cria um novo objeto do tipo PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="d077a-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="d077a-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="d077a-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="d077a-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d077a-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d077a-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d077a-106">DESCRIPTION</span></span>
<span data-ttu-id="d077a-107">Objeto correspondente aos Índices da API de Gremlin IncludedPath.</span><span class="sxs-lookup"><span data-stu-id="d077a-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="d077a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d077a-108">EXAMPLES</span></span>

### <span data-ttu-id="d077a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d077a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="d077a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d077a-110">PARAMETERS</span></span>

### <span data-ttu-id="d077a-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="d077a-111">-DataType</span></span>
<span data-ttu-id="d077a-112">Datatype para o qual o comportamento de indexação é aplicado.</span><span class="sxs-lookup"><span data-stu-id="d077a-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="d077a-113">Os valores possíveis incluem: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span><span class="sxs-lookup"><span data-stu-id="d077a-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="d077a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d077a-114">-DefaultProfile</span></span>
<span data-ttu-id="d077a-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d077a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d077a-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="d077a-116">-Kind</span></span>
<span data-ttu-id="d077a-117">Indica o tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="d077a-117">Indicates the type of index.</span></span>
<span data-ttu-id="d077a-118">Os valores possíveis incluem: 'Hash', 'Range', 'Spatial'</span><span class="sxs-lookup"><span data-stu-id="d077a-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="d077a-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="d077a-119">-Precision</span></span>
<span data-ttu-id="d077a-120">A precisão do índice.</span><span class="sxs-lookup"><span data-stu-id="d077a-120">The precision of the index.</span></span>
<span data-ttu-id="d077a-121">-1 é precisão máxima.</span><span class="sxs-lookup"><span data-stu-id="d077a-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d077a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d077a-122">CommonParameters</span></span>
<span data-ttu-id="d077a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d077a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d077a-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d077a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d077a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d077a-125">INPUTS</span></span>

### <span data-ttu-id="d077a-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d077a-126">None</span></span>

## <span data-ttu-id="d077a-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d077a-127">OUTPUTS</span></span>

### <span data-ttu-id="d077a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="d077a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="d077a-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="d077a-129">NOTES</span></span>

## <span data-ttu-id="d077a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d077a-130">RELATED LINKS</span></span>
