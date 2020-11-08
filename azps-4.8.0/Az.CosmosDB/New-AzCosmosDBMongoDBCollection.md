---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114629"
---
# <span data-ttu-id="6ea2f-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="6ea2f-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="6ea2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ea2f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea2f-103">Cria uma nova coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="6ea2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ea2f-104">SYNTAX</span></span>

### <span data-ttu-id="6ea2f-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ea2f-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea2f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ea2f-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ea2f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ea2f-107">DESCRIPTION</span></span>
<span data-ttu-id="6ea2f-108">Cria uma nova coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="6ea2f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ea2f-109">EXAMPLES</span></span>

### <span data-ttu-id="6ea2f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ea2f-110">Example 1</span></span>
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

## <span data-ttu-id="6ea2f-111">OS</span><span class="sxs-lookup"><span data-stu-id="6ea2f-111">PARAMETERS</span></span>

### <span data-ttu-id="6ea2f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6ea2f-112">-AccountName</span></span>
<span data-ttu-id="6ea2f-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6ea2f-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="6ea2f-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="6ea2f-115">TTL para armazenamento analítico.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="6ea2f-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6ea2f-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6ea2f-117">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6ea2f-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ea2f-118">-Confirm</span></span>
<span data-ttu-id="6ea2f-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ea2f-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ea2f-120">-DatabaseName</span></span>
<span data-ttu-id="6ea2f-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-121">Database name.</span></span>

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

### <span data-ttu-id="6ea2f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea2f-122">-DefaultProfile</span></span>
<span data-ttu-id="6ea2f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ea2f-124">-Índice</span><span class="sxs-lookup"><span data-stu-id="6ea2f-124">-Index</span></span>
<span data-ttu-id="6ea2f-125">Matriz de objetos PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="6ea2f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ea2f-126">-Name</span></span>
<span data-ttu-id="6ea2f-127">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-127">Collection name.</span></span>

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

### <span data-ttu-id="6ea2f-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6ea2f-128">-ParentObject</span></span>
<span data-ttu-id="6ea2f-129">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="6ea2f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea2f-130">-ResourceGroupName</span></span>
<span data-ttu-id="6ea2f-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-131">Name of resource group.</span></span>

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

### <span data-ttu-id="6ea2f-132">-Fragmentos</span><span class="sxs-lookup"><span data-stu-id="6ea2f-132">-Shard</span></span>
<span data-ttu-id="6ea2f-133">Caminho da chave de fragmentação.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-133">Sharding key path.</span></span>

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

### <span data-ttu-id="6ea2f-134">-Throughput</span><span class="sxs-lookup"><span data-stu-id="6ea2f-134">-Throughput</span></span>
<span data-ttu-id="6ea2f-135">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6ea2f-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="6ea2f-136">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-136">Default value is 400.</span></span>

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

### <span data-ttu-id="6ea2f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea2f-137">-WhatIf</span></span>
<span data-ttu-id="6ea2f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ea2f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ea2f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea2f-140">CommonParameters</span></span>
<span data-ttu-id="6ea2f-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea2f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea2f-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ea2f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea2f-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ea2f-143">INPUTS</span></span>

### <span data-ttu-id="6ea2f-144">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6ea2f-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="6ea2f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ea2f-145">OUTPUTS</span></span>

### <span data-ttu-id="6ea2f-146">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="6ea2f-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="6ea2f-147">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="6ea2f-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="6ea2f-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ea2f-148">NOTES</span></span>

## <span data-ttu-id="6ea2f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ea2f-149">RELATED LINKS</span></span>
