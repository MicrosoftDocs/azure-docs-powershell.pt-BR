---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115077"
---
# <span data-ttu-id="8d18f-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="8d18f-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="8d18f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d18f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d18f-103">Atualiza o gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8d18f-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="8d18f-104">Executa uma operação de patch do lado do cliente lendo o gráfico existente.</span><span class="sxs-lookup"><span data-stu-id="8d18f-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="8d18f-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d18f-105">SYNTAX</span></span>

### <span data-ttu-id="8d18f-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d18f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d18f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d18f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d18f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d18f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d18f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d18f-109">DESCRIPTION</span></span>
<span data-ttu-id="8d18f-110">Atualiza o gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8d18f-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="8d18f-111">Executa uma operação de patch do lado do cliente lendo o gráfico existente.</span><span class="sxs-lookup"><span data-stu-id="8d18f-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="8d18f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d18f-112">EXAMPLES</span></span>

### <span data-ttu-id="8d18f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d18f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="8d18f-114">OS</span><span class="sxs-lookup"><span data-stu-id="8d18f-114">PARAMETERS</span></span>

### <span data-ttu-id="8d18f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d18f-115">-AccountName</span></span>
<span data-ttu-id="8d18f-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="8d18f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8d18f-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8d18f-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8d18f-118">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="8d18f-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8d18f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d18f-119">-Confirm</span></span>
<span data-ttu-id="8d18f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d18f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d18f-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d18f-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="8d18f-122">ConflictResolutionPolicy objeto do tipo PSConflictResolutionPolicy, quando fornecido, é definido como o ConflictResolutionPolicy do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8d18f-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="8d18f-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="8d18f-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="8d18f-124">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="8d18f-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="8d18f-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="8d18f-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="8d18f-126">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="8d18f-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="8d18f-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="8d18f-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="8d18f-128">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="8d18f-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="8d18f-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d18f-129">-DatabaseName</span></span>
<span data-ttu-id="8d18f-130">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8d18f-130">Database name.</span></span>

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

### <span data-ttu-id="8d18f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d18f-131">-DefaultProfile</span></span>
<span data-ttu-id="8d18f-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d18f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d18f-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="8d18f-133">-IndexingPolicy</span></span>
<span data-ttu-id="8d18f-134">Objeto de política de indexação do tipo Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d18f-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="8d18f-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d18f-135">-InputObject</span></span>
<span data-ttu-id="8d18f-136">Objeto de gráfico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8d18f-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d18f-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d18f-137">-Name</span></span>
<span data-ttu-id="8d18f-138">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="8d18f-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="8d18f-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8d18f-139">-ParentObject</span></span>
<span data-ttu-id="8d18f-140">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="8d18f-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="8d18f-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="8d18f-141">-PartitionKeyKind</span></span>
<span data-ttu-id="8d18f-142">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="8d18f-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="8d18f-143">Os valores possíveis incluem: ' hash ', ' intervalo '</span><span class="sxs-lookup"><span data-stu-id="8d18f-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="8d18f-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="8d18f-144">-PartitionKeyPath</span></span>
<span data-ttu-id="8d18f-145">Caminho da chave da partição, por exemplo, '/address/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="8d18f-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="8d18f-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="8d18f-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="8d18f-147">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="8d18f-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="8d18f-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d18f-148">-ResourceGroupName</span></span>
<span data-ttu-id="8d18f-149">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d18f-149">Name of resource group.</span></span>

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

### <span data-ttu-id="8d18f-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="8d18f-150">-Throughput</span></span>
<span data-ttu-id="8d18f-151">O throughput do Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8d18f-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="8d18f-152">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="8d18f-152">Default value is 400.</span></span>

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

### <span data-ttu-id="8d18f-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="8d18f-153">-TtlInSeconds</span></span>
<span data-ttu-id="8d18f-154">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="8d18f-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="8d18f-155">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="8d18f-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="8d18f-156">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="8d18f-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="8d18f-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="8d18f-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="8d18f-158">UniqueKeyPolicy objeto do tipo Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d18f-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="8d18f-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d18f-159">-WhatIf</span></span>
<span data-ttu-id="8d18f-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d18f-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d18f-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d18f-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d18f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d18f-162">CommonParameters</span></span>
<span data-ttu-id="8d18f-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d18f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d18f-164">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d18f-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d18f-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d18f-165">INPUTS</span></span>

### <span data-ttu-id="8d18f-166">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="8d18f-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="8d18f-167">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="8d18f-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="8d18f-168">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d18f-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="8d18f-169">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8d18f-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="8d18f-170">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="8d18f-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="8d18f-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d18f-171">OUTPUTS</span></span>

### <span data-ttu-id="8d18f-172">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="8d18f-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="8d18f-173">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8d18f-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="8d18f-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d18f-174">NOTES</span></span>

## <span data-ttu-id="8d18f-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d18f-175">RELATED LINKS</span></span>
