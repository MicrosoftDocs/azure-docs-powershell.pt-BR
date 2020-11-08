---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112876"
---
# <span data-ttu-id="71d9f-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="71d9f-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="71d9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="71d9f-103">Obtém o banco de dados do CosmosDB MongoDB</span><span class="sxs-lookup"><span data-stu-id="71d9f-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="71d9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71d9f-104">SYNTAX</span></span>

### <span data-ttu-id="71d9f-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="71d9f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71d9f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71d9f-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71d9f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71d9f-107">DESCRIPTION</span></span>
<span data-ttu-id="71d9f-108">O cmdlet **Get-AzCosmosDBMongoDBDatabase** Obtém o banco de dados do MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="71d9f-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="71d9f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71d9f-109">EXAMPLES</span></span>

### <span data-ttu-id="71d9f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71d9f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="71d9f-111">Objeto de recurso contém propriedades _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="71d9f-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="71d9f-112">OS</span><span class="sxs-lookup"><span data-stu-id="71d9f-112">PARAMETERS</span></span>

### <span data-ttu-id="71d9f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="71d9f-113">-AccountName</span></span>
<span data-ttu-id="71d9f-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="71d9f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="71d9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d9f-115">-DefaultProfile</span></span>
<span data-ttu-id="71d9f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71d9f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71d9f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="71d9f-117">-Name</span></span>
<span data-ttu-id="71d9f-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71d9f-118">Database name.</span></span>

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

### <span data-ttu-id="71d9f-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="71d9f-119">-ParentObject</span></span>
<span data-ttu-id="71d9f-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="71d9f-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71d9f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d9f-121">-ResourceGroupName</span></span>
<span data-ttu-id="71d9f-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71d9f-122">Name of resource group.</span></span>

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

### <span data-ttu-id="71d9f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d9f-123">CommonParameters</span></span>
<span data-ttu-id="71d9f-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d9f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d9f-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71d9f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d9f-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71d9f-126">INPUTS</span></span>

### <span data-ttu-id="71d9f-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="71d9f-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="71d9f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71d9f-128">OUTPUTS</span></span>

### <span data-ttu-id="71d9f-129">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="71d9f-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="71d9f-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="71d9f-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="71d9f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71d9f-131">NOTES</span></span>

## <span data-ttu-id="71d9f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71d9f-132">RELATED LINKS</span></span>
