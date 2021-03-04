---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: a36222b3a6cacf567fd0b5e7541c2dc53a44fa22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888544"
---
# <span data-ttu-id="61757-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="61757-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="61757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61757-102">SYNOPSIS</span></span>
<span data-ttu-id="61757-103">Atualiza o Contêiner Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="61757-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="61757-104">Executa uma operação de patch do lado do cliente lendo o Contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="61757-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="61757-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="61757-105">SYNTAX</span></span>

### <span data-ttu-id="61757-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="61757-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61757-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61757-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61757-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61757-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-AnalyticalStorageTtl <Int32>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61757-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="61757-109">DESCRIPTION</span></span>
<span data-ttu-id="61757-110">Atualiza o Contêiner Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="61757-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="61757-111">Executa uma operação de patch do lado do cliente lendo o Contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="61757-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="61757-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61757-112">EXAMPLES</span></span>

### <span data-ttu-id="61757-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61757-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="61757-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="61757-114">PARAMETERS</span></span>

### <span data-ttu-id="61757-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61757-115">-AccountName</span></span>
<span data-ttu-id="61757-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="61757-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="61757-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="61757-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="61757-118">TTL para Armazenamento Analítico (em Segundos).</span><span class="sxs-lookup"><span data-stu-id="61757-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="61757-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="61757-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="61757-120">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="61757-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="61757-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61757-121">-Confirm</span></span>
<span data-ttu-id="61757-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61757-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61757-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="61757-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="61757-124">ConflictResolutionPolicy Objeto do tipo PSSqlConflictResolutionPolicy, quando fornecido, é definido como ConflictResolutionPolicy do contêiner.</span><span class="sxs-lookup"><span data-stu-id="61757-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="61757-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="61757-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="61757-126">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="61757-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="61757-127">Se fornecido junto com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="61757-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="61757-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="61757-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="61757-129">Para ser fornecido quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="61757-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="61757-130">Se fornecido junto com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="61757-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="61757-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="61757-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="61757-132">Para ser fornecido quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="61757-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="61757-133">Se fornecido junto com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="61757-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="61757-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61757-134">-DatabaseName</span></span>
<span data-ttu-id="61757-135">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="61757-135">Database name.</span></span>

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

### <span data-ttu-id="61757-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61757-136">-DefaultProfile</span></span>
<span data-ttu-id="61757-137">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61757-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61757-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="61757-138">-IndexingPolicy</span></span>
<span data-ttu-id="61757-139">Objeto de política de indexação do tipo Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="61757-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="61757-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61757-140">-InputObject</span></span>
<span data-ttu-id="61757-141">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="61757-141">Sql Container object.</span></span>

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

### <span data-ttu-id="61757-142">-Name</span><span class="sxs-lookup"><span data-stu-id="61757-142">-Name</span></span>
<span data-ttu-id="61757-143">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="61757-143">Container name.</span></span>

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

### <span data-ttu-id="61757-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="61757-144">-ParentObject</span></span>
<span data-ttu-id="61757-145">Objeto Sql Database.</span><span class="sxs-lookup"><span data-stu-id="61757-145">Sql Database object.</span></span>

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

### <span data-ttu-id="61757-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="61757-146">-PartitionKeyKind</span></span>
<span data-ttu-id="61757-147">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="61757-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="61757-148">Os valores possíveis incluem: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="61757-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="61757-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="61757-149">-PartitionKeyPath</span></span>
<span data-ttu-id="61757-150">Caminho da Chave de Partição, por exemplo, '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="61757-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="61757-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="61757-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="61757-152">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="61757-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="61757-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61757-153">-ResourceGroupName</span></span>
<span data-ttu-id="61757-154">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61757-154">Name of resource group.</span></span>

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

### <span data-ttu-id="61757-155">-Throughput</span><span class="sxs-lookup"><span data-stu-id="61757-155">-Throughput</span></span>
<span data-ttu-id="61757-156">A produtividade de SQL contêiner (RU/s).</span><span class="sxs-lookup"><span data-stu-id="61757-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="61757-157">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="61757-157">Default value is 400.</span></span>

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

### <span data-ttu-id="61757-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="61757-158">-TtlInSeconds</span></span>
<span data-ttu-id="61757-159">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="61757-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="61757-160">Se o valor estiver faltando ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="61757-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="61757-161">Se o valor for definido como n, os itens expiram n segundos após o último tempo modificado.</span><span class="sxs-lookup"><span data-stu-id="61757-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="61757-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="61757-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="61757-163">Objeto UniqueKeyPolicy do tipo Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="61757-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="61757-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61757-164">-WhatIf</span></span>
<span data-ttu-id="61757-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61757-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61757-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61757-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61757-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61757-167">CommonParameters</span></span>
<span data-ttu-id="61757-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61757-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61757-169">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61757-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61757-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61757-170">INPUTS</span></span>

### <span data-ttu-id="61757-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="61757-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="61757-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="61757-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="61757-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="61757-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="61757-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="61757-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="61757-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="61757-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="61757-176">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="61757-176">OUTPUTS</span></span>

### <span data-ttu-id="61757-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="61757-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="61757-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="61757-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="61757-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="61757-179">NOTES</span></span>

## <span data-ttu-id="61757-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61757-180">RELATED LINKS</span></span>
