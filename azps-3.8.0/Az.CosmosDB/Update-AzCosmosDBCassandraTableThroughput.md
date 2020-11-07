---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944423"
---
# <span data-ttu-id="40739-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="40739-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="40739-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40739-102">SYNOPSIS</span></span>
<span data-ttu-id="40739-103">Atualiza o valor de produtividade de uma tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="40739-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="40739-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40739-104">SYNTAX</span></span>

### <span data-ttu-id="40739-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="40739-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40739-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40739-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40739-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40739-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40739-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40739-108">EXAMPLES</span></span>

### <span data-ttu-id="40739-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40739-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="40739-110">OS</span><span class="sxs-lookup"><span data-stu-id="40739-110">PARAMETERS</span></span>

### <span data-ttu-id="40739-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40739-111">-AccountName</span></span>
<span data-ttu-id="40739-112">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="40739-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40739-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40739-113">-Confirm</span></span>
<span data-ttu-id="40739-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40739-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40739-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40739-115">-DefaultProfile</span></span>
<span data-ttu-id="40739-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40739-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40739-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40739-117">-InputObject</span></span>
<span data-ttu-id="40739-118">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="40739-118">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40739-119">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="40739-119">-KeyspaceName</span></span>
<span data-ttu-id="40739-120">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="40739-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="40739-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="40739-121">-Name</span></span>
<span data-ttu-id="40739-122">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="40739-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="40739-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="40739-123">-ParentObject</span></span>
<span data-ttu-id="40739-124">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="40739-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="40739-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40739-125">-ResourceGroupName</span></span>
<span data-ttu-id="40739-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40739-126">Name of resource group.</span></span>

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

### <span data-ttu-id="40739-127">-Throughput</span><span class="sxs-lookup"><span data-stu-id="40739-127">-Throughput</span></span>
<span data-ttu-id="40739-128">A taxa de transferência do espaço de Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="40739-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="40739-129">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="40739-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40739-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40739-130">-WhatIf</span></span>
<span data-ttu-id="40739-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40739-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40739-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40739-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40739-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40739-133">CommonParameters</span></span>
<span data-ttu-id="40739-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40739-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40739-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40739-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40739-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40739-136">INPUTS</span></span>

### <span data-ttu-id="40739-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="40739-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="40739-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40739-138">OUTPUTS</span></span>

### <span data-ttu-id="40739-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="40739-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="40739-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40739-140">NOTES</span></span>

## <span data-ttu-id="40739-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40739-141">RELATED LINKS</span></span>
