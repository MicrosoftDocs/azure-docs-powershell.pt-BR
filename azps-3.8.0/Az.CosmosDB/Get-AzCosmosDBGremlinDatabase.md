---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944125"
---
# <span data-ttu-id="a146c-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="a146c-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="a146c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a146c-102">SYNOPSIS</span></span>
<span data-ttu-id="a146c-103">Obtém o banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a146c-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="a146c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a146c-104">SYNTAX</span></span>

### <span data-ttu-id="a146c-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a146c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a146c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a146c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a146c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a146c-107">DESCRIPTION</span></span>
<span data-ttu-id="a146c-108">O cmdlet **Get-AzCosmosDBGremlinDatabase** Obtém o banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a146c-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="a146c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a146c-109">EXAMPLES</span></span>

### <span data-ttu-id="a146c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a146c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="a146c-111">Objeto de recurso contém _rid, _ts _etag.</span><span class="sxs-lookup"><span data-stu-id="a146c-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="a146c-112">OS</span><span class="sxs-lookup"><span data-stu-id="a146c-112">PARAMETERS</span></span>

### <span data-ttu-id="a146c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a146c-113">-AccountName</span></span>
<span data-ttu-id="a146c-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="a146c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a146c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a146c-115">-DefaultProfile</span></span>
<span data-ttu-id="a146c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a146c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a146c-117">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="a146c-117">-Detailed</span></span>
<span data-ttu-id="a146c-118">Se fornecido, o cmdlet retornará o banco de dados com o valor de produtividade correspondente.</span><span class="sxs-lookup"><span data-stu-id="a146c-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="a146c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a146c-119">-InputObject</span></span>
<span data-ttu-id="a146c-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a146c-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a146c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a146c-121">-Name</span></span>
<span data-ttu-id="a146c-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a146c-122">Database name.</span></span>

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

### <span data-ttu-id="a146c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a146c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a146c-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a146c-124">Name of resource group.</span></span>

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

### <span data-ttu-id="a146c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a146c-125">CommonParameters</span></span>
<span data-ttu-id="a146c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a146c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a146c-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a146c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a146c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a146c-128">INPUTS</span></span>

### <span data-ttu-id="a146c-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a146c-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a146c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a146c-130">OUTPUTS</span></span>

### <span data-ttu-id="a146c-131">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a146c-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="a146c-132">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a146c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a146c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a146c-133">NOTES</span></span>

## <span data-ttu-id="a146c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a146c-134">RELATED LINKS</span></span>
