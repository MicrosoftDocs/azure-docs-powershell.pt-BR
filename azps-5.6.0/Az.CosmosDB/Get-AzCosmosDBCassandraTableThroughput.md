---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 7693d507874dc5ebc4aa7b9c720c3efbe2963c05
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889346"
---
# <span data-ttu-id="0b066-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="0b066-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="0b066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b066-102">SYNOPSIS</span></span>
<span data-ttu-id="0b066-103">Obtém o valor de produtividade da Tabela de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0b066-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="0b066-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0b066-104">SYNTAX</span></span>

### <span data-ttu-id="0b066-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b066-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b066-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b066-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b066-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b066-107">DESCRIPTION</span></span>
<span data-ttu-id="0b066-108">O cmdlet **Get-AzCosmosDBCassandraTableThroughput** obtém o objeto de transferência correspondente a um determinado Keyspace.</span><span class="sxs-lookup"><span data-stu-id="0b066-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="0b066-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b066-109">EXAMPLES</span></span>

### <span data-ttu-id="0b066-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b066-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="0b066-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0b066-111">PARAMETERS</span></span>

### <span data-ttu-id="0b066-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b066-112">-AccountName</span></span>
<span data-ttu-id="0b066-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="0b066-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0b066-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b066-114">-Confirm</span></span>
<span data-ttu-id="0b066-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b066-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b066-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b066-116">-DefaultProfile</span></span>
<span data-ttu-id="0b066-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b066-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b066-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b066-118">-InputObject</span></span>
<span data-ttu-id="0b066-119">Objeto Table de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0b066-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="0b066-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="0b066-120">-KeyspaceName</span></span>
<span data-ttu-id="0b066-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0b066-121">Database name.</span></span>

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

### <span data-ttu-id="0b066-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0b066-122">-Name</span></span>
<span data-ttu-id="0b066-123">Nome da tabela de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0b066-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="0b066-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b066-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b066-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b066-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0b066-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b066-126">-WhatIf</span></span>
<span data-ttu-id="0b066-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b066-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b066-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b066-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b066-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b066-129">CommonParameters</span></span>
<span data-ttu-id="0b066-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b066-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b066-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b066-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b066-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b066-132">INPUTS</span></span>

### <span data-ttu-id="0b066-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0b066-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="0b066-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0b066-134">OUTPUTS</span></span>

### <span data-ttu-id="0b066-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0b066-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0b066-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="0b066-136">NOTES</span></span>

## <span data-ttu-id="0b066-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b066-137">RELATED LINKS</span></span>
