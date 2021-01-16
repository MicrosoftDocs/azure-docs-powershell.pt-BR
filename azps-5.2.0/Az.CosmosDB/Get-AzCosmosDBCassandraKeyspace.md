---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259039"
---
# <span data-ttu-id="fdc49-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="fdc49-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="fdc49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdc49-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc49-103">Obtém um espaço de CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="fdc49-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="fdc49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdc49-104">SYNTAX</span></span>

### <span data-ttu-id="fdc49-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fdc49-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdc49-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc49-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdc49-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdc49-107">DESCRIPTION</span></span>
<span data-ttu-id="fdc49-108">O cmdlet **Get-AzCosmosDBCassandraKeyspace** cria um novo ou atualiza um espaço keyCosmosDB Cassandra existente.</span><span class="sxs-lookup"><span data-stu-id="fdc49-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="fdc49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdc49-109">EXAMPLES</span></span>

### <span data-ttu-id="fdc49-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdc49-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="fdc49-111">Get-AzCosmosDBCassandraKeyspace Obtém as propriedades de um CassandraKeyspace existente.</span><span class="sxs-lookup"><span data-stu-id="fdc49-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="fdc49-112">Você pode expandir o recurso para obter as propriedades _etag, _ts _rid.</span><span class="sxs-lookup"><span data-stu-id="fdc49-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="fdc49-113">OS</span><span class="sxs-lookup"><span data-stu-id="fdc49-113">PARAMETERS</span></span>

### <span data-ttu-id="fdc49-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fdc49-114">-AccountName</span></span>
<span data-ttu-id="fdc49-115">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="fdc49-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fdc49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc49-116">-DefaultProfile</span></span>
<span data-ttu-id="fdc49-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdc49-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdc49-118">-Name</span></span>
<span data-ttu-id="fdc49-119">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="fdc49-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="fdc49-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fdc49-120">-ParentObject</span></span>
<span data-ttu-id="fdc49-121">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fdc49-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fdc49-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc49-122">-ResourceGroupName</span></span>
<span data-ttu-id="fdc49-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdc49-123">Name of resource group.</span></span>

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

### <span data-ttu-id="fdc49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc49-124">CommonParameters</span></span>
<span data-ttu-id="fdc49-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc49-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdc49-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc49-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdc49-127">INPUTS</span></span>

### <span data-ttu-id="fdc49-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fdc49-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fdc49-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdc49-129">OUTPUTS</span></span>

### <span data-ttu-id="fdc49-130">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="fdc49-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="fdc49-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fdc49-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fdc49-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdc49-132">NOTES</span></span>

## <span data-ttu-id="fdc49-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdc49-133">RELATED LINKS</span></span>
