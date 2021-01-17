---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434098"
---
# <span data-ttu-id="fa2c8-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="fa2c8-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="fa2c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2c8-103">Obtém o gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="fa2c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa2c8-104">SYNTAX</span></span>

### <span data-ttu-id="fa2c8-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa2c8-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="fa2c8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa2c8-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa2c8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa2c8-107">DESCRIPTION</span></span>
<span data-ttu-id="fa2c8-108">O cmdlet **Get-AzCosmosDBGremlinGraph** Obtém as propriedades do gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="fa2c8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa2c8-109">EXAMPLES</span></span>

### <span data-ttu-id="fa2c8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa2c8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="fa2c8-111">Objeto de recurso contém IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="fa2c8-112">OS</span><span class="sxs-lookup"><span data-stu-id="fa2c8-112">PARAMETERS</span></span>

### <span data-ttu-id="fa2c8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fa2c8-113">-AccountName</span></span>
<span data-ttu-id="fa2c8-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fa2c8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fa2c8-115">-DatabaseName</span></span>
<span data-ttu-id="fa2c8-116">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-116">Database name.</span></span>

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

### <span data-ttu-id="fa2c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2c8-117">-DefaultProfile</span></span>
<span data-ttu-id="fa2c8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa2c8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa2c8-119">-Name</span></span>
<span data-ttu-id="fa2c8-120">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="fa2c8-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fa2c8-121">-ParentObject</span></span>
<span data-ttu-id="fa2c8-122">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="fa2c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa2c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa2c8-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-124">Name of resource group.</span></span>

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

### <span data-ttu-id="fa2c8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2c8-125">CommonParameters</span></span>
<span data-ttu-id="fa2c8-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa2c8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2c8-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa2c8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2c8-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa2c8-128">INPUTS</span></span>

### <span data-ttu-id="fa2c8-129">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fa2c8-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="fa2c8-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa2c8-130">OUTPUTS</span></span>

### <span data-ttu-id="fa2c8-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="fa2c8-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="fa2c8-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fa2c8-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fa2c8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa2c8-133">NOTES</span></span>

## <span data-ttu-id="fa2c8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa2c8-134">RELATED LINKS</span></span>
