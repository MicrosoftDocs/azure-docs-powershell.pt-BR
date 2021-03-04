---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 21dd30bd60e9b26fc306ed99b31cd3c52d9fdf8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888554"
---
# <span data-ttu-id="e4c74-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="e4c74-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="e4c74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c74-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c74-103">Atualiza o valor de produtividade de um Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e4c74-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e4c74-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4c74-104">SYNTAX</span></span>

### <span data-ttu-id="e4c74-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4c74-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4c74-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4c74-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4c74-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4c74-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c74-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4c74-108">DESCRIPTION</span></span>
<span data-ttu-id="e4c74-109">Atualiza o valor de produtividade de um Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e4c74-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e4c74-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4c74-110">EXAMPLES</span></span>

### <span data-ttu-id="e4c74-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4c74-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="e4c74-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4c74-112">PARAMETERS</span></span>

### <span data-ttu-id="e4c74-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e4c74-113">-AccountName</span></span>
<span data-ttu-id="e4c74-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="e4c74-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e4c74-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e4c74-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e4c74-116">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="e4c74-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e4c74-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4c74-117">-Confirm</span></span>
<span data-ttu-id="e4c74-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c74-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c74-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c74-119">-DefaultProfile</span></span>
<span data-ttu-id="e4c74-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4c74-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c74-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4c74-121">-InputObject</span></span>
<span data-ttu-id="e4c74-122">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e4c74-122">CosmosDB Account object</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4c74-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e4c74-123">-Name</span></span>
<span data-ttu-id="e4c74-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e4c74-124">Database name.</span></span>

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

### <span data-ttu-id="e4c74-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e4c74-125">-ParentObject</span></span>
<span data-ttu-id="e4c74-126">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e4c74-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e4c74-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c74-127">-ResourceGroupName</span></span>
<span data-ttu-id="e4c74-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4c74-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e4c74-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e4c74-129">-Throughput</span></span>
<span data-ttu-id="e4c74-130">A produtividade do Banco de Dados de Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e4c74-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="e4c74-131">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="e4c74-131">Default value is 400.</span></span>

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

### <span data-ttu-id="e4c74-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c74-132">-WhatIf</span></span>
<span data-ttu-id="e4c74-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4c74-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c74-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4c74-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c74-135">CommonParameters</span></span>
<span data-ttu-id="e4c74-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c74-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4c74-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c74-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4c74-138">INPUTS</span></span>

### <span data-ttu-id="e4c74-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e4c74-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e4c74-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4c74-140">OUTPUTS</span></span>

### <span data-ttu-id="e4c74-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e4c74-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e4c74-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4c74-142">NOTES</span></span>

## <span data-ttu-id="e4c74-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4c74-143">RELATED LINKS</span></span>
