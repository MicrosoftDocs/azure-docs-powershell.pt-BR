---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955711"
---
# <span data-ttu-id="36831-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="36831-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="36831-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36831-102">SYNOPSIS</span></span>
<span data-ttu-id="36831-103">Obtém o banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="36831-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="36831-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36831-104">SYNTAX</span></span>

### <span data-ttu-id="36831-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="36831-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36831-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36831-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36831-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36831-107">DESCRIPTION</span></span>
<span data-ttu-id="36831-108">O cmdlet **Get-AzCosmosDBGremlinDatabase** Obtém o banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="36831-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="36831-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36831-109">EXAMPLES</span></span>

### <span data-ttu-id="36831-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36831-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="36831-111">Objeto de recurso contém _rid, _ts _etag.</span><span class="sxs-lookup"><span data-stu-id="36831-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="36831-112">OS</span><span class="sxs-lookup"><span data-stu-id="36831-112">PARAMETERS</span></span>

### <span data-ttu-id="36831-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36831-113">-AccountName</span></span>
<span data-ttu-id="36831-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="36831-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36831-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36831-115">-DefaultProfile</span></span>
<span data-ttu-id="36831-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36831-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36831-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="36831-117">-Name</span></span>
<span data-ttu-id="36831-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="36831-118">Database name.</span></span>

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

### <span data-ttu-id="36831-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="36831-119">-ParentObject</span></span>
<span data-ttu-id="36831-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="36831-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36831-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36831-121">-ResourceGroupName</span></span>
<span data-ttu-id="36831-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36831-122">Name of resource group.</span></span>

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

### <span data-ttu-id="36831-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36831-123">CommonParameters</span></span>
<span data-ttu-id="36831-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36831-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36831-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36831-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36831-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36831-126">INPUTS</span></span>

### <span data-ttu-id="36831-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="36831-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="36831-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36831-128">OUTPUTS</span></span>

### <span data-ttu-id="36831-129">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="36831-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="36831-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="36831-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="36831-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36831-131">NOTES</span></span>

## <span data-ttu-id="36831-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36831-132">RELATED LINKS</span></span>
