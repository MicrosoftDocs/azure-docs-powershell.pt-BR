---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112399"
---
# <span data-ttu-id="5ea83-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="5ea83-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="5ea83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ea83-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea83-103">Obtém um espaço de CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5ea83-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5ea83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ea83-104">SYNTAX</span></span>

### <span data-ttu-id="5ea83-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5ea83-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ea83-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ea83-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ea83-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ea83-107">DESCRIPTION</span></span>
<span data-ttu-id="5ea83-108">O cmdlet **Get-AzCosmosDBCassandraKeyspace** cria um novo ou atualiza um espaço keyCosmosDB Cassandra existente.</span><span class="sxs-lookup"><span data-stu-id="5ea83-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5ea83-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ea83-109">EXAMPLES</span></span>

### <span data-ttu-id="5ea83-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ea83-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="5ea83-111">Get-AzCosmosDBCassandraKeyspace Obtém as propriedades de um CassandraKeyspace existente.</span><span class="sxs-lookup"><span data-stu-id="5ea83-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="5ea83-112">Você pode expandir o recurso para obter as propriedades _etag, _ts _rid.</span><span class="sxs-lookup"><span data-stu-id="5ea83-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="5ea83-113">OS</span><span class="sxs-lookup"><span data-stu-id="5ea83-113">PARAMETERS</span></span>

### <span data-ttu-id="5ea83-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5ea83-114">-AccountName</span></span>
<span data-ttu-id="5ea83-115">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="5ea83-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5ea83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea83-116">-DefaultProfile</span></span>
<span data-ttu-id="5ea83-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ea83-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ea83-118">-Name</span></span>
<span data-ttu-id="5ea83-119">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5ea83-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5ea83-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ea83-120">-ParentObject</span></span>
<span data-ttu-id="5ea83-121">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5ea83-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5ea83-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea83-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ea83-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ea83-123">Name of resource group.</span></span>

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

### <span data-ttu-id="5ea83-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea83-124">CommonParameters</span></span>
<span data-ttu-id="5ea83-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea83-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea83-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ea83-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea83-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ea83-127">INPUTS</span></span>

### <span data-ttu-id="5ea83-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5ea83-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5ea83-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ea83-129">OUTPUTS</span></span>

### <span data-ttu-id="5ea83-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5ea83-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="5ea83-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5ea83-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5ea83-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ea83-132">NOTES</span></span>

## <span data-ttu-id="5ea83-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ea83-133">RELATED LINKS</span></span>
