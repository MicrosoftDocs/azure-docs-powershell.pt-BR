---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4818f0bb179274181c998c4ad07ca013ade0a2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889339"
---
# <span data-ttu-id="65286-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="65286-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="65286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65286-102">SYNOPSIS</span></span>
<span data-ttu-id="65286-103">Obtém o Gráfico de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="65286-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="65286-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65286-104">SYNTAX</span></span>

### <span data-ttu-id="65286-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65286-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="65286-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65286-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65286-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65286-107">DESCRIPTION</span></span>
<span data-ttu-id="65286-108">O cmdlet **Get-AzCosmosDBGremlinGraph** obtém as propriedades do CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="65286-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="65286-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65286-109">EXAMPLES</span></span>

### <span data-ttu-id="65286-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65286-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="65286-111">Objeto Resource contém IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="65286-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="65286-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65286-112">PARAMETERS</span></span>

### <span data-ttu-id="65286-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65286-113">-AccountName</span></span>
<span data-ttu-id="65286-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="65286-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="65286-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="65286-115">-DatabaseName</span></span>
<span data-ttu-id="65286-116">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="65286-116">Database name.</span></span>

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

### <span data-ttu-id="65286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65286-117">-DefaultProfile</span></span>
<span data-ttu-id="65286-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65286-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65286-119">-Name</span><span class="sxs-lookup"><span data-stu-id="65286-119">-Name</span></span>
<span data-ttu-id="65286-120">Nome do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="65286-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="65286-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="65286-121">-ParentObject</span></span>
<span data-ttu-id="65286-122">Objeto Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="65286-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="65286-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65286-123">-ResourceGroupName</span></span>
<span data-ttu-id="65286-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65286-124">Name of resource group.</span></span>

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

### <span data-ttu-id="65286-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65286-125">CommonParameters</span></span>
<span data-ttu-id="65286-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65286-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65286-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65286-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65286-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65286-128">INPUTS</span></span>

### <span data-ttu-id="65286-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="65286-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="65286-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65286-130">OUTPUTS</span></span>

### <span data-ttu-id="65286-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="65286-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="65286-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="65286-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="65286-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="65286-133">NOTES</span></span>

## <span data-ttu-id="65286-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65286-134">RELATED LINKS</span></span>
