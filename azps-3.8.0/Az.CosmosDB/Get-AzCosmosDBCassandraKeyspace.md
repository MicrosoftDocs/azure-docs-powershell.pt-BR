---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777543"
---
# <span data-ttu-id="9836d-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="9836d-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="9836d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9836d-102">SYNOPSIS</span></span>
<span data-ttu-id="9836d-103">Obtém um espaço de CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9836d-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9836d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9836d-104">SYNTAX</span></span>

### <span data-ttu-id="9836d-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9836d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9836d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9836d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9836d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9836d-107">DESCRIPTION</span></span>
<span data-ttu-id="9836d-108">O cmdlet **Get-AzCosmosDBCassandraKeyspace** cria um novo ou atualiza um espaço keyCosmosDB Cassandra existente.</span><span class="sxs-lookup"><span data-stu-id="9836d-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9836d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9836d-109">EXAMPLES</span></span>

### <span data-ttu-id="9836d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9836d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="9836d-111">Get-AzCosmosDBCassandraKeyspace Obtém as propriedades de um CassandraKeyspace existente.</span><span class="sxs-lookup"><span data-stu-id="9836d-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="9836d-112">Você pode expandir o recurso para obter as propriedades _etag, _ts _rid.</span><span class="sxs-lookup"><span data-stu-id="9836d-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="9836d-113">OS</span><span class="sxs-lookup"><span data-stu-id="9836d-113">PARAMETERS</span></span>

### <span data-ttu-id="9836d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9836d-114">-AccountName</span></span>
<span data-ttu-id="9836d-115">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="9836d-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9836d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9836d-116">-DefaultProfile</span></span>
<span data-ttu-id="9836d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9836d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9836d-118">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="9836d-118">-Detailed</span></span>
<span data-ttu-id="9836d-119">Se fornecido, o cmdlet retornará o espaço de keyspace com o valor de produtividade correspondente.</span><span class="sxs-lookup"><span data-stu-id="9836d-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="9836d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9836d-120">-InputObject</span></span>
<span data-ttu-id="9836d-121">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="9836d-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9836d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9836d-122">-Name</span></span>
<span data-ttu-id="9836d-123">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9836d-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9836d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9836d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9836d-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9836d-125">Name of resource group.</span></span>

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

### <span data-ttu-id="9836d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9836d-126">CommonParameters</span></span>
<span data-ttu-id="9836d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9836d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9836d-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9836d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9836d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9836d-129">INPUTS</span></span>

### <span data-ttu-id="9836d-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9836d-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9836d-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9836d-131">OUTPUTS</span></span>

### <span data-ttu-id="9836d-132">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9836d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="9836d-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9836d-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9836d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9836d-134">NOTES</span></span>

## <span data-ttu-id="9836d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9836d-135">RELATED LINKS</span></span>
