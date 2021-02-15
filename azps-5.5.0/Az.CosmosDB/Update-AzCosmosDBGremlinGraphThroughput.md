---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112030"
---
# <span data-ttu-id="5515e-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="5515e-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="5515e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5515e-102">SYNOPSIS</span></span>
<span data-ttu-id="5515e-103">Atualiza o valor de produtividade de um Graph Desalinhado Demlin.</span><span class="sxs-lookup"><span data-stu-id="5515e-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5515e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5515e-104">SYNTAX</span></span>

### <span data-ttu-id="5515e-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5515e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5515e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5515e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5515e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5515e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5515e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5515e-108">DESCRIPTION</span></span>
<span data-ttu-id="5515e-109">Atualiza o valor de produtividade de um Graph Desalinhado Demlin.</span><span class="sxs-lookup"><span data-stu-id="5515e-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5515e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5515e-110">EXAMPLES</span></span>

### <span data-ttu-id="5515e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5515e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="5515e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5515e-112">PARAMETERS</span></span>

### <span data-ttu-id="5515e-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="5515e-113">-AccountName</span></span>
<span data-ttu-id="5515e-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="5515e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5515e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5515e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5515e-116">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="5515e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5515e-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5515e-117">-Confirm</span></span>
<span data-ttu-id="5515e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5515e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5515e-119">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="5515e-119">-DatabaseName</span></span>
<span data-ttu-id="5515e-120">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5515e-120">Database name.</span></span>

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

### <span data-ttu-id="5515e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5515e-121">-DefaultProfile</span></span>
<span data-ttu-id="5515e-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5515e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5515e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5515e-123">-InputObject</span></span>
<span data-ttu-id="5515e-124">Objeto de Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5515e-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5515e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5515e-125">-Name</span></span>
<span data-ttu-id="5515e-126">Nome do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5515e-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="5515e-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5515e-127">-ParentObject</span></span>
<span data-ttu-id="5515e-128">Objeto de Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5515e-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5515e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5515e-129">-ResourceGroupName</span></span>
<span data-ttu-id="5515e-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5515e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5515e-131">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="5515e-131">-Throughput</span></span>
<span data-ttu-id="5515e-132">A produtividade do Gremlin Graph (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5515e-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="5515e-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="5515e-133">Default value is 400.</span></span>

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

### <span data-ttu-id="5515e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5515e-134">-WhatIf</span></span>
<span data-ttu-id="5515e-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5515e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5515e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5515e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5515e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5515e-137">CommonParameters</span></span>
<span data-ttu-id="5515e-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5515e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5515e-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5515e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5515e-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="5515e-140">INPUTS</span></span>

### <span data-ttu-id="5515e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5515e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5515e-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="5515e-142">OUTPUTS</span></span>

### <span data-ttu-id="5515e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5515e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5515e-144">Notas</span><span class="sxs-lookup"><span data-stu-id="5515e-144">NOTES</span></span>

## <span data-ttu-id="5515e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5515e-145">RELATED LINKS</span></span>
