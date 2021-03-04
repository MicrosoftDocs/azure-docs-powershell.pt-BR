---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 2458c31ba75470c5d2b5bb2b73d817eb58c5bc61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888549"
---
# <span data-ttu-id="7b624-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="7b624-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="7b624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b624-102">SYNOPSIS</span></span>
<span data-ttu-id="7b624-103">Atualiza a coleção MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7b624-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="7b624-104">Executa uma operação de patch do lado do cliente lendo a Coleção existente.</span><span class="sxs-lookup"><span data-stu-id="7b624-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="7b624-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7b624-105">SYNTAX</span></span>

### <span data-ttu-id="7b624-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7b624-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b624-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b624-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b624-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b624-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b624-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7b624-109">DESCRIPTION</span></span>
<span data-ttu-id="7b624-110">Atualiza a coleção MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7b624-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="7b624-111">Executa uma operação de patch do lado do cliente lendo a Coleção existente.</span><span class="sxs-lookup"><span data-stu-id="7b624-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="7b624-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b624-112">EXAMPLES</span></span>

### <span data-ttu-id="7b624-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b624-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="7b624-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7b624-114">PARAMETERS</span></span>

### <span data-ttu-id="7b624-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7b624-115">-AccountName</span></span>
<span data-ttu-id="7b624-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="7b624-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7b624-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="7b624-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="7b624-118">TTL para Armazenamento Analítico.</span><span class="sxs-lookup"><span data-stu-id="7b624-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="7b624-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7b624-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7b624-120">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="7b624-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7b624-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b624-121">-Confirm</span></span>
<span data-ttu-id="7b624-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b624-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b624-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7b624-123">-DatabaseName</span></span>
<span data-ttu-id="7b624-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7b624-124">Database name.</span></span>

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

### <span data-ttu-id="7b624-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b624-125">-DefaultProfile</span></span>
<span data-ttu-id="7b624-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b624-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b624-127">-Index</span><span class="sxs-lookup"><span data-stu-id="7b624-127">-Index</span></span>
<span data-ttu-id="7b624-128">Matriz de objetos PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="7b624-128">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b624-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b624-129">-InputObject</span></span>
<span data-ttu-id="7b624-130">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="7b624-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b624-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7b624-131">-Name</span></span>
<span data-ttu-id="7b624-132">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="7b624-132">Collection name.</span></span>

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

### <span data-ttu-id="7b624-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7b624-133">-ParentObject</span></span>
<span data-ttu-id="7b624-134">Objeto Mongo Database.</span><span class="sxs-lookup"><span data-stu-id="7b624-134">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b624-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b624-135">-ResourceGroupName</span></span>
<span data-ttu-id="7b624-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b624-136">Name of resource group.</span></span>

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

### <span data-ttu-id="7b624-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="7b624-137">-Shard</span></span>
<span data-ttu-id="7b624-138">Caminho da chave de estilhaço.</span><span class="sxs-lookup"><span data-stu-id="7b624-138">Sharding key path.</span></span>

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

### <span data-ttu-id="7b624-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="7b624-139">-Throughput</span></span>
<span data-ttu-id="7b624-140">A produtividade de SQL contêiner (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7b624-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="7b624-141">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="7b624-141">Default value is 400.</span></span>

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

### <span data-ttu-id="7b624-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b624-142">-WhatIf</span></span>
<span data-ttu-id="7b624-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b624-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b624-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b624-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b624-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b624-145">CommonParameters</span></span>
<span data-ttu-id="7b624-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b624-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b624-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b624-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b624-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b624-148">INPUTS</span></span>

### <span data-ttu-id="7b624-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7b624-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="7b624-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="7b624-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="7b624-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7b624-151">OUTPUTS</span></span>

### <span data-ttu-id="7b624-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="7b624-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="7b624-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7b624-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7b624-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="7b624-154">NOTES</span></span>

## <span data-ttu-id="7b624-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b624-155">RELATED LINKS</span></span>
