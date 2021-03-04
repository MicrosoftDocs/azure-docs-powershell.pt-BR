---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 2d784a82974f47c67bae89d55042b81c9c83e273
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888728"
---
# <span data-ttu-id="4004f-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="4004f-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="4004f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4004f-102">SYNOPSIS</span></span>
<span data-ttu-id="4004f-103">Obtém uma Tabela de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4004f-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="4004f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4004f-104">SYNTAX</span></span>

### <span data-ttu-id="4004f-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4004f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4004f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4004f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4004f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4004f-107">DESCRIPTION</span></span>
<span data-ttu-id="4004f-108">O cmdlet **Get-AzCosmosDBCassandraTable** cria um novo ou atualiza um Espaço-Chave existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4004f-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4004f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4004f-109">EXAMPLES</span></span>

### <span data-ttu-id="4004f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4004f-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="4004f-111">{{ Get-AzCosmosDBCassandraTable obtém as propriedades de uma CassandraKeyspace existente.</span><span class="sxs-lookup"><span data-stu-id="4004f-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="4004f-112">Você pode expandir o Recurso para obter as propriedades DefaultTtl, Schema, _etag, _ts, _rid.}}</span><span class="sxs-lookup"><span data-stu-id="4004f-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="4004f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4004f-113">PARAMETERS</span></span>

### <span data-ttu-id="4004f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4004f-114">-AccountName</span></span>
<span data-ttu-id="4004f-115">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="4004f-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4004f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4004f-116">-DefaultProfile</span></span>
<span data-ttu-id="4004f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4004f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4004f-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="4004f-118">-KeyspaceName</span></span>
<span data-ttu-id="4004f-119">Nome do Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4004f-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4004f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4004f-120">-Name</span></span>
<span data-ttu-id="4004f-121">Nome da tabela de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4004f-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4004f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4004f-122">-ParentObject</span></span>
<span data-ttu-id="4004f-123">Objeto Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4004f-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="4004f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4004f-124">-ResourceGroupName</span></span>
<span data-ttu-id="4004f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4004f-125">Name of resource group.</span></span>

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

### <span data-ttu-id="4004f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4004f-126">CommonParameters</span></span>
<span data-ttu-id="4004f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4004f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4004f-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4004f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4004f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4004f-129">INPUTS</span></span>

### <span data-ttu-id="4004f-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4004f-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="4004f-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4004f-131">OUTPUTS</span></span>

### <span data-ttu-id="4004f-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4004f-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="4004f-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4004f-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4004f-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="4004f-134">NOTES</span></span>

## <span data-ttu-id="4004f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4004f-135">RELATED LINKS</span></span>
