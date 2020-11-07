---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944438"
---
# <span data-ttu-id="c26aa-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="c26aa-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="c26aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c26aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c26aa-103">Define o gráfico de Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c26aa-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="c26aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c26aa-104">SYNTAX</span></span>

### <span data-ttu-id="c26aa-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c26aa-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c26aa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c26aa-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c26aa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c26aa-107">DESCRIPTION</span></span>
<span data-ttu-id="c26aa-108">O cmdlet **set-AzCosmosDBGremlinGraph** define um gráfico de Gremlin de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c26aa-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="c26aa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c26aa-109">EXAMPLES</span></span>

### <span data-ttu-id="c26aa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c26aa-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="c26aa-111">Objeto de recurso contém IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="c26aa-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="c26aa-112">OS</span><span class="sxs-lookup"><span data-stu-id="c26aa-112">PARAMETERS</span></span>

### <span data-ttu-id="c26aa-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c26aa-113">-AccountName</span></span>
<span data-ttu-id="c26aa-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c26aa-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c26aa-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c26aa-115">-Confirm</span></span>
<span data-ttu-id="c26aa-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c26aa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c26aa-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c26aa-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="c26aa-118">ConflictResolutionPolicy objeto do tipo PSConflictResolutionPolicy, quando fornecido, é definido como o ConflictResolutionPolicy do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c26aa-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c26aa-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="c26aa-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="c26aa-120">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="c26aa-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="c26aa-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="c26aa-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="c26aa-122">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="c26aa-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="c26aa-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="c26aa-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="c26aa-124">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="c26aa-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="c26aa-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c26aa-125">-DatabaseName</span></span>
<span data-ttu-id="c26aa-126">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c26aa-126">Database name.</span></span>

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

### <span data-ttu-id="c26aa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26aa-127">-DefaultProfile</span></span>
<span data-ttu-id="c26aa-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c26aa-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c26aa-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c26aa-129">-IndexingPolicy</span></span>
<span data-ttu-id="c26aa-130">Objeto de política de indexação do tipo Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="c26aa-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c26aa-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c26aa-131">-InputObject</span></span>
<span data-ttu-id="c26aa-132">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c26aa-132">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c26aa-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="c26aa-133">-Name</span></span>
<span data-ttu-id="c26aa-134">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="c26aa-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="c26aa-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="c26aa-135">-PartitionKeyKind</span></span>
<span data-ttu-id="c26aa-136">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="c26aa-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="c26aa-137">Os valores possíveis incluem: ' hash ', ' intervalo '</span><span class="sxs-lookup"><span data-stu-id="c26aa-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="c26aa-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="c26aa-138">-PartitionKeyPath</span></span>
<span data-ttu-id="c26aa-139">Caminho da chave da partição, por exemplo, '/address/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="c26aa-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="c26aa-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c26aa-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="c26aa-141">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="c26aa-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="c26aa-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c26aa-142">-ResourceGroupName</span></span>
<span data-ttu-id="c26aa-143">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c26aa-143">Name of resource group.</span></span>

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

### <span data-ttu-id="c26aa-144">-Throughput</span><span class="sxs-lookup"><span data-stu-id="c26aa-144">-Throughput</span></span>
<span data-ttu-id="c26aa-145">O throughput do Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c26aa-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="c26aa-146">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="c26aa-146">Default value is 400.</span></span>

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

### <span data-ttu-id="c26aa-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c26aa-147">-TtlInSeconds</span></span>
<span data-ttu-id="c26aa-148">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="c26aa-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="c26aa-149">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="c26aa-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="c26aa-150">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="c26aa-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="c26aa-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c26aa-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="c26aa-152">UniqueKeyPolicy objeto do tipo Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="c26aa-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c26aa-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c26aa-153">-WhatIf</span></span>
<span data-ttu-id="c26aa-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c26aa-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c26aa-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c26aa-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c26aa-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26aa-156">CommonParameters</span></span>
<span data-ttu-id="c26aa-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c26aa-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26aa-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c26aa-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26aa-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c26aa-159">INPUTS</span></span>

### <span data-ttu-id="c26aa-160">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c26aa-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="c26aa-161">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c26aa-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="c26aa-162">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c26aa-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="c26aa-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c26aa-163">OUTPUTS</span></span>

### <span data-ttu-id="c26aa-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="c26aa-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="c26aa-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c26aa-165">NOTES</span></span>

## <span data-ttu-id="c26aa-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c26aa-166">RELATED LINKS</span></span>
