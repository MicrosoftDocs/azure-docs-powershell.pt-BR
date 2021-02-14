---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116473"
---
# <span data-ttu-id="945c4-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="945c4-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="945c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="945c4-102">SYNOPSIS</span></span>
<span data-ttu-id="945c4-103">Obtém o Graph de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="945c4-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="945c4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="945c4-104">SYNTAX</span></span>

### <span data-ttu-id="945c4-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="945c4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="945c4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="945c4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="945c4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="945c4-107">DESCRIPTION</span></span>
<span data-ttu-id="945c4-108">O cmdlet **Get-AzCosmosDBGremlinGraph** obtém as propriedades do OceanDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="945c4-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="945c4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="945c4-109">EXAMPLES</span></span>

### <span data-ttu-id="945c4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="945c4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="945c4-111">O Objeto de Recurso contém IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="945c4-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="945c4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="945c4-112">PARAMETERS</span></span>

### <span data-ttu-id="945c4-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="945c4-113">-AccountName</span></span>
<span data-ttu-id="945c4-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="945c4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="945c4-115">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="945c4-115">-DatabaseName</span></span>
<span data-ttu-id="945c4-116">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="945c4-116">Database name.</span></span>

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

### <span data-ttu-id="945c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945c4-117">-DefaultProfile</span></span>
<span data-ttu-id="945c4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="945c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="945c4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="945c4-119">-Name</span></span>
<span data-ttu-id="945c4-120">Nome do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="945c4-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="945c4-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="945c4-121">-ParentObject</span></span>
<span data-ttu-id="945c4-122">Objeto de Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="945c4-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="945c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="945c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="945c4-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="945c4-124">Name of resource group.</span></span>

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

### <span data-ttu-id="945c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945c4-125">CommonParameters</span></span>
<span data-ttu-id="945c4-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945c4-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="945c4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945c4-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="945c4-128">INPUTS</span></span>

### <span data-ttu-id="945c4-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="945c4-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="945c4-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="945c4-130">OUTPUTS</span></span>

### <span data-ttu-id="945c4-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="945c4-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="945c4-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="945c4-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="945c4-133">Notas</span><span class="sxs-lookup"><span data-stu-id="945c4-133">NOTES</span></span>

## <span data-ttu-id="945c4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="945c4-134">RELATED LINKS</span></span>
