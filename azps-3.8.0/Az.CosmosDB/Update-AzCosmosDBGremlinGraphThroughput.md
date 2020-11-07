---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942183"
---
# <span data-ttu-id="9249c-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="9249c-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="9249c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9249c-102">SYNOPSIS</span></span>
<span data-ttu-id="9249c-103">Atualiza o valor de produtividade de um gráfico de Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9249c-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="9249c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9249c-104">SYNTAX</span></span>

### <span data-ttu-id="9249c-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9249c-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9249c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9249c-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9249c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9249c-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9249c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9249c-108">EXAMPLES</span></span>

### <span data-ttu-id="9249c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9249c-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="9249c-110">OS</span><span class="sxs-lookup"><span data-stu-id="9249c-110">PARAMETERS</span></span>

### <span data-ttu-id="9249c-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9249c-111">-AccountName</span></span>
<span data-ttu-id="9249c-112">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="9249c-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9249c-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9249c-113">-Confirm</span></span>
<span data-ttu-id="9249c-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9249c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9249c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9249c-115">-DatabaseName</span></span>
<span data-ttu-id="9249c-116">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9249c-116">Database name.</span></span>

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

### <span data-ttu-id="9249c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9249c-117">-DefaultProfile</span></span>
<span data-ttu-id="9249c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9249c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9249c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9249c-119">-InputObject</span></span>
<span data-ttu-id="9249c-120">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9249c-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9249c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9249c-121">-Name</span></span>
<span data-ttu-id="9249c-122">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="9249c-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="9249c-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9249c-123">-ParentObject</span></span>
<span data-ttu-id="9249c-124">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9249c-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9249c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9249c-125">-ResourceGroupName</span></span>
<span data-ttu-id="9249c-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9249c-126">Name of resource group.</span></span>

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

### <span data-ttu-id="9249c-127">-Throughput</span><span class="sxs-lookup"><span data-stu-id="9249c-127">-Throughput</span></span>
<span data-ttu-id="9249c-128">O throughput do Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9249c-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="9249c-129">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="9249c-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9249c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9249c-130">-WhatIf</span></span>
<span data-ttu-id="9249c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9249c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9249c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9249c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9249c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9249c-133">CommonParameters</span></span>
<span data-ttu-id="9249c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9249c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9249c-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9249c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9249c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9249c-136">INPUTS</span></span>

### <span data-ttu-id="9249c-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9249c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="9249c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9249c-138">OUTPUTS</span></span>

### <span data-ttu-id="9249c-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9249c-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9249c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9249c-140">NOTES</span></span>

## <span data-ttu-id="9249c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9249c-141">RELATED LINKS</span></span>
