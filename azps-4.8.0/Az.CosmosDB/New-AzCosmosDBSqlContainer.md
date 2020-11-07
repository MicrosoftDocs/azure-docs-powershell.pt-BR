---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948373"
---
# <span data-ttu-id="c2b16-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="c2b16-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="c2b16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2b16-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b16-103">Cria um novo contêiner SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c2b16-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c2b16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2b16-104">SYNTAX</span></span>

### <span data-ttu-id="c2b16-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2b16-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2b16-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2b16-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2b16-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2b16-107">DESCRIPTION</span></span>
<span data-ttu-id="c2b16-108">Cria um novo contêiner SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c2b16-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c2b16-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2b16-109">EXAMPLES</span></span>

### <span data-ttu-id="c2b16-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2b16-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="c2b16-111">OS</span><span class="sxs-lookup"><span data-stu-id="c2b16-111">PARAMETERS</span></span>

### <span data-ttu-id="c2b16-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2b16-112">-AccountName</span></span>
<span data-ttu-id="c2b16-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c2b16-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2b16-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c2b16-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c2b16-115">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="c2b16-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c2b16-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2b16-116">-Confirm</span></span>
<span data-ttu-id="c2b16-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2b16-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b16-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b16-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="c2b16-119">ConflictResolutionPolicy objeto do tipo PSSqlConflictResolutionPolicy, quando fornecido, é definido como o ConflictResolutionPolicy do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c2b16-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="c2b16-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="c2b16-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="c2b16-121">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="c2b16-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="c2b16-122">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="c2b16-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2b16-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="c2b16-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="c2b16-124">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="c2b16-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="c2b16-125">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="c2b16-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2b16-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="c2b16-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="c2b16-127">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="c2b16-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="c2b16-128">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="c2b16-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="c2b16-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2b16-129">-DatabaseName</span></span>
<span data-ttu-id="c2b16-130">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c2b16-130">Database name.</span></span>

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

### <span data-ttu-id="c2b16-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b16-131">-DefaultProfile</span></span>
<span data-ttu-id="c2b16-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b16-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b16-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b16-133">-IndexingPolicy</span></span>
<span data-ttu-id="c2b16-134">Objeto de política de indexação do tipo Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="c2b16-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="c2b16-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2b16-135">-Name</span></span>
<span data-ttu-id="c2b16-136">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c2b16-136">Container name.</span></span>

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

### <span data-ttu-id="c2b16-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2b16-137">-ParentObject</span></span>
<span data-ttu-id="c2b16-138">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="c2b16-138">Sql Database object.</span></span>

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

### <span data-ttu-id="c2b16-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="c2b16-139">-PartitionKeyKind</span></span>
<span data-ttu-id="c2b16-140">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="c2b16-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="c2b16-141">Os valores possíveis incluem: ' hash ', ' intervalo '</span><span class="sxs-lookup"><span data-stu-id="c2b16-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="c2b16-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="c2b16-142">-PartitionKeyPath</span></span>
<span data-ttu-id="c2b16-143">Caminho da chave da partição, por exemplo, '/address/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="c2b16-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="c2b16-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c2b16-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="c2b16-145">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="c2b16-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="c2b16-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b16-146">-ResourceGroupName</span></span>
<span data-ttu-id="c2b16-147">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2b16-147">Name of resource group.</span></span>

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

### <span data-ttu-id="c2b16-148">-Throughput</span><span class="sxs-lookup"><span data-stu-id="c2b16-148">-Throughput</span></span>
<span data-ttu-id="c2b16-149">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c2b16-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="c2b16-150">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="c2b16-150">Default value is 400.</span></span>

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

### <span data-ttu-id="c2b16-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c2b16-151">-TtlInSeconds</span></span>
<span data-ttu-id="c2b16-152">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="c2b16-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="c2b16-153">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="c2b16-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="c2b16-154">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="c2b16-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="c2b16-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b16-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="c2b16-156">UniqueKeyPolicy objeto do tipo Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c2b16-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="c2b16-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b16-157">-WhatIf</span></span>
<span data-ttu-id="c2b16-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2b16-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b16-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2b16-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b16-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b16-160">CommonParameters</span></span>
<span data-ttu-id="c2b16-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b16-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b16-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b16-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b16-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2b16-163">INPUTS</span></span>

### <span data-ttu-id="c2b16-164">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b16-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="c2b16-165">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b16-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="c2b16-166">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c2b16-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="c2b16-167">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c2b16-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="c2b16-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2b16-168">OUTPUTS</span></span>

### <span data-ttu-id="c2b16-169">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c2b16-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c2b16-170">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="c2b16-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="c2b16-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2b16-171">NOTES</span></span>

## <span data-ttu-id="c2b16-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2b16-172">RELATED LINKS</span></span>
