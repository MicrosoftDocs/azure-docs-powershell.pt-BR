---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: fb387adafa1a1a71d9a42b09b8c7255955eccd9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888729"
---
# <span data-ttu-id="c75cb-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="c75cb-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="c75cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c75cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c75cb-103">Obtém um Espaço-Chave de Cassandra de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c75cb-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="c75cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c75cb-104">SYNTAX</span></span>

### <span data-ttu-id="c75cb-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c75cb-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c75cb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75cb-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c75cb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c75cb-107">DESCRIPTION</span></span>
<span data-ttu-id="c75cb-108">O cmdlet **Get-AzCosmosDBCassandraKeyspace** cria um novo ou atualiza um Espaço-Chave existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c75cb-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="c75cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c75cb-109">EXAMPLES</span></span>

### <span data-ttu-id="c75cb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c75cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="c75cb-111">Get-AzCosmosDBCassandraKeyspace obtém as propriedades de uma CassandraKeyspace existente.</span><span class="sxs-lookup"><span data-stu-id="c75cb-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="c75cb-112">Você pode expandir o Recurso para obter as _etag, _ts, _rid propriedades.</span><span class="sxs-lookup"><span data-stu-id="c75cb-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="c75cb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c75cb-113">PARAMETERS</span></span>

### <span data-ttu-id="c75cb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c75cb-114">-AccountName</span></span>
<span data-ttu-id="c75cb-115">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="c75cb-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c75cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c75cb-116">-DefaultProfile</span></span>
<span data-ttu-id="c75cb-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c75cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c75cb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c75cb-118">-Name</span></span>
<span data-ttu-id="c75cb-119">Nome do Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c75cb-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c75cb-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c75cb-120">-ParentObject</span></span>
<span data-ttu-id="c75cb-121">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c75cb-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c75cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c75cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="c75cb-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c75cb-123">Name of resource group.</span></span>

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

### <span data-ttu-id="c75cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c75cb-124">CommonParameters</span></span>
<span data-ttu-id="c75cb-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c75cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c75cb-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c75cb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c75cb-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c75cb-127">INPUTS</span></span>

### <span data-ttu-id="c75cb-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c75cb-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c75cb-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c75cb-129">OUTPUTS</span></span>

### <span data-ttu-id="c75cb-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c75cb-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="c75cb-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c75cb-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c75cb-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="c75cb-132">NOTES</span></span>

## <span data-ttu-id="c75cb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c75cb-133">RELATED LINKS</span></span>
