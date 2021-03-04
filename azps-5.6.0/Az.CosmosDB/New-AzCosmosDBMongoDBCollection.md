---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 3864693c5fd6da8c96557aac6f1626329f4e906f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885732"
---
# <span data-ttu-id="911a1-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="911a1-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="911a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="911a1-102">SYNOPSIS</span></span>
<span data-ttu-id="911a1-103">Cria uma nova coleção MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="911a1-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="911a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="911a1-104">SYNTAX</span></span>

### <span data-ttu-id="911a1-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="911a1-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="911a1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="911a1-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="911a1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="911a1-107">DESCRIPTION</span></span>
<span data-ttu-id="911a1-108">Cria uma nova coleção MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="911a1-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="911a1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="911a1-109">EXAMPLES</span></span>

### <span data-ttu-id="911a1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="911a1-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="911a1-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="911a1-111">PARAMETERS</span></span>

### <span data-ttu-id="911a1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="911a1-112">-AccountName</span></span>
<span data-ttu-id="911a1-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="911a1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="911a1-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="911a1-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="911a1-115">TTL para Armazenamento Analítico.</span><span class="sxs-lookup"><span data-stu-id="911a1-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="911a1-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="911a1-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="911a1-117">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="911a1-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="911a1-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="911a1-118">-Confirm</span></span>
<span data-ttu-id="911a1-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="911a1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="911a1-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="911a1-120">-DatabaseName</span></span>
<span data-ttu-id="911a1-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="911a1-121">Database name.</span></span>

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

### <span data-ttu-id="911a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="911a1-122">-DefaultProfile</span></span>
<span data-ttu-id="911a1-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="911a1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="911a1-124">-Index</span><span class="sxs-lookup"><span data-stu-id="911a1-124">-Index</span></span>
<span data-ttu-id="911a1-125">Matriz de objetos PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="911a1-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="911a1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="911a1-126">-Name</span></span>
<span data-ttu-id="911a1-127">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="911a1-127">Collection name.</span></span>

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

### <span data-ttu-id="911a1-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="911a1-128">-ParentObject</span></span>
<span data-ttu-id="911a1-129">Objeto Mongo Database.</span><span class="sxs-lookup"><span data-stu-id="911a1-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="911a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="911a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="911a1-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="911a1-131">Name of resource group.</span></span>

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

### <span data-ttu-id="911a1-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="911a1-132">-Shard</span></span>
<span data-ttu-id="911a1-133">Caminho da chave de estilhaço.</span><span class="sxs-lookup"><span data-stu-id="911a1-133">Sharding key path.</span></span>

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

### <span data-ttu-id="911a1-134">-Throughput</span><span class="sxs-lookup"><span data-stu-id="911a1-134">-Throughput</span></span>
<span data-ttu-id="911a1-135">A produtividade de SQL contêiner (RU/s).</span><span class="sxs-lookup"><span data-stu-id="911a1-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="911a1-136">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="911a1-136">Default value is 400.</span></span>

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

### <span data-ttu-id="911a1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="911a1-137">-WhatIf</span></span>
<span data-ttu-id="911a1-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="911a1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="911a1-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="911a1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="911a1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="911a1-140">CommonParameters</span></span>
<span data-ttu-id="911a1-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="911a1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="911a1-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="911a1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="911a1-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="911a1-143">INPUTS</span></span>

### <span data-ttu-id="911a1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="911a1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="911a1-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="911a1-145">OUTPUTS</span></span>

### <span data-ttu-id="911a1-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="911a1-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="911a1-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="911a1-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="911a1-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="911a1-148">NOTES</span></span>

## <span data-ttu-id="911a1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="911a1-149">RELATED LINKS</span></span>
