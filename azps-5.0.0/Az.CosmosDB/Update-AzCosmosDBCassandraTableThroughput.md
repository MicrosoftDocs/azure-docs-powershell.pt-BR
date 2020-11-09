---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281241"
---
# <span data-ttu-id="23c2b-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="23c2b-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="23c2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="23c2b-103">Atualiza o valor de produtividade de uma tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="23c2b-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="23c2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23c2b-104">SYNTAX</span></span>

### <span data-ttu-id="23c2b-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="23c2b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23c2b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23c2b-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23c2b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23c2b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23c2b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="23c2b-109">Atualiza o valor de produtividade de uma tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="23c2b-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="23c2b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23c2b-110">EXAMPLES</span></span>

### <span data-ttu-id="23c2b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23c2b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="23c2b-112">OS</span><span class="sxs-lookup"><span data-stu-id="23c2b-112">PARAMETERS</span></span>

### <span data-ttu-id="23c2b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23c2b-113">-AccountName</span></span>
<span data-ttu-id="23c2b-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="23c2b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="23c2b-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="23c2b-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="23c2b-116">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="23c2b-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="23c2b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23c2b-117">-Confirm</span></span>
<span data-ttu-id="23c2b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23c2b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23c2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c2b-119">-DefaultProfile</span></span>
<span data-ttu-id="23c2b-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23c2b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23c2b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23c2b-121">-InputObject</span></span>
<span data-ttu-id="23c2b-122">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="23c2b-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="23c2b-123">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="23c2b-123">-KeyspaceName</span></span>
<span data-ttu-id="23c2b-124">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="23c2b-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="23c2b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="23c2b-125">-Name</span></span>
<span data-ttu-id="23c2b-126">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="23c2b-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="23c2b-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="23c2b-127">-ParentObject</span></span>
<span data-ttu-id="23c2b-128">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="23c2b-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="23c2b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c2b-129">-ResourceGroupName</span></span>
<span data-ttu-id="23c2b-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23c2b-130">Name of resource group.</span></span>

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

### <span data-ttu-id="23c2b-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="23c2b-131">-Throughput</span></span>
<span data-ttu-id="23c2b-132">A taxa de transferência do espaço de Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="23c2b-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="23c2b-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="23c2b-133">Default value is 400.</span></span>

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

### <span data-ttu-id="23c2b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23c2b-134">-WhatIf</span></span>
<span data-ttu-id="23c2b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23c2b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23c2b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23c2b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23c2b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c2b-137">CommonParameters</span></span>
<span data-ttu-id="23c2b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23c2b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c2b-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23c2b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c2b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23c2b-140">INPUTS</span></span>

### <span data-ttu-id="23c2b-141">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="23c2b-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="23c2b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23c2b-142">OUTPUTS</span></span>

### <span data-ttu-id="23c2b-143">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="23c2b-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="23c2b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23c2b-144">NOTES</span></span>

## <span data-ttu-id="23c2b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23c2b-145">RELATED LINKS</span></span>
