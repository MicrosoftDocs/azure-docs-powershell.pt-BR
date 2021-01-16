---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264393"
---
# <span data-ttu-id="16d0d-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="16d0d-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="16d0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="16d0d-103">Atualiza o valor de produtividade de um gráfico de Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="16d0d-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="16d0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16d0d-104">SYNTAX</span></span>

### <span data-ttu-id="16d0d-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="16d0d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d0d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d0d-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d0d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d0d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16d0d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16d0d-108">DESCRIPTION</span></span>
<span data-ttu-id="16d0d-109">Atualiza o valor de produtividade de um gráfico de Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="16d0d-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="16d0d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16d0d-110">EXAMPLES</span></span>

### <span data-ttu-id="16d0d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16d0d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="16d0d-112">OS</span><span class="sxs-lookup"><span data-stu-id="16d0d-112">PARAMETERS</span></span>

### <span data-ttu-id="16d0d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16d0d-113">-AccountName</span></span>
<span data-ttu-id="16d0d-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="16d0d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="16d0d-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="16d0d-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="16d0d-116">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="16d0d-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d0d-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16d0d-117">-Confirm</span></span>
<span data-ttu-id="16d0d-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16d0d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16d0d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16d0d-119">-DatabaseName</span></span>
<span data-ttu-id="16d0d-120">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="16d0d-120">Database name.</span></span>

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

### <span data-ttu-id="16d0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d0d-121">-DefaultProfile</span></span>
<span data-ttu-id="16d0d-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16d0d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16d0d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16d0d-123">-InputObject</span></span>
<span data-ttu-id="16d0d-124">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="16d0d-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="16d0d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="16d0d-125">-Name</span></span>
<span data-ttu-id="16d0d-126">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="16d0d-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="16d0d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="16d0d-127">-ParentObject</span></span>
<span data-ttu-id="16d0d-128">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="16d0d-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="16d0d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d0d-129">-ResourceGroupName</span></span>
<span data-ttu-id="16d0d-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="16d0d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="16d0d-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="16d0d-131">-Throughput</span></span>
<span data-ttu-id="16d0d-132">O throughput do Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="16d0d-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="16d0d-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="16d0d-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d0d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d0d-134">-WhatIf</span></span>
<span data-ttu-id="16d0d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16d0d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16d0d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16d0d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16d0d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d0d-137">CommonParameters</span></span>
<span data-ttu-id="16d0d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d0d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d0d-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16d0d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d0d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16d0d-140">INPUTS</span></span>

### <span data-ttu-id="16d0d-141">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="16d0d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="16d0d-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16d0d-142">OUTPUTS</span></span>

### <span data-ttu-id="16d0d-143">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="16d0d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="16d0d-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16d0d-144">NOTES</span></span>

## <span data-ttu-id="16d0d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16d0d-145">RELATED LINKS</span></span>
