---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944437"
---
# <span data-ttu-id="fd302-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="fd302-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="fd302-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd302-102">SYNOPSIS</span></span>
<span data-ttu-id="fd302-103">Define a coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="fd302-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="fd302-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd302-104">SYNTAX</span></span>

### <span data-ttu-id="fd302-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd302-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd302-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd302-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd302-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd302-107">DESCRIPTION</span></span>
<span data-ttu-id="fd302-108">O cmdlet **set-AzCosmosDBMongoDBCollection** define a coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="fd302-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="fd302-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd302-109">EXAMPLES</span></span>

### <span data-ttu-id="fd302-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd302-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="fd302-111">Objeto de recurso contém MongoIndexes, _rid, _ts, _etag Propriedades.</span><span class="sxs-lookup"><span data-stu-id="fd302-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="fd302-112">OS</span><span class="sxs-lookup"><span data-stu-id="fd302-112">PARAMETERS</span></span>

### <span data-ttu-id="fd302-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd302-113">-AccountName</span></span>
<span data-ttu-id="fd302-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="fd302-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fd302-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd302-115">-Confirm</span></span>
<span data-ttu-id="fd302-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd302-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd302-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd302-117">-DatabaseName</span></span>
<span data-ttu-id="fd302-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fd302-118">Database name.</span></span>

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

### <span data-ttu-id="fd302-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd302-119">-DefaultProfile</span></span>
<span data-ttu-id="fd302-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd302-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd302-121">-Índice</span><span class="sxs-lookup"><span data-stu-id="fd302-121">-Index</span></span>
<span data-ttu-id="fd302-122">Matriz de objetos PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="fd302-122">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="fd302-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd302-123">-InputObject</span></span>
<span data-ttu-id="fd302-124">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="fd302-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="fd302-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd302-125">-Name</span></span>
<span data-ttu-id="fd302-126">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="fd302-126">Collection name.</span></span>

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

### <span data-ttu-id="fd302-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd302-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd302-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd302-128">Name of resource group.</span></span>

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

### <span data-ttu-id="fd302-129">-Fragmentos</span><span class="sxs-lookup"><span data-stu-id="fd302-129">-Shard</span></span>
<span data-ttu-id="fd302-130">Caminho da chave de fragmentação.</span><span class="sxs-lookup"><span data-stu-id="fd302-130">Sharding key path.</span></span>

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

### <span data-ttu-id="fd302-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="fd302-131">-Throughput</span></span>
<span data-ttu-id="fd302-132">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="fd302-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="fd302-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="fd302-133">Default value is 400.</span></span>

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

### <span data-ttu-id="fd302-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd302-134">-WhatIf</span></span>
<span data-ttu-id="fd302-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd302-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd302-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd302-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd302-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd302-137">CommonParameters</span></span>
<span data-ttu-id="fd302-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd302-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd302-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd302-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd302-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd302-140">INPUTS</span></span>

### <span data-ttu-id="fd302-141">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fd302-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="fd302-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd302-142">OUTPUTS</span></span>

### <span data-ttu-id="fd302-143">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="fd302-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="fd302-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd302-144">NOTES</span></span>

## <span data-ttu-id="fd302-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd302-145">RELATED LINKS</span></span>
