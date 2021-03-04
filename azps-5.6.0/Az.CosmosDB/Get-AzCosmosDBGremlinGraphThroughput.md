---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: f5357e23b8a4e4ec5c613dc7a6b1b0f53e5bac3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889338"
---
# <span data-ttu-id="09a04-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="09a04-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="09a04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09a04-102">SYNOPSIS</span></span>
<span data-ttu-id="09a04-103">Obtém a produtividade de um Gráfico de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="09a04-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="09a04-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09a04-104">SYNTAX</span></span>

### <span data-ttu-id="09a04-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09a04-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a04-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09a04-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09a04-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09a04-107">DESCRIPTION</span></span>
<span data-ttu-id="09a04-108">O cmdlet **Get-AzCosmosDBGremlinGraphThroughput** obtém a produtividade de um Gráfico de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="09a04-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="09a04-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09a04-109">EXAMPLES</span></span>

### <span data-ttu-id="09a04-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="09a04-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="09a04-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09a04-111">PARAMETERS</span></span>

### <span data-ttu-id="09a04-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09a04-112">-AccountName</span></span>
<span data-ttu-id="09a04-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="09a04-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09a04-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09a04-114">-Confirm</span></span>
<span data-ttu-id="09a04-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09a04-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09a04-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09a04-116">-DatabaseName</span></span>
<span data-ttu-id="09a04-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="09a04-117">Database name.</span></span>

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

### <span data-ttu-id="09a04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a04-118">-DefaultProfile</span></span>
<span data-ttu-id="09a04-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09a04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09a04-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09a04-120">-InputObject</span></span>
<span data-ttu-id="09a04-121">Objeto Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="09a04-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a04-122">-Name</span><span class="sxs-lookup"><span data-stu-id="09a04-122">-Name</span></span>
<span data-ttu-id="09a04-123">Nome do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="09a04-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="09a04-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a04-124">-ResourceGroupName</span></span>
<span data-ttu-id="09a04-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09a04-125">Name of resource group.</span></span>

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

### <span data-ttu-id="09a04-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a04-126">-WhatIf</span></span>
<span data-ttu-id="09a04-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09a04-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09a04-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09a04-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09a04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a04-129">CommonParameters</span></span>
<span data-ttu-id="09a04-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a04-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09a04-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a04-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09a04-132">INPUTS</span></span>

### <span data-ttu-id="09a04-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="09a04-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="09a04-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09a04-134">OUTPUTS</span></span>

### <span data-ttu-id="09a04-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="09a04-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="09a04-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="09a04-136">NOTES</span></span>

## <span data-ttu-id="09a04-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09a04-137">RELATED LINKS</span></span>
