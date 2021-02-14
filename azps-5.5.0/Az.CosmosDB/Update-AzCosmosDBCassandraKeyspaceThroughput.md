---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111021"
---
# <span data-ttu-id="a3385-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="a3385-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="a3385-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3385-102">SYNOPSIS</span></span>
<span data-ttu-id="a3385-103">Atualiza o valor de produtividade de um Espaço de Keyspace do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a3385-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="a3385-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3385-104">SYNTAX</span></span>

### <span data-ttu-id="a3385-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3385-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3385-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3385-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3385-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3385-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3385-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3385-108">DESCRIPTION</span></span>
<span data-ttu-id="a3385-109">Atualiza o valor de produtividade de um Espaço de Keyspace do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a3385-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="a3385-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3385-110">EXAMPLES</span></span>

### <span data-ttu-id="a3385-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3385-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="a3385-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3385-112">PARAMETERS</span></span>

### <span data-ttu-id="a3385-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="a3385-113">-AccountName</span></span>
<span data-ttu-id="a3385-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="a3385-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a3385-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="a3385-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a3385-116">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="a3385-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a3385-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a3385-117">-Confirm</span></span>
<span data-ttu-id="a3385-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3385-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3385-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3385-119">-DefaultProfile</span></span>
<span data-ttu-id="a3385-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3385-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3385-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3385-121">-InputObject</span></span>
<span data-ttu-id="a3385-122">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="a3385-122">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3385-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3385-123">-Name</span></span>
<span data-ttu-id="a3385-124">Nome do Espaço de Teclas Descaroçador.</span><span class="sxs-lookup"><span data-stu-id="a3385-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="a3385-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a3385-125">-ParentObject</span></span>
<span data-ttu-id="a3385-126">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="a3385-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a3385-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3385-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3385-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3385-128">Name of resource group.</span></span>

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

### <span data-ttu-id="a3385-129">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="a3385-129">-Throughput</span></span>
<span data-ttu-id="a3385-130">A produtividade de Guida Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="a3385-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="a3385-131">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="a3385-131">Default value is 400.</span></span>

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

### <span data-ttu-id="a3385-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3385-132">-WhatIf</span></span>
<span data-ttu-id="a3385-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a3385-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3385-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3385-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3385-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3385-135">CommonParameters</span></span>
<span data-ttu-id="a3385-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3385-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3385-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3385-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3385-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="a3385-138">INPUTS</span></span>

### <span data-ttu-id="a3385-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a3385-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a3385-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="a3385-140">OUTPUTS</span></span>

### <span data-ttu-id="a3385-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a3385-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a3385-142">Notas</span><span class="sxs-lookup"><span data-stu-id="a3385-142">NOTES</span></span>

## <span data-ttu-id="a3385-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3385-143">RELATED LINKS</span></span>
