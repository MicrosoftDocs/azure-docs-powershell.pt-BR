---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 500bd1203f7f70b5749986a6b4ff1ab8d5978185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888552"
---
# <span data-ttu-id="d0126-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="d0126-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="d0126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0126-102">SYNOPSIS</span></span>
<span data-ttu-id="d0126-103">Atualiza o Gráfico de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d0126-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="d0126-104">Executa uma operação de patch do lado do cliente lendo o Graph existente.</span><span class="sxs-lookup"><span data-stu-id="d0126-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="d0126-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d0126-105">SYNTAX</span></span>

### <span data-ttu-id="d0126-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d0126-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0126-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0126-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0126-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0126-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0126-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d0126-109">DESCRIPTION</span></span>
<span data-ttu-id="d0126-110">Atualiza o Gráfico de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d0126-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="d0126-111">Executa uma operação de patch do lado do cliente lendo o Graph existente.</span><span class="sxs-lookup"><span data-stu-id="d0126-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="d0126-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0126-112">EXAMPLES</span></span>

### <span data-ttu-id="d0126-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0126-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="d0126-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d0126-114">PARAMETERS</span></span>

### <span data-ttu-id="d0126-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0126-115">-AccountName</span></span>
<span data-ttu-id="d0126-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="d0126-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d0126-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d0126-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d0126-118">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="d0126-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d0126-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0126-119">-Confirm</span></span>
<span data-ttu-id="d0126-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0126-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0126-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0126-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="d0126-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span><span class="sxs-lookup"><span data-stu-id="d0126-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="d0126-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d0126-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="d0126-124">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="d0126-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="d0126-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="d0126-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="d0126-126">Para ser fornecido quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="d0126-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="d0126-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="d0126-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="d0126-128">Para ser fornecido quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="d0126-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="d0126-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0126-129">-DatabaseName</span></span>
<span data-ttu-id="d0126-130">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d0126-130">Database name.</span></span>

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

### <span data-ttu-id="d0126-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0126-131">-DefaultProfile</span></span>
<span data-ttu-id="d0126-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0126-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0126-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d0126-133">-IndexingPolicy</span></span>
<span data-ttu-id="d0126-134">Objeto de política de indexação do tipo Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="d0126-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="d0126-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0126-135">-InputObject</span></span>
<span data-ttu-id="d0126-136">Objeto Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="d0126-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="d0126-137">-Name</span><span class="sxs-lookup"><span data-stu-id="d0126-137">-Name</span></span>
<span data-ttu-id="d0126-138">Nome do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d0126-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d0126-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0126-139">-ParentObject</span></span>
<span data-ttu-id="d0126-140">Objeto Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="d0126-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="d0126-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="d0126-141">-PartitionKeyKind</span></span>
<span data-ttu-id="d0126-142">O tipo de algoritmo usado para particionamento.</span><span class="sxs-lookup"><span data-stu-id="d0126-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="d0126-143">Os valores possíveis incluem: 'Hash', 'Range'</span><span class="sxs-lookup"><span data-stu-id="d0126-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="d0126-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="d0126-144">-PartitionKeyPath</span></span>
<span data-ttu-id="d0126-145">Caminho da Chave de Partição, por exemplo, '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="d0126-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="d0126-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d0126-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="d0126-147">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="d0126-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="d0126-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0126-148">-ResourceGroupName</span></span>
<span data-ttu-id="d0126-149">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0126-149">Name of resource group.</span></span>

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

### <span data-ttu-id="d0126-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d0126-150">-Throughput</span></span>
<span data-ttu-id="d0126-151">A produtividade do Gráfico de Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d0126-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="d0126-152">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="d0126-152">Default value is 400.</span></span>

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

### <span data-ttu-id="d0126-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d0126-153">-TtlInSeconds</span></span>
<span data-ttu-id="d0126-154">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="d0126-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="d0126-155">Se o valor estiver faltando ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="d0126-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="d0126-156">Se o valor for definido como n, os itens expiram n segundos após o último tempo modificado.</span><span class="sxs-lookup"><span data-stu-id="d0126-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="d0126-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d0126-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="d0126-158">Objeto UniqueKeyPolicy do tipo Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="d0126-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="d0126-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0126-159">-WhatIf</span></span>
<span data-ttu-id="d0126-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d0126-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0126-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0126-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0126-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0126-162">CommonParameters</span></span>
<span data-ttu-id="d0126-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0126-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0126-164">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0126-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0126-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0126-165">INPUTS</span></span>

### <span data-ttu-id="d0126-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d0126-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="d0126-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d0126-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="d0126-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0126-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="d0126-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d0126-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="d0126-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d0126-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="d0126-171">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d0126-171">OUTPUTS</span></span>

### <span data-ttu-id="d0126-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d0126-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="d0126-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d0126-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d0126-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="d0126-174">NOTES</span></span>

## <span data-ttu-id="d0126-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0126-175">RELATED LINKS</span></span>
