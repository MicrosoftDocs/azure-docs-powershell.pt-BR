---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 4fc4bd816511132d5a4fd5d317069e3baf9d9225
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887222"
---
# <span data-ttu-id="e7b49-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e7b49-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e7b49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7b49-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b49-103">Cria um novo Contêiner Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e7b49-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e7b49-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7b49-104">SYNTAX</span></span>

### <span data-ttu-id="e7b49-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e7b49-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7b49-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7b49-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7b49-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7b49-107">DESCRIPTION</span></span>
<span data-ttu-id="e7b49-108">Cria um novo Contêiner Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e7b49-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e7b49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7b49-109">EXAMPLES</span></span>

### <span data-ttu-id="e7b49-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e7b49-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="e7b49-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7b49-111">PARAMETERS</span></span>

### <span data-ttu-id="e7b49-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7b49-112">-AccountName</span></span>
<span data-ttu-id="e7b49-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="e7b49-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e7b49-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="e7b49-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="e7b49-115">TTL para Armazenamento Analítico (em Segundos).</span><span class="sxs-lookup"><span data-stu-id="e7b49-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="e7b49-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e7b49-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e7b49-117">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="e7b49-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e7b49-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7b49-118">-Confirm</span></span>
<span data-ttu-id="e7b49-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7b49-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b49-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e7b49-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="e7b49-121">ConflictResolutionPolicy Objeto do tipo PSSqlConflictResolutionPolicy, quando fornecido, é definido como ConflictResolutionPolicy do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e7b49-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b49-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="e7b49-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="e7b49-123">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="e7b49-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="e7b49-124">Se fornecido junto com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e7b49-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e7b49-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="e7b49-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="e7b49-126">Para ser fornecido quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="e7b49-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="e7b49-127">Se fornecido junto com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e7b49-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e7b49-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="e7b49-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="e7b49-129">Para ser fornecido quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="e7b49-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="e7b49-130">Se fornecido junto com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e7b49-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e7b49-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7b49-131">-DatabaseName</span></span>
<span data-ttu-id="e7b49-132">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e7b49-132">Database name.</span></span>

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

### <span data-ttu-id="e7b49-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b49-133">-DefaultProfile</span></span>
<span data-ttu-id="e7b49-134">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7b49-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7b49-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e7b49-135">-IndexingPolicy</span></span>
<span data-ttu-id="e7b49-136">Objeto de política de indexação do tipo Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="e7b49-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b49-137">-Name</span><span class="sxs-lookup"><span data-stu-id="e7b49-137">-Name</span></span>
<span data-ttu-id="e7b49-138">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e7b49-138">Container name.</span></span>

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

### <span data-ttu-id="e7b49-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e7b49-139">-ParentObject</span></span>
<span data-ttu-id="e7b49-140">Objeto Sql Database.</span><span class="sxs-lookup"><span data-stu-id="e7b49-140">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b49-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="e7b49-141">-PartitionKeyKind</span></span>
<span data-ttu-id="e7b49-142">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="e7b49-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="e7b49-143">Os valores possíveis incluem: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="e7b49-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="e7b49-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="e7b49-144">-PartitionKeyPath</span></span>
<span data-ttu-id="e7b49-145">Caminho da Chave de Partição, por exemplo, '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="e7b49-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b49-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e7b49-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="e7b49-147">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="e7b49-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="e7b49-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b49-148">-ResourceGroupName</span></span>
<span data-ttu-id="e7b49-149">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7b49-149">Name of resource group.</span></span>

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

### <span data-ttu-id="e7b49-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e7b49-150">-Throughput</span></span>
<span data-ttu-id="e7b49-151">A produtividade de SQL contêiner (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e7b49-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="e7b49-152">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="e7b49-152">Default value is 400.</span></span>

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

### <span data-ttu-id="e7b49-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="e7b49-153">-TtlInSeconds</span></span>
<span data-ttu-id="e7b49-154">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="e7b49-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="e7b49-155">Se o valor estiver faltando ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="e7b49-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="e7b49-156">Se o valor for definido como n, os itens expiram n segundos após o último tempo modificado.</span><span class="sxs-lookup"><span data-stu-id="e7b49-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="e7b49-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e7b49-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="e7b49-158">Objeto UniqueKeyPolicy do tipo Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e7b49-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b49-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b49-159">-WhatIf</span></span>
<span data-ttu-id="e7b49-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7b49-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7b49-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7b49-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b49-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b49-162">CommonParameters</span></span>
<span data-ttu-id="e7b49-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7b49-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b49-164">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7b49-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b49-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7b49-165">INPUTS</span></span>

### <span data-ttu-id="e7b49-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e7b49-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="e7b49-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e7b49-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="e7b49-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e7b49-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="e7b49-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e7b49-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="e7b49-170">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7b49-170">OUTPUTS</span></span>

### <span data-ttu-id="e7b49-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e7b49-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e7b49-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="e7b49-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e7b49-173">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7b49-173">NOTES</span></span>

## <span data-ttu-id="e7b49-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7b49-174">RELATED LINKS</span></span>
