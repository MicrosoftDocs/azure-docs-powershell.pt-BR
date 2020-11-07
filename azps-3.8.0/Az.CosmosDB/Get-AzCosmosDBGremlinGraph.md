---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944122"
---
# <span data-ttu-id="8eed7-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="8eed7-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="8eed7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eed7-102">SYNOPSIS</span></span>
<span data-ttu-id="8eed7-103">Obtém o gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8eed7-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="8eed7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8eed7-104">SYNTAX</span></span>

### <span data-ttu-id="8eed7-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8eed7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="8eed7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8eed7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eed7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8eed7-107">DESCRIPTION</span></span>
<span data-ttu-id="8eed7-108">O cmdlet **Get-AzCosmosDBGremlinGraph** Obtém as propriedades do gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8eed7-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="8eed7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8eed7-109">EXAMPLES</span></span>

### <span data-ttu-id="8eed7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8eed7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="8eed7-111">Objeto de recurso contém IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="8eed7-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="8eed7-112">OS</span><span class="sxs-lookup"><span data-stu-id="8eed7-112">PARAMETERS</span></span>

### <span data-ttu-id="8eed7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8eed7-113">-AccountName</span></span>
<span data-ttu-id="8eed7-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="8eed7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8eed7-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8eed7-115">-DatabaseName</span></span>
<span data-ttu-id="8eed7-116">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8eed7-116">Database name.</span></span>

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

### <span data-ttu-id="8eed7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eed7-117">-DefaultProfile</span></span>
<span data-ttu-id="8eed7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8eed7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eed7-119">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="8eed7-119">-Detailed</span></span>
<span data-ttu-id="8eed7-120">Se fornecido, o cmdlet retornará o gráfico Gremlin com o valor de produtividade correspondente.</span><span class="sxs-lookup"><span data-stu-id="8eed7-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eed7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eed7-121">-InputObject</span></span>
<span data-ttu-id="8eed7-122">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8eed7-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="8eed7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8eed7-123">-Name</span></span>
<span data-ttu-id="8eed7-124">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="8eed7-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="8eed7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eed7-125">-ResourceGroupName</span></span>
<span data-ttu-id="8eed7-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8eed7-126">Name of resource group.</span></span>

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

### <span data-ttu-id="8eed7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eed7-127">CommonParameters</span></span>
<span data-ttu-id="8eed7-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eed7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eed7-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8eed7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eed7-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8eed7-130">INPUTS</span></span>

### <span data-ttu-id="8eed7-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8eed7-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="8eed7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8eed7-132">OUTPUTS</span></span>

### <span data-ttu-id="8eed7-133">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="8eed7-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="8eed7-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8eed7-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8eed7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8eed7-135">NOTES</span></span>

## <span data-ttu-id="8eed7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eed7-136">RELATED LINKS</span></span>
