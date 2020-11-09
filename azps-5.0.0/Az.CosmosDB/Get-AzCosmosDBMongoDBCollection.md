---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281393"
---
# <span data-ttu-id="6fc57-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="6fc57-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="6fc57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fc57-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc57-103">Obtém a coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="6fc57-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="6fc57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fc57-104">SYNTAX</span></span>

### <span data-ttu-id="6fc57-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6fc57-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="6fc57-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fc57-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fc57-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fc57-107">DESCRIPTION</span></span>
<span data-ttu-id="6fc57-108">O cmdlet **Get-AzCosmosDBMongoDBCollection** Obtém a coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="6fc57-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="6fc57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fc57-109">EXAMPLES</span></span>

### <span data-ttu-id="6fc57-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6fc57-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="6fc57-111">Objeto de recurso contém MongoIndexes, _rid, _ts, _etag Propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fc57-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="6fc57-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6fc57-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="6fc57-113">Este exemplo obtém a ShardKey da coleção recuperada</span><span class="sxs-lookup"><span data-stu-id="6fc57-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="6fc57-114">OS</span><span class="sxs-lookup"><span data-stu-id="6fc57-114">PARAMETERS</span></span>

### <span data-ttu-id="6fc57-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6fc57-115">-AccountName</span></span>
<span data-ttu-id="6fc57-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="6fc57-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6fc57-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6fc57-117">-DatabaseName</span></span>
<span data-ttu-id="6fc57-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc57-118">Database name.</span></span>

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

### <span data-ttu-id="6fc57-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc57-119">-DefaultProfile</span></span>
<span data-ttu-id="6fc57-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fc57-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fc57-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fc57-121">-Name</span></span>
<span data-ttu-id="6fc57-122">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="6fc57-122">Collection name.</span></span>

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

### <span data-ttu-id="6fc57-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6fc57-123">-ParentObject</span></span>
<span data-ttu-id="6fc57-124">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="6fc57-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="6fc57-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc57-125">-ResourceGroupName</span></span>
<span data-ttu-id="6fc57-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6fc57-126">Name of resource group.</span></span>

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

### <span data-ttu-id="6fc57-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc57-127">CommonParameters</span></span>
<span data-ttu-id="6fc57-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc57-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc57-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fc57-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc57-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fc57-130">INPUTS</span></span>

### <span data-ttu-id="6fc57-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6fc57-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="6fc57-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fc57-132">OUTPUTS</span></span>

### <span data-ttu-id="6fc57-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="6fc57-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="6fc57-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6fc57-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6fc57-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fc57-135">NOTES</span></span>

## <span data-ttu-id="6fc57-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fc57-136">RELATED LINKS</span></span>
