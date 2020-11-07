---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: f1cb4a45a68758dc1209b4e30d352def8e348e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944106"
---
# <span data-ttu-id="406dc-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="406dc-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="406dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="406dc-102">SYNOPSIS</span></span>
<span data-ttu-id="406dc-103">Obtém o banco de dados do CosmosDB MongoDB</span><span class="sxs-lookup"><span data-stu-id="406dc-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="406dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="406dc-104">SYNTAX</span></span>

### <span data-ttu-id="406dc-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="406dc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="406dc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="406dc-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="406dc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="406dc-107">DESCRIPTION</span></span>
<span data-ttu-id="406dc-108">O cmdlet **Get-AzCosmosDBMongoDBDatabase** Obtém o banco de dados do MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="406dc-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="406dc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="406dc-109">EXAMPLES</span></span>

### <span data-ttu-id="406dc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="406dc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="406dc-111">Objeto de recurso contém propriedades _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="406dc-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="406dc-112">OS</span><span class="sxs-lookup"><span data-stu-id="406dc-112">PARAMETERS</span></span>

### <span data-ttu-id="406dc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="406dc-113">-AccountName</span></span>
<span data-ttu-id="406dc-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="406dc-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="406dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406dc-115">-DefaultProfile</span></span>
<span data-ttu-id="406dc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="406dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406dc-117">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="406dc-117">-Detailed</span></span>
<span data-ttu-id="406dc-118">Se fornecido, o cmdlet retornará o banco de dados com o valor de produtividade correspondente.</span><span class="sxs-lookup"><span data-stu-id="406dc-118">If provided then, the cmdlet returns the database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="406dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="406dc-119">-InputObject</span></span>
<span data-ttu-id="406dc-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="406dc-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="406dc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="406dc-121">-Name</span></span>
<span data-ttu-id="406dc-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="406dc-122">Database name.</span></span>

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

### <span data-ttu-id="406dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="406dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="406dc-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="406dc-124">Name of resource group.</span></span>

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

### <span data-ttu-id="406dc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406dc-125">CommonParameters</span></span>
<span data-ttu-id="406dc-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="406dc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406dc-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="406dc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406dc-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="406dc-128">INPUTS</span></span>

### <span data-ttu-id="406dc-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="406dc-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="406dc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="406dc-130">OUTPUTS</span></span>

### <span data-ttu-id="406dc-131">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="406dc-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="406dc-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="406dc-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="406dc-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="406dc-133">NOTES</span></span>

## <span data-ttu-id="406dc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="406dc-134">RELATED LINKS</span></span>
