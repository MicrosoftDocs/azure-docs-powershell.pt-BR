---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260029"
---
# <span data-ttu-id="58a63-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="58a63-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="58a63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58a63-102">SYNOPSIS</span></span>
<span data-ttu-id="58a63-103">Obtém o gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="58a63-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="58a63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58a63-104">SYNTAX</span></span>

### <span data-ttu-id="58a63-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="58a63-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="58a63-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a63-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58a63-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58a63-107">DESCRIPTION</span></span>
<span data-ttu-id="58a63-108">O cmdlet **Get-AzCosmosDBGremlinGraph** Obtém as propriedades do gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="58a63-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="58a63-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58a63-109">EXAMPLES</span></span>

### <span data-ttu-id="58a63-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58a63-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="58a63-111">Objeto de recurso contém IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="58a63-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="58a63-112">OS</span><span class="sxs-lookup"><span data-stu-id="58a63-112">PARAMETERS</span></span>

### <span data-ttu-id="58a63-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58a63-113">-AccountName</span></span>
<span data-ttu-id="58a63-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="58a63-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58a63-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="58a63-115">-DatabaseName</span></span>
<span data-ttu-id="58a63-116">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="58a63-116">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58a63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a63-117">-DefaultProfile</span></span>
<span data-ttu-id="58a63-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58a63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a63-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="58a63-119">-Name</span></span>
<span data-ttu-id="58a63-120">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="58a63-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="58a63-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="58a63-121">-ParentObject</span></span>
<span data-ttu-id="58a63-122">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="58a63-122">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58a63-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a63-123">-ResourceGroupName</span></span>
<span data-ttu-id="58a63-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58a63-124">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58a63-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a63-125">CommonParameters</span></span>
<span data-ttu-id="58a63-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a63-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a63-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58a63-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a63-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58a63-128">INPUTS</span></span>

### <span data-ttu-id="58a63-129">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="58a63-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="58a63-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58a63-130">OUTPUTS</span></span>

### <span data-ttu-id="58a63-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="58a63-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="58a63-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="58a63-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="58a63-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58a63-133">NOTES</span></span>

## <span data-ttu-id="58a63-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58a63-134">RELATED LINKS</span></span>
