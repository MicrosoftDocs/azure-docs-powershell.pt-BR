---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 464dbb54a96f7f543607cd2f053a0e7360eba344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893361"
---
# <span data-ttu-id="d2a8a-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="d2a8a-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="d2a8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a8a-103">Cria um novo Gráfico de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d2a8a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2a8a-104">SYNTAX</span></span>

### <span data-ttu-id="d2a8a-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2a8a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a8a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2a8a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2a8a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2a8a-107">DESCRIPTION</span></span>
<span data-ttu-id="d2a8a-108">Cria um novo Gráfico de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d2a8a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2a8a-109">EXAMPLES</span></span>

### <span data-ttu-id="d2a8a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2a8a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="d2a8a-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2a8a-111">PARAMETERS</span></span>

### <span data-ttu-id="d2a8a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2a8a-112">-AccountName</span></span>
<span data-ttu-id="d2a8a-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d2a8a-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d2a8a-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d2a8a-115">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d2a8a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2a8a-116">-Confirm</span></span>
<span data-ttu-id="d2a8a-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2a8a-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2a8a-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="d2a8a-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="d2a8a-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d2a8a-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="d2a8a-121">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="d2a8a-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="d2a8a-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="d2a8a-123">Para ser fornecido quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="d2a8a-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="d2a8a-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="d2a8a-125">Para ser fornecido quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="d2a8a-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2a8a-126">-DatabaseName</span></span>
<span data-ttu-id="d2a8a-127">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-127">Database name.</span></span>

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

### <span data-ttu-id="d2a8a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a8a-128">-DefaultProfile</span></span>
<span data-ttu-id="d2a8a-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a8a-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d2a8a-130">-IndexingPolicy</span></span>
<span data-ttu-id="d2a8a-131">Objeto de política de indexação do tipo Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="d2a8a-132">-Name</span><span class="sxs-lookup"><span data-stu-id="d2a8a-132">-Name</span></span>
<span data-ttu-id="d2a8a-133">Nome do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d2a8a-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d2a8a-134">-ParentObject</span></span>
<span data-ttu-id="d2a8a-135">Objeto Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="d2a8a-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="d2a8a-136">-PartitionKeyKind</span></span>
<span data-ttu-id="d2a8a-137">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="d2a8a-138">Os valores possíveis incluem: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="d2a8a-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="d2a8a-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="d2a8a-139">-PartitionKeyPath</span></span>
<span data-ttu-id="d2a8a-140">Caminho da Chave de Partição, por exemplo, '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="d2a8a-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d2a8a-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="d2a8a-142">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="d2a8a-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="d2a8a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a8a-143">-ResourceGroupName</span></span>
<span data-ttu-id="d2a8a-144">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-144">Name of resource group.</span></span>

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

### <span data-ttu-id="d2a8a-145">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d2a8a-145">-Throughput</span></span>
<span data-ttu-id="d2a8a-146">A produtividade do Gráfico de Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d2a8a-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="d2a8a-147">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-147">Default value is 400.</span></span>

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

### <span data-ttu-id="d2a8a-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d2a8a-148">-TtlInSeconds</span></span>
<span data-ttu-id="d2a8a-149">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="d2a8a-150">Se o valor estiver faltando ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="d2a8a-151">Se o valor for definido como n, os itens expiram n segundos após o último tempo modificado.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="d2a8a-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d2a8a-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="d2a8a-153">Objeto UniqueKeyPolicy do tipo Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="d2a8a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a8a-154">-WhatIf</span></span>
<span data-ttu-id="d2a8a-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a8a-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2a8a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a8a-157">CommonParameters</span></span>
<span data-ttu-id="d2a8a-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a8a-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2a8a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a8a-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2a8a-160">INPUTS</span></span>

### <span data-ttu-id="d2a8a-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d2a8a-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="d2a8a-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d2a8a-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="d2a8a-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d2a8a-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="d2a8a-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d2a8a-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="d2a8a-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2a8a-165">OUTPUTS</span></span>

### <span data-ttu-id="d2a8a-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d2a8a-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="d2a8a-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d2a8a-167">System.Exception</span></span>

## <span data-ttu-id="d2a8a-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2a8a-168">NOTES</span></span>

## <span data-ttu-id="d2a8a-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2a8a-169">RELATED LINKS</span></span>
