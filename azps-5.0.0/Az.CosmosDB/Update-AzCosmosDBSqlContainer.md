---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281220"
---
# <span data-ttu-id="cfbff-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="cfbff-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="cfbff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfbff-102">SYNOPSIS</span></span>
<span data-ttu-id="cfbff-103">Atualiza o contêiner SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="cfbff-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="cfbff-104">Executa uma operação de patch do lado do cliente lendo o contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="cfbff-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="cfbff-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfbff-105">SYNTAX</span></span>

### <span data-ttu-id="cfbff-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cfbff-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfbff-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfbff-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfbff-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfbff-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfbff-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfbff-109">DESCRIPTION</span></span>
<span data-ttu-id="cfbff-110">Atualiza o contêiner SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="cfbff-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="cfbff-111">Executa uma operação de patch do lado do cliente lendo o contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="cfbff-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="cfbff-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfbff-112">EXAMPLES</span></span>

### <span data-ttu-id="cfbff-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cfbff-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="cfbff-114">OS</span><span class="sxs-lookup"><span data-stu-id="cfbff-114">PARAMETERS</span></span>

### <span data-ttu-id="cfbff-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cfbff-115">-AccountName</span></span>
<span data-ttu-id="cfbff-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="cfbff-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cfbff-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="cfbff-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="cfbff-118">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="cfbff-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="cfbff-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cfbff-119">-Confirm</span></span>
<span data-ttu-id="cfbff-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfbff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfbff-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="cfbff-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="cfbff-122">ConflictResolutionPolicy objeto do tipo PSSqlConflictResolutionPolicy, quando fornecido, é definido como o ConflictResolutionPolicy do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfbff-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="cfbff-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="cfbff-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="cfbff-124">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="cfbff-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="cfbff-125">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="cfbff-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="cfbff-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="cfbff-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="cfbff-127">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="cfbff-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="cfbff-128">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="cfbff-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="cfbff-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="cfbff-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="cfbff-130">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="cfbff-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="cfbff-131">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="cfbff-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="cfbff-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cfbff-132">-DatabaseName</span></span>
<span data-ttu-id="cfbff-133">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cfbff-133">Database name.</span></span>

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

### <span data-ttu-id="cfbff-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbff-134">-DefaultProfile</span></span>
<span data-ttu-id="cfbff-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfbff-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfbff-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="cfbff-136">-IndexingPolicy</span></span>
<span data-ttu-id="cfbff-137">Objeto de política de indexação do tipo Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfbff-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="cfbff-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfbff-138">-InputObject</span></span>
<span data-ttu-id="cfbff-139">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="cfbff-139">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfbff-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfbff-140">-Name</span></span>
<span data-ttu-id="cfbff-141">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfbff-141">Container name.</span></span>

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

### <span data-ttu-id="cfbff-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cfbff-142">-ParentObject</span></span>
<span data-ttu-id="cfbff-143">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="cfbff-143">Sql Database object.</span></span>

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

### <span data-ttu-id="cfbff-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="cfbff-144">-PartitionKeyKind</span></span>
<span data-ttu-id="cfbff-145">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="cfbff-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="cfbff-146">Os valores possíveis incluem: ' hash ', ' intervalo '</span><span class="sxs-lookup"><span data-stu-id="cfbff-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="cfbff-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="cfbff-147">-PartitionKeyPath</span></span>
<span data-ttu-id="cfbff-148">Caminho da chave da partição, por exemplo, '/address/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="cfbff-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbff-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="cfbff-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="cfbff-150">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="cfbff-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="cfbff-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfbff-151">-ResourceGroupName</span></span>
<span data-ttu-id="cfbff-152">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cfbff-152">Name of resource group.</span></span>

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

### <span data-ttu-id="cfbff-153">-Throughput</span><span class="sxs-lookup"><span data-stu-id="cfbff-153">-Throughput</span></span>
<span data-ttu-id="cfbff-154">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="cfbff-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="cfbff-155">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="cfbff-155">Default value is 400.</span></span>

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

### <span data-ttu-id="cfbff-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="cfbff-156">-TtlInSeconds</span></span>
<span data-ttu-id="cfbff-157">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="cfbff-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="cfbff-158">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="cfbff-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="cfbff-159">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="cfbff-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="cfbff-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="cfbff-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="cfbff-161">UniqueKeyPolicy objeto do tipo Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfbff-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="cfbff-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfbff-162">-WhatIf</span></span>
<span data-ttu-id="cfbff-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cfbff-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfbff-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cfbff-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfbff-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbff-165">CommonParameters</span></span>
<span data-ttu-id="cfbff-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfbff-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbff-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfbff-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbff-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfbff-168">INPUTS</span></span>

### <span data-ttu-id="cfbff-169">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="cfbff-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="cfbff-170">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="cfbff-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="cfbff-171">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="cfbff-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="cfbff-172">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="cfbff-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="cfbff-173">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="cfbff-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="cfbff-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfbff-174">OUTPUTS</span></span>

### <span data-ttu-id="cfbff-175">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="cfbff-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="cfbff-176">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="cfbff-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="cfbff-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfbff-177">NOTES</span></span>

## <span data-ttu-id="cfbff-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfbff-178">RELATED LINKS</span></span>
