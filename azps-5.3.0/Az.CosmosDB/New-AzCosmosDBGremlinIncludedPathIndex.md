---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434067"
---
# <span data-ttu-id="9be46-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="9be46-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="9be46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9be46-102">SYNOPSIS</span></span>
<span data-ttu-id="9be46-103">Cria um novo objeto do tipo PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="9be46-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="9be46-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBGremlinIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="9be46-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="9be46-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9be46-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9be46-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9be46-106">DESCRIPTION</span></span>
<span data-ttu-id="9be46-107">Objeto correspondente aos índices IncludedPath's da API Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9be46-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="9be46-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9be46-108">EXAMPLES</span></span>

### <span data-ttu-id="9be46-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9be46-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="9be46-110">OS</span><span class="sxs-lookup"><span data-stu-id="9be46-110">PARAMETERS</span></span>

### <span data-ttu-id="9be46-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="9be46-111">-DataType</span></span>
<span data-ttu-id="9be46-112">Tipo de dados ao qual o comportamento de indexação é aplicado.</span><span class="sxs-lookup"><span data-stu-id="9be46-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="9be46-113">Os valores possíveis incluem: ' String ', ' Number ', ' Point ', ' Polygon ', ' LineString ', ' MultiPolygon '</span><span class="sxs-lookup"><span data-stu-id="9be46-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="9be46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be46-114">-DefaultProfile</span></span>
<span data-ttu-id="9be46-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9be46-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9be46-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="9be46-116">-Kind</span></span>
<span data-ttu-id="9be46-117">Indica o tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="9be46-117">Indicates the type of index.</span></span>
<span data-ttu-id="9be46-118">Os valores possíveis incluem: ' hash ', ' intervalo ', ' Spatial '</span><span class="sxs-lookup"><span data-stu-id="9be46-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="9be46-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="9be46-119">-Precision</span></span>
<span data-ttu-id="9be46-120">A precisão do índice.</span><span class="sxs-lookup"><span data-stu-id="9be46-120">The precision of the index.</span></span>
<span data-ttu-id="9be46-121">-1 é a precisão máxima.</span><span class="sxs-lookup"><span data-stu-id="9be46-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="9be46-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be46-122">CommonParameters</span></span>
<span data-ttu-id="9be46-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be46-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be46-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9be46-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be46-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9be46-125">INPUTS</span></span>

### <span data-ttu-id="9be46-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9be46-126">None</span></span>

## <span data-ttu-id="9be46-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9be46-127">OUTPUTS</span></span>

### <span data-ttu-id="9be46-128">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="9be46-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="9be46-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9be46-129">NOTES</span></span>

## <span data-ttu-id="9be46-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9be46-130">RELATED LINKS</span></span>
