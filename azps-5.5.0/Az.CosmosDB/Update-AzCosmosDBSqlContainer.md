---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 60bbe085aaaa65c65ba33839db5f02ae5198e155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112027"
---
# <span data-ttu-id="0a096-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="0a096-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="0a096-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a096-102">SYNOPSIS</span></span>
<span data-ttu-id="0a096-103">Atualiza o Contêiner Sql do Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="0a096-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="0a096-104">Executa uma operação de patch do lado do cliente lendo o Contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="0a096-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="0a096-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a096-105">SYNTAX</span></span>

### <span data-ttu-id="0a096-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0a096-106">ByNameParameterSet (Default)</span></span>
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

### <span data-ttu-id="0a096-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a096-107">ByParentObjectParameterSet</span></span>
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

### <span data-ttu-id="0a096-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a096-108">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="0a096-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a096-109">DESCRIPTION</span></span>
<span data-ttu-id="0a096-110">Atualiza o Contêiner Sql do Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="0a096-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="0a096-111">Executa uma operação de patch do lado do cliente lendo o Contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="0a096-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="0a096-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a096-112">EXAMPLES</span></span>

### <span data-ttu-id="0a096-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a096-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="0a096-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a096-114">PARAMETERS</span></span>

### <span data-ttu-id="0a096-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="0a096-115">-AccountName</span></span>
<span data-ttu-id="0a096-116">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="0a096-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0a096-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="0a096-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="0a096-118">TTL para Armazenamento Analítico (em Segundos).</span><span class="sxs-lookup"><span data-stu-id="0a096-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="0a096-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0a096-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0a096-120">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="0a096-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0a096-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0a096-121">-Confirm</span></span>
<span data-ttu-id="0a096-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a096-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a096-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a096-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="0a096-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as conflictResolutionPolicy of the container.</span><span class="sxs-lookup"><span data-stu-id="0a096-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="0a096-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="0a096-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="0a096-126">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="0a096-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="0a096-127">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="0a096-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0a096-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="0a096-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="0a096-129">A ser fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="0a096-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="0a096-130">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="0a096-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0a096-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="0a096-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="0a096-132">A ser fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="0a096-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="0a096-133">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="0a096-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0a096-134">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="0a096-134">-DatabaseName</span></span>
<span data-ttu-id="0a096-135">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0a096-135">Database name.</span></span>

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

### <span data-ttu-id="0a096-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a096-136">-DefaultProfile</span></span>
<span data-ttu-id="0a096-137">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a096-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a096-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0a096-138">-IndexingPolicy</span></span>
<span data-ttu-id="0a096-139">Objeto de política de indexação do tipo Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a096-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="0a096-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a096-140">-InputObject</span></span>
<span data-ttu-id="0a096-141">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="0a096-141">Sql Container object.</span></span>

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

### <span data-ttu-id="0a096-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a096-142">-Name</span></span>
<span data-ttu-id="0a096-143">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="0a096-143">Container name.</span></span>

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

### <span data-ttu-id="0a096-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0a096-144">-ParentObject</span></span>
<span data-ttu-id="0a096-145">Objeto banco de dados sql.</span><span class="sxs-lookup"><span data-stu-id="0a096-145">Sql Database object.</span></span>

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

### <span data-ttu-id="0a096-146">-PartitionKeyKeyKey</span><span class="sxs-lookup"><span data-stu-id="0a096-146">-PartitionKeyKind</span></span>
<span data-ttu-id="0a096-147">O tipo de algoritmo usado para particionar.</span><span class="sxs-lookup"><span data-stu-id="0a096-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="0a096-148">Os valores possíveis incluem: 'Hash', 'Intervalo'</span><span class="sxs-lookup"><span data-stu-id="0a096-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="0a096-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="0a096-149">-PartitionKeyPath</span></span>
<span data-ttu-id="0a096-150">Caminho da Chave de Partição, por exemplo, '/endereço/cep'.</span><span class="sxs-lookup"><span data-stu-id="0a096-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="0a096-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="0a096-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="0a096-152">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="0a096-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="0a096-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a096-153">-ResourceGroupName</span></span>
<span data-ttu-id="0a096-154">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a096-154">Name of resource group.</span></span>

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

### <span data-ttu-id="0a096-155">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="0a096-155">-Throughput</span></span>
<span data-ttu-id="0a096-156">A produtividade do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0a096-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="0a096-157">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="0a096-157">Default value is 400.</span></span>

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

### <span data-ttu-id="0a096-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="0a096-158">-TtlInSeconds</span></span>
<span data-ttu-id="0a096-159">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="0a096-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="0a096-160">Se o valor estiver ausente ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="0a096-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="0a096-161">Se o valor estiver definido como n, os itens expiram n segundos após o tempo da última modificação.</span><span class="sxs-lookup"><span data-stu-id="0a096-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="0a096-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0a096-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="0a096-163">Objeto UniqueKeyPolicy do tipo Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="0a096-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="0a096-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a096-164">-WhatIf</span></span>
<span data-ttu-id="0a096-165">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0a096-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a096-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a096-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a096-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a096-167">CommonParameters</span></span>
<span data-ttu-id="0a096-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a096-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a096-169">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a096-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a096-170">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a096-170">INPUTS</span></span>

### <span data-ttu-id="0a096-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0a096-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="0a096-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0a096-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="0a096-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a096-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="0a096-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0a096-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="0a096-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="0a096-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="0a096-176">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a096-176">OUTPUTS</span></span>

### <span data-ttu-id="0a096-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0a096-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="0a096-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="0a096-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="0a096-179">Notas</span><span class="sxs-lookup"><span data-stu-id="0a096-179">NOTES</span></span>

## <span data-ttu-id="0a096-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a096-180">RELATED LINKS</span></span>
