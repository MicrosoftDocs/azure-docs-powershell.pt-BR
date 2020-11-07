---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944425"
---
# <span data-ttu-id="2797f-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="2797f-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="2797f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2797f-102">SYNOPSIS</span></span>
<span data-ttu-id="2797f-103">Cria um novo ou atualiza um contêiner SQL do CosmosDB existente.</span><span class="sxs-lookup"><span data-stu-id="2797f-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="2797f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2797f-104">SYNTAX</span></span>

### <span data-ttu-id="2797f-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2797f-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2797f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2797f-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2797f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2797f-107">DESCRIPTION</span></span>
<span data-ttu-id="2797f-108">O cmdlet **set-AzCosmosDBSqlContainer** cria um novo ou atualiza um contêiner SQL existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2797f-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="2797f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2797f-109">EXAMPLES</span></span>

### <span data-ttu-id="2797f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2797f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="2797f-111">OS</span><span class="sxs-lookup"><span data-stu-id="2797f-111">PARAMETERS</span></span>

### <span data-ttu-id="2797f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2797f-112">-AccountName</span></span>
<span data-ttu-id="2797f-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="2797f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2797f-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2797f-114">-Confirm</span></span>
<span data-ttu-id="2797f-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2797f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2797f-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="2797f-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="2797f-117">ConflictResolutionPolicy objeto do tipo PSSqlConflictResolutionPolicy, quando fornecido, é definido como o ConflictResolutionPolicy do contêiner.</span><span class="sxs-lookup"><span data-stu-id="2797f-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="2797f-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="2797f-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="2797f-119">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="2797f-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="2797f-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="2797f-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="2797f-121">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="2797f-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="2797f-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="2797f-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="2797f-123">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="2797f-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="2797f-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2797f-124">-DatabaseName</span></span>
<span data-ttu-id="2797f-125">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2797f-125">Database name.</span></span>

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

### <span data-ttu-id="2797f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2797f-126">-DefaultProfile</span></span>
<span data-ttu-id="2797f-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2797f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2797f-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2797f-128">-IndexingPolicy</span></span>
<span data-ttu-id="2797f-129">Objeto de política de indexação do tipo Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="2797f-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="2797f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2797f-130">-InputObject</span></span>
<span data-ttu-id="2797f-131">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="2797f-131">Sql Database object.</span></span>

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

### <span data-ttu-id="2797f-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="2797f-132">-Name</span></span>
<span data-ttu-id="2797f-133">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="2797f-133">Container name.</span></span>

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

### <span data-ttu-id="2797f-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="2797f-134">-PartitionKeyKind</span></span>
<span data-ttu-id="2797f-135">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="2797f-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="2797f-136">Os valores possíveis incluem: ' hash ', ' intervalo '</span><span class="sxs-lookup"><span data-stu-id="2797f-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="2797f-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="2797f-137">-PartitionKeyPath</span></span>
<span data-ttu-id="2797f-138">Caminho da chave da partição, por exemplo, '/address/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="2797f-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="2797f-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="2797f-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="2797f-140">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="2797f-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="2797f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2797f-141">-ResourceGroupName</span></span>
<span data-ttu-id="2797f-142">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2797f-142">Name of resource group.</span></span>

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

### <span data-ttu-id="2797f-143">-Throughput</span><span class="sxs-lookup"><span data-stu-id="2797f-143">-Throughput</span></span>
<span data-ttu-id="2797f-144">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="2797f-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="2797f-145">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="2797f-145">Default value is 400.</span></span>

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

### <span data-ttu-id="2797f-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="2797f-146">-TtlInSeconds</span></span>
<span data-ttu-id="2797f-147">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="2797f-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="2797f-148">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="2797f-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="2797f-149">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="2797f-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="2797f-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2797f-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="2797f-151">UniqueKeyPolicy objeto do tipo Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="2797f-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="2797f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2797f-152">-WhatIf</span></span>
<span data-ttu-id="2797f-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2797f-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2797f-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2797f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2797f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2797f-155">CommonParameters</span></span>
<span data-ttu-id="2797f-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2797f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2797f-157">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2797f-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2797f-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2797f-158">INPUTS</span></span>

### <span data-ttu-id="2797f-159">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2797f-159">None</span></span>

## <span data-ttu-id="2797f-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2797f-160">OUTPUTS</span></span>

### <span data-ttu-id="2797f-161">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2797f-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="2797f-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2797f-162">NOTES</span></span>

## <span data-ttu-id="2797f-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2797f-163">RELATED LINKS</span></span>
