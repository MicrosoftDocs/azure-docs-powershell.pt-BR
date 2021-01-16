---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259576"
---
# <span data-ttu-id="dced4-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="dced4-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="dced4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dced4-102">SYNOPSIS</span></span>
<span data-ttu-id="dced4-103">Obtém a taxa de transferência de um banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="dced4-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="dced4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dced4-104">SYNTAX</span></span>

### <span data-ttu-id="dced4-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dced4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dced4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dced4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dced4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dced4-107">DESCRIPTION</span></span>
<span data-ttu-id="dced4-108">O cmdlet **Get-AzCosmosDBGremlinDatabaseThroughput** Obtém a taxa de transferência de um banco de dados do Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="dced4-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="dced4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dced4-109">EXAMPLES</span></span>

### <span data-ttu-id="dced4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dced4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="dced4-111">OS</span><span class="sxs-lookup"><span data-stu-id="dced4-111">PARAMETERS</span></span>

### <span data-ttu-id="dced4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dced4-112">-AccountName</span></span>
<span data-ttu-id="dced4-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="dced4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dced4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dced4-114">-DefaultProfile</span></span>
<span data-ttu-id="dced4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dced4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dced4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dced4-116">-InputObject</span></span>
<span data-ttu-id="dced4-117">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="dced4-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dced4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dced4-118">-Name</span></span>
<span data-ttu-id="dced4-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dced4-119">Database name.</span></span>

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

### <span data-ttu-id="dced4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dced4-120">-ResourceGroupName</span></span>
<span data-ttu-id="dced4-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dced4-121">Name of resource group.</span></span>

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

### <span data-ttu-id="dced4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dced4-122">CommonParameters</span></span>
<span data-ttu-id="dced4-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dced4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dced4-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dced4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dced4-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dced4-125">INPUTS</span></span>

### <span data-ttu-id="dced4-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dced4-126">None</span></span>

## <span data-ttu-id="dced4-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dced4-127">OUTPUTS</span></span>

### <span data-ttu-id="dced4-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dced4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dced4-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dced4-129">NOTES</span></span>

## <span data-ttu-id="dced4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dced4-130">RELATED LINKS</span></span>
