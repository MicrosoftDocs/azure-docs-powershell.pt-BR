---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112041"
---
# <span data-ttu-id="13931-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="13931-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="13931-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13931-102">SYNOPSIS</span></span>
<span data-ttu-id="13931-103">Atualiza o valor de produtividade de uma Tabela Desarmável.</span><span class="sxs-lookup"><span data-stu-id="13931-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="13931-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13931-104">SYNTAX</span></span>

### <span data-ttu-id="13931-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="13931-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13931-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13931-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13931-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13931-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13931-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="13931-108">DESCRIPTION</span></span>
<span data-ttu-id="13931-109">Atualiza o valor de produtividade de uma Tabela Desarmável.</span><span class="sxs-lookup"><span data-stu-id="13931-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="13931-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13931-110">EXAMPLES</span></span>

### <span data-ttu-id="13931-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13931-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="13931-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13931-112">PARAMETERS</span></span>

### <span data-ttu-id="13931-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="13931-113">-AccountName</span></span>
<span data-ttu-id="13931-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="13931-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="13931-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="13931-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="13931-116">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="13931-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="13931-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="13931-117">-Confirm</span></span>
<span data-ttu-id="13931-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13931-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13931-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13931-119">-DefaultProfile</span></span>
<span data-ttu-id="13931-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13931-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13931-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13931-121">-InputObject</span></span>
<span data-ttu-id="13931-122">Objeto Desa Keyspace.</span><span class="sxs-lookup"><span data-stu-id="13931-122">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13931-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="13931-123">-KeyspaceName</span></span>
<span data-ttu-id="13931-124">Nome do Espaço de Teclas Descaroçador.</span><span class="sxs-lookup"><span data-stu-id="13931-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="13931-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="13931-125">-Name</span></span>
<span data-ttu-id="13931-126">Nome da tabela Desarmá.</span><span class="sxs-lookup"><span data-stu-id="13931-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="13931-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="13931-127">-ParentObject</span></span>
<span data-ttu-id="13931-128">Objeto Desa Keyspace.</span><span class="sxs-lookup"><span data-stu-id="13931-128">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13931-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13931-129">-ResourceGroupName</span></span>
<span data-ttu-id="13931-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13931-130">Name of resource group.</span></span>

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

### <span data-ttu-id="13931-131">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="13931-131">-Throughput</span></span>
<span data-ttu-id="13931-132">A produtividade de Guida Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="13931-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="13931-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="13931-133">Default value is 400.</span></span>

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

### <span data-ttu-id="13931-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13931-134">-WhatIf</span></span>
<span data-ttu-id="13931-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="13931-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13931-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13931-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13931-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13931-137">CommonParameters</span></span>
<span data-ttu-id="13931-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13931-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13931-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13931-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13931-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="13931-140">INPUTS</span></span>

### <span data-ttu-id="13931-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="13931-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="13931-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="13931-142">OUTPUTS</span></span>

### <span data-ttu-id="13931-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="13931-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="13931-144">Notas</span><span class="sxs-lookup"><span data-stu-id="13931-144">NOTES</span></span>

## <span data-ttu-id="13931-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13931-145">RELATED LINKS</span></span>
