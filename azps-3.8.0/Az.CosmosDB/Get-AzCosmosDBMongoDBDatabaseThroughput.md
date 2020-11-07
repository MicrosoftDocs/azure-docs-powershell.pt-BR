---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1d470870d27001a07302240dba1abd7e56153d0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944107"
---
# <span data-ttu-id="949db-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="949db-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="949db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="949db-102">SYNOPSIS</span></span>
<span data-ttu-id="949db-103">Obtém as propriedades de produtividade CosmosDB do banco de dados do MongoDB.</span><span class="sxs-lookup"><span data-stu-id="949db-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="949db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="949db-104">SYNTAX</span></span>

### <span data-ttu-id="949db-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="949db-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949db-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="949db-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="949db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="949db-107">DESCRIPTION</span></span>
<span data-ttu-id="949db-108">O cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** Obtém as propriedades de produtividade do banco de dados do MongoDB.</span><span class="sxs-lookup"><span data-stu-id="949db-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="949db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="949db-109">EXAMPLES</span></span>

### <span data-ttu-id="949db-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="949db-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="949db-111">OS</span><span class="sxs-lookup"><span data-stu-id="949db-111">PARAMETERS</span></span>

### <span data-ttu-id="949db-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="949db-112">-AccountName</span></span>
<span data-ttu-id="949db-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="949db-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="949db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="949db-114">-DefaultProfile</span></span>
<span data-ttu-id="949db-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="949db-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="949db-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="949db-116">-InputObject</span></span>
<span data-ttu-id="949db-117">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="949db-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949db-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="949db-118">-Name</span></span>
<span data-ttu-id="949db-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="949db-119">Database name.</span></span>

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

### <span data-ttu-id="949db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="949db-120">-ResourceGroupName</span></span>
<span data-ttu-id="949db-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="949db-121">Name of resource group.</span></span>

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

### <span data-ttu-id="949db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="949db-122">CommonParameters</span></span>
<span data-ttu-id="949db-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="949db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="949db-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="949db-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="949db-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="949db-125">INPUTS</span></span>

### <span data-ttu-id="949db-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="949db-126">None</span></span>

## <span data-ttu-id="949db-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="949db-127">OUTPUTS</span></span>

### <span data-ttu-id="949db-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="949db-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="949db-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="949db-129">NOTES</span></span>

## <span data-ttu-id="949db-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="949db-130">RELATED LINKS</span></span>
