---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281338"
---
# <span data-ttu-id="bf006-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="bf006-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="bf006-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf006-102">SYNOPSIS</span></span>
<span data-ttu-id="bf006-103">Cria uma nova tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bf006-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="bf006-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf006-104">SYNTAX</span></span>

### <span data-ttu-id="bf006-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf006-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf006-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf006-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf006-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf006-107">DESCRIPTION</span></span>
<span data-ttu-id="bf006-108">Cria uma nova tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bf006-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="bf006-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf006-109">EXAMPLES</span></span>

### <span data-ttu-id="bf006-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf006-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="bf006-111">OS</span><span class="sxs-lookup"><span data-stu-id="bf006-111">PARAMETERS</span></span>

### <span data-ttu-id="bf006-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf006-112">-AccountName</span></span>
<span data-ttu-id="bf006-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="bf006-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bf006-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="bf006-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="bf006-115">TTL de armazenamento analítico.</span><span class="sxs-lookup"><span data-stu-id="bf006-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="bf006-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="bf006-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bf006-117">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="bf006-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="bf006-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf006-118">-Confirm</span></span>
<span data-ttu-id="bf006-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf006-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf006-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf006-120">-DefaultProfile</span></span>
<span data-ttu-id="bf006-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf006-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf006-122">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="bf006-122">-KeyspaceName</span></span>
<span data-ttu-id="bf006-123">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bf006-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="bf006-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf006-124">-Name</span></span>
<span data-ttu-id="bf006-125">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bf006-125">Cassandra Table Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf006-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf006-126">-ParentObject</span></span>
<span data-ttu-id="bf006-127">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bf006-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="bf006-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf006-128">-ResourceGroupName</span></span>
<span data-ttu-id="bf006-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf006-129">Name of resource group.</span></span>

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

### <span data-ttu-id="bf006-130">-Esquema</span><span class="sxs-lookup"><span data-stu-id="bf006-130">-Schema</span></span>
<span data-ttu-id="bf006-131">Objeto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="bf006-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="bf006-132">Use New-AzCosmosDBCassandraSchema para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="bf006-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf006-133">-Throughput</span><span class="sxs-lookup"><span data-stu-id="bf006-133">-Throughput</span></span>
<span data-ttu-id="bf006-134">A taxa de transferência do espaço de Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="bf006-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="bf006-135">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="bf006-135">Default value is 400.</span></span>

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

### <span data-ttu-id="bf006-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="bf006-136">-TtlInSeconds</span></span>
<span data-ttu-id="bf006-137">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="bf006-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="bf006-138">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="bf006-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="bf006-139">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="bf006-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="bf006-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf006-140">-WhatIf</span></span>
<span data-ttu-id="bf006-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf006-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf006-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf006-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf006-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf006-143">CommonParameters</span></span>
<span data-ttu-id="bf006-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf006-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf006-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf006-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf006-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf006-146">INPUTS</span></span>

### <span data-ttu-id="bf006-147">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="bf006-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="bf006-148">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="bf006-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="bf006-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf006-149">OUTPUTS</span></span>

### <span data-ttu-id="bf006-150">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="bf006-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="bf006-151">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="bf006-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="bf006-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf006-152">NOTES</span></span>

## <span data-ttu-id="bf006-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf006-153">RELATED LINKS</span></span>
