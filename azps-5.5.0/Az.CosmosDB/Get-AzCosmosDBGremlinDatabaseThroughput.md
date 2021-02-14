---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116476"
---
# <span data-ttu-id="11782-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="11782-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="11782-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11782-102">SYNOPSIS</span></span>
<span data-ttu-id="11782-103">Obtém a produtividade de um Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="11782-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="11782-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11782-104">SYNTAX</span></span>

### <span data-ttu-id="11782-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11782-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11782-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11782-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11782-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="11782-107">DESCRIPTION</span></span>
<span data-ttu-id="11782-108">O cmdlet **Get-AzCosmosDBGremlinDatabaseThroughput** obtém a produtividade de um Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="11782-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="11782-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11782-109">EXAMPLES</span></span>

### <span data-ttu-id="11782-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11782-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="11782-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11782-111">PARAMETERS</span></span>

### <span data-ttu-id="11782-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="11782-112">-AccountName</span></span>
<span data-ttu-id="11782-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="11782-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="11782-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11782-114">-DefaultProfile</span></span>
<span data-ttu-id="11782-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11782-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11782-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11782-116">-InputObject</span></span>
<span data-ttu-id="11782-117">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="11782-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="11782-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="11782-118">-Name</span></span>
<span data-ttu-id="11782-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="11782-119">Database name.</span></span>

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

### <span data-ttu-id="11782-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11782-120">-ResourceGroupName</span></span>
<span data-ttu-id="11782-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11782-121">Name of resource group.</span></span>

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

### <span data-ttu-id="11782-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11782-122">CommonParameters</span></span>
<span data-ttu-id="11782-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11782-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11782-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11782-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11782-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="11782-125">INPUTS</span></span>

### <span data-ttu-id="11782-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="11782-126">None</span></span>

## <span data-ttu-id="11782-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="11782-127">OUTPUTS</span></span>

### <span data-ttu-id="11782-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="11782-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="11782-129">Notas</span><span class="sxs-lookup"><span data-stu-id="11782-129">NOTES</span></span>

## <span data-ttu-id="11782-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11782-130">RELATED LINKS</span></span>
