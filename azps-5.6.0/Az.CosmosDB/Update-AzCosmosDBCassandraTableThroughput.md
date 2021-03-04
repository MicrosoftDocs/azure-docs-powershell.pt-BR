---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 989035c1478228eb8895a2f99779129c605b2f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888563"
---
# <span data-ttu-id="c10ee-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="c10ee-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="c10ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c10ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c10ee-103">Atualiza o valor de produtividade de uma Tabela de Cassandra de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c10ee-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="c10ee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c10ee-104">SYNTAX</span></span>

### <span data-ttu-id="c10ee-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c10ee-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c10ee-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c10ee-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c10ee-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c10ee-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c10ee-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c10ee-108">DESCRIPTION</span></span>
<span data-ttu-id="c10ee-109">Atualiza o valor de produtividade de uma Tabela de Cassandra de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c10ee-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="c10ee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c10ee-110">EXAMPLES</span></span>

### <span data-ttu-id="c10ee-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c10ee-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="c10ee-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c10ee-112">PARAMETERS</span></span>

### <span data-ttu-id="c10ee-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c10ee-113">-AccountName</span></span>
<span data-ttu-id="c10ee-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="c10ee-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c10ee-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c10ee-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c10ee-116">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="c10ee-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c10ee-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c10ee-117">-Confirm</span></span>
<span data-ttu-id="c10ee-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c10ee-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c10ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c10ee-119">-DefaultProfile</span></span>
<span data-ttu-id="c10ee-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c10ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c10ee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c10ee-121">-InputObject</span></span>
<span data-ttu-id="c10ee-122">Objeto Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c10ee-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c10ee-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="c10ee-123">-KeyspaceName</span></span>
<span data-ttu-id="c10ee-124">Nome do Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c10ee-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c10ee-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c10ee-125">-Name</span></span>
<span data-ttu-id="c10ee-126">Nome da tabela de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c10ee-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="c10ee-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c10ee-127">-ParentObject</span></span>
<span data-ttu-id="c10ee-128">Objeto Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c10ee-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c10ee-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c10ee-129">-ResourceGroupName</span></span>
<span data-ttu-id="c10ee-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c10ee-130">Name of resource group.</span></span>

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

### <span data-ttu-id="c10ee-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="c10ee-131">-Throughput</span></span>
<span data-ttu-id="c10ee-132">A produtividade de Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c10ee-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="c10ee-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="c10ee-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c10ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c10ee-134">-WhatIf</span></span>
<span data-ttu-id="c10ee-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c10ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c10ee-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c10ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c10ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c10ee-137">CommonParameters</span></span>
<span data-ttu-id="c10ee-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c10ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c10ee-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c10ee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c10ee-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c10ee-140">INPUTS</span></span>

### <span data-ttu-id="c10ee-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c10ee-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="c10ee-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c10ee-142">OUTPUTS</span></span>

### <span data-ttu-id="c10ee-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c10ee-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c10ee-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="c10ee-144">NOTES</span></span>

## <span data-ttu-id="c10ee-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c10ee-145">RELATED LINKS</span></span>
