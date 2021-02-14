---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 7b773bd51a928c21761900cf1f6f8c34e73c2d0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111028"
---
# <span data-ttu-id="f3ea7-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="f3ea7-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="f3ea7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ea7-103">Cria um novo Contêiner Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f3ea7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3ea7-104">SYNTAX</span></span>

### <span data-ttu-id="f3ea7-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f3ea7-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ea7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ea7-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3ea7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3ea7-107">DESCRIPTION</span></span>
<span data-ttu-id="f3ea7-108">Cria um novo Contêiner Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f3ea7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3ea7-109">EXAMPLES</span></span>

### <span data-ttu-id="f3ea7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3ea7-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="f3ea7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3ea7-111">PARAMETERS</span></span>

### <span data-ttu-id="f3ea7-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="f3ea7-112">-AccountName</span></span>
<span data-ttu-id="f3ea7-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f3ea7-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="f3ea7-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="f3ea7-115">TTL para Armazenamento Analítico (em Segundos).</span><span class="sxs-lookup"><span data-stu-id="f3ea7-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="f3ea7-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f3ea7-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f3ea7-117">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f3ea7-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f3ea7-118">-Confirm</span></span>
<span data-ttu-id="f3ea7-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ea7-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f3ea7-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f3ea7-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as conflictResolutionPolicy of the container.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f3ea7-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f3ea7-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f3ea7-123">Pode ter os valores: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="f3ea7-124">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f3ea7-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f3ea7-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f3ea7-126">A ser fornecida quando o tipo for LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="f3ea7-127">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f3ea7-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f3ea7-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f3ea7-129">A ser fornecida quando o tipo for personalizado.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="f3ea7-130">Se fornecido juntamente com o parâmetro ConflictResolutionPolicy, ele será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f3ea7-131">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="f3ea7-131">-DatabaseName</span></span>
<span data-ttu-id="f3ea7-132">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-132">Database name.</span></span>

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

### <span data-ttu-id="f3ea7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ea7-133">-DefaultProfile</span></span>
<span data-ttu-id="f3ea7-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ea7-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f3ea7-135">-IndexingPolicy</span></span>
<span data-ttu-id="f3ea7-136">Objeto de política de indexação do tipo Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="f3ea7-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3ea7-137">-Name</span></span>
<span data-ttu-id="f3ea7-138">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-138">Container name.</span></span>

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

### <span data-ttu-id="f3ea7-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f3ea7-139">-ParentObject</span></span>
<span data-ttu-id="f3ea7-140">Objeto banco de dados sql.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-140">Sql Database object.</span></span>

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

### <span data-ttu-id="f3ea7-141">-PartitionKeyKeyKey</span><span class="sxs-lookup"><span data-stu-id="f3ea7-141">-PartitionKeyKind</span></span>
<span data-ttu-id="f3ea7-142">O tipo de algoritmo usado para particionar.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f3ea7-143">Os valores possíveis incluem: 'Hash', 'Intervalo'</span><span class="sxs-lookup"><span data-stu-id="f3ea7-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f3ea7-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f3ea7-144">-PartitionKeyPath</span></span>
<span data-ttu-id="f3ea7-145">Caminho da Chave de Partição, por exemplo, '/endereço/cep'.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f3ea7-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f3ea7-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="f3ea7-147">A versão da definição da chave de partição</span><span class="sxs-lookup"><span data-stu-id="f3ea7-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f3ea7-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ea7-148">-ResourceGroupName</span></span>
<span data-ttu-id="f3ea7-149">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-149">Name of resource group.</span></span>

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

### <span data-ttu-id="f3ea7-150">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="f3ea7-150">-Throughput</span></span>
<span data-ttu-id="f3ea7-151">A produtividade do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f3ea7-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="f3ea7-152">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-152">Default value is 400.</span></span>

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

### <span data-ttu-id="f3ea7-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f3ea7-153">-TtlInSeconds</span></span>
<span data-ttu-id="f3ea7-154">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="f3ea7-155">Se o valor estiver ausente ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f3ea7-156">Se o valor estiver definido como n, os itens expiram n segundos após o tempo da última modificação.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f3ea7-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f3ea7-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f3ea7-158">Objeto UniqueKeyPolicy do tipo Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f3ea7-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ea7-159">-WhatIf</span></span>
<span data-ttu-id="f3ea7-160">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ea7-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ea7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ea7-162">CommonParameters</span></span>
<span data-ttu-id="f3ea7-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ea7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ea7-164">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3ea7-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ea7-165">Entradas</span><span class="sxs-lookup"><span data-stu-id="f3ea7-165">INPUTS</span></span>

### <span data-ttu-id="f3ea7-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f3ea7-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="f3ea7-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f3ea7-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="f3ea7-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f3ea7-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="f3ea7-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f3ea7-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="f3ea7-170">Saídas</span><span class="sxs-lookup"><span data-stu-id="f3ea7-170">OUTPUTS</span></span>

### <span data-ttu-id="f3ea7-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f3ea7-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f3ea7-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="f3ea7-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f3ea7-173">Notas</span><span class="sxs-lookup"><span data-stu-id="f3ea7-173">NOTES</span></span>

## <span data-ttu-id="f3ea7-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3ea7-174">RELATED LINKS</span></span>
