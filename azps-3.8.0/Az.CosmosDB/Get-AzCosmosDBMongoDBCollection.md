---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944120"
---
# <span data-ttu-id="59853-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="59853-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="59853-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59853-102">SYNOPSIS</span></span>
<span data-ttu-id="59853-103">Obtém a coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="59853-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="59853-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59853-104">SYNTAX</span></span>

### <span data-ttu-id="59853-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="59853-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="59853-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59853-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59853-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59853-107">DESCRIPTION</span></span>
<span data-ttu-id="59853-108">O cmdlet **Get-AzCosmosDBMongoDBCollection** Obtém a coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="59853-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="59853-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59853-109">EXAMPLES</span></span>

### <span data-ttu-id="59853-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59853-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="59853-111">Objeto de recurso contém MongoIndexes, _rid, _ts, _etag Propriedades.</span><span class="sxs-lookup"><span data-stu-id="59853-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="59853-112">OS</span><span class="sxs-lookup"><span data-stu-id="59853-112">PARAMETERS</span></span>

### <span data-ttu-id="59853-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="59853-113">-AccountName</span></span>
<span data-ttu-id="59853-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="59853-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="59853-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59853-115">-DatabaseName</span></span>
<span data-ttu-id="59853-116">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="59853-116">Database name.</span></span>

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

### <span data-ttu-id="59853-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59853-117">-DefaultProfile</span></span>
<span data-ttu-id="59853-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59853-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59853-119">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="59853-119">-Detailed</span></span>
<span data-ttu-id="59853-120">Se fornecido, o cmdlet retornará a coleção com o valor de produtividade correspondente.</span><span class="sxs-lookup"><span data-stu-id="59853-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59853-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59853-121">-InputObject</span></span>
<span data-ttu-id="59853-122">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="59853-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="59853-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="59853-123">-Name</span></span>
<span data-ttu-id="59853-124">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="59853-124">Collection name.</span></span>

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

### <span data-ttu-id="59853-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59853-125">-ResourceGroupName</span></span>
<span data-ttu-id="59853-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59853-126">Name of resource group.</span></span>

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

### <span data-ttu-id="59853-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59853-127">CommonParameters</span></span>
<span data-ttu-id="59853-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59853-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59853-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59853-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59853-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59853-130">INPUTS</span></span>

### <span data-ttu-id="59853-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="59853-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="59853-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59853-132">OUTPUTS</span></span>

### <span data-ttu-id="59853-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="59853-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="59853-134">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="59853-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="59853-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59853-135">NOTES</span></span>

## <span data-ttu-id="59853-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59853-136">RELATED LINKS</span></span>
