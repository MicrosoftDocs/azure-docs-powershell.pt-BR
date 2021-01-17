---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434068"
---
# <span data-ttu-id="f2659-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="f2659-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="f2659-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2659-102">SYNOPSIS</span></span>
<span data-ttu-id="f2659-103">Cria um novo gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f2659-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f2659-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2659-104">SYNTAX</span></span>

### <span data-ttu-id="f2659-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2659-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2659-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2659-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2659-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2659-107">DESCRIPTION</span></span>
<span data-ttu-id="f2659-108">Cria um novo gráfico CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f2659-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f2659-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2659-109">EXAMPLES</span></span>

### <span data-ttu-id="f2659-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2659-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="f2659-111">OS</span><span class="sxs-lookup"><span data-stu-id="f2659-111">PARAMETERS</span></span>

### <span data-ttu-id="f2659-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2659-112">-AccountName</span></span>
<span data-ttu-id="f2659-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="f2659-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f2659-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f2659-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f2659-115">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="f2659-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f2659-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2659-116">-Confirm</span></span>
<span data-ttu-id="f2659-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2659-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2659-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2659-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f2659-119">ConflictResolutionPolicy objeto do tipo PSConflictResolutionPolicy, quando fornecido, é definido como o ConflictResolutionPolicy do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f2659-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f2659-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f2659-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f2659-121">Pode ter os valores: LastWriterWins, Custom, manual.</span><span class="sxs-lookup"><span data-stu-id="f2659-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="f2659-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f2659-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f2659-123">Seja fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="f2659-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="f2659-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f2659-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f2659-125">Seja fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="f2659-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="f2659-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2659-126">-DatabaseName</span></span>
<span data-ttu-id="f2659-127">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f2659-127">Database name.</span></span>

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

### <span data-ttu-id="f2659-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2659-128">-DefaultProfile</span></span>
<span data-ttu-id="f2659-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2659-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2659-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f2659-130">-IndexingPolicy</span></span>
<span data-ttu-id="f2659-131">Objeto de política de indexação do tipo Microsoft. Azure. Commands. CosmosDB. PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f2659-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="f2659-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2659-132">-Name</span></span>
<span data-ttu-id="f2659-133">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="f2659-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f2659-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f2659-134">-ParentObject</span></span>
<span data-ttu-id="f2659-135">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="f2659-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f2659-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="f2659-136">-PartitionKeyKind</span></span>
<span data-ttu-id="f2659-137">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="f2659-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f2659-138">Os valores possíveis incluem: ' hash ', ' intervalo '</span><span class="sxs-lookup"><span data-stu-id="f2659-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f2659-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f2659-139">-PartitionKeyPath</span></span>
<span data-ttu-id="f2659-140">Caminho da chave da partição, por exemplo, '/address/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="f2659-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f2659-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f2659-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="f2659-142">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="f2659-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f2659-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2659-143">-ResourceGroupName</span></span>
<span data-ttu-id="f2659-144">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2659-144">Name of resource group.</span></span>

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

### <span data-ttu-id="f2659-145">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f2659-145">-Throughput</span></span>
<span data-ttu-id="f2659-146">O throughput do Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f2659-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="f2659-147">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="f2659-147">Default value is 400.</span></span>

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

### <span data-ttu-id="f2659-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f2659-148">-TtlInSeconds</span></span>
<span data-ttu-id="f2659-149">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="f2659-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="f2659-150">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="f2659-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f2659-151">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="f2659-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f2659-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f2659-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f2659-153">UniqueKeyPolicy objeto do tipo Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="f2659-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f2659-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2659-154">-WhatIf</span></span>
<span data-ttu-id="f2659-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2659-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2659-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2659-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2659-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2659-157">CommonParameters</span></span>
<span data-ttu-id="f2659-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2659-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2659-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2659-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2659-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2659-160">INPUTS</span></span>

### <span data-ttu-id="f2659-161">Microsoft. Azure. Commands. CosmosDB. Models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f2659-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="f2659-162">Microsoft. Azure. Commands. CosmosDB. Models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f2659-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="f2659-163">Microsoft. Azure. Commands. CosmosDB. Models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2659-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="f2659-164">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f2659-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="f2659-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2659-165">OUTPUTS</span></span>

### <span data-ttu-id="f2659-166">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="f2659-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="f2659-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f2659-167">System.Exception</span></span>

## <span data-ttu-id="f2659-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2659-168">NOTES</span></span>

## <span data-ttu-id="f2659-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2659-169">RELATED LINKS</span></span>
