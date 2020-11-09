---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281404"
---
# <span data-ttu-id="c1f58-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="c1f58-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="c1f58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1f58-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f58-103">Obtém uma tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c1f58-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="c1f58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1f58-104">SYNTAX</span></span>

### <span data-ttu-id="c1f58-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1f58-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1f58-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1f58-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1f58-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1f58-107">DESCRIPTION</span></span>
<span data-ttu-id="c1f58-108">O cmdlet **Get-AzCosmosDBCassandraTable** cria um novo ou atualiza um espaço keyCosmosDB Cassandra existente.</span><span class="sxs-lookup"><span data-stu-id="c1f58-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="c1f58-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1f58-109">EXAMPLES</span></span>

### <span data-ttu-id="c1f58-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1f58-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="c1f58-111">{{Get-AzCosmosDBCassandraTable Obtém as propriedades de um CassandraKeyspace existente.</span><span class="sxs-lookup"><span data-stu-id="c1f58-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="c1f58-112">Você pode expandir o recurso para obter o DefaultTtl, o esquema, _etag, _ts, _rid Properties.}}</span><span class="sxs-lookup"><span data-stu-id="c1f58-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="c1f58-113">OS</span><span class="sxs-lookup"><span data-stu-id="c1f58-113">PARAMETERS</span></span>

### <span data-ttu-id="c1f58-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1f58-114">-AccountName</span></span>
<span data-ttu-id="c1f58-115">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c1f58-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c1f58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f58-116">-DefaultProfile</span></span>
<span data-ttu-id="c1f58-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1f58-118">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="c1f58-118">-KeyspaceName</span></span>
<span data-ttu-id="c1f58-119">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c1f58-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c1f58-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1f58-120">-Name</span></span>
<span data-ttu-id="c1f58-121">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c1f58-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="c1f58-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c1f58-122">-ParentObject</span></span>
<span data-ttu-id="c1f58-123">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c1f58-123">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f58-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f58-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1f58-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c1f58-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c1f58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f58-126">CommonParameters</span></span>
<span data-ttu-id="c1f58-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1f58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f58-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1f58-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f58-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1f58-129">INPUTS</span></span>

### <span data-ttu-id="c1f58-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c1f58-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="c1f58-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1f58-131">OUTPUTS</span></span>

### <span data-ttu-id="c1f58-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="c1f58-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="c1f58-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c1f58-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c1f58-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1f58-134">NOTES</span></span>

## <span data-ttu-id="c1f58-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1f58-135">RELATED LINKS</span></span>
