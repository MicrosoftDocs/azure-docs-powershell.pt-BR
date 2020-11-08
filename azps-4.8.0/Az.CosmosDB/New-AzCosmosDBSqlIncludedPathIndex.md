---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: f6bd378ac39c0e00975616b08d3bb9c14358d5d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114625"
---
# <span data-ttu-id="a411e-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="a411e-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="a411e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a411e-102">SYNOPSIS</span></span>
<span data-ttu-id="a411e-103">Cria um novo objeto do tipo PSIndexes.</span><span class="sxs-lookup"><span data-stu-id="a411e-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="a411e-104">Ele pode ser passado como um valor de parâmetro para Set-AzCosmosDBSqlIncludedPath.</span><span class="sxs-lookup"><span data-stu-id="a411e-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="a411e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a411e-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a411e-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a411e-106">DESCRIPTION</span></span>
<span data-ttu-id="a411e-107">Objeto correspondente aos índices do IncludedPath's da API SQL.</span><span class="sxs-lookup"><span data-stu-id="a411e-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="a411e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a411e-108">EXAMPLES</span></span>

### <span data-ttu-id="a411e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a411e-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="a411e-110">OS</span><span class="sxs-lookup"><span data-stu-id="a411e-110">PARAMETERS</span></span>

### <span data-ttu-id="a411e-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="a411e-111">-DataType</span></span>
<span data-ttu-id="a411e-112">Tipo de dados ao qual o comportamento de indexação é aplicado.</span><span class="sxs-lookup"><span data-stu-id="a411e-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="a411e-113">Os valores possíveis incluem: ' String ', ' Number ', ' Point ', ' Polygon ', ' LineString ', ' MultiPolygon '</span><span class="sxs-lookup"><span data-stu-id="a411e-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="a411e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a411e-114">-DefaultProfile</span></span>
<span data-ttu-id="a411e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a411e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a411e-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="a411e-116">-Kind</span></span>
<span data-ttu-id="a411e-117">Indica o tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="a411e-117">Indicates the type of index.</span></span>
<span data-ttu-id="a411e-118">Os valores possíveis incluem: ' hash ', ' intervalo ', ' Spatial '</span><span class="sxs-lookup"><span data-stu-id="a411e-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="a411e-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="a411e-119">-Precision</span></span>
<span data-ttu-id="a411e-120">A precisão do índice.</span><span class="sxs-lookup"><span data-stu-id="a411e-120">The precision of the index.</span></span>
<span data-ttu-id="a411e-121">-1 é a precisão máxima.</span><span class="sxs-lookup"><span data-stu-id="a411e-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="a411e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a411e-122">CommonParameters</span></span>
<span data-ttu-id="a411e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a411e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a411e-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a411e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a411e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a411e-125">INPUTS</span></span>

### <span data-ttu-id="a411e-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a411e-126">None</span></span>

## <span data-ttu-id="a411e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a411e-127">OUTPUTS</span></span>

### <span data-ttu-id="a411e-128">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="a411e-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="a411e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a411e-129">NOTES</span></span>

## <span data-ttu-id="a411e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a411e-130">RELATED LINKS</span></span>
