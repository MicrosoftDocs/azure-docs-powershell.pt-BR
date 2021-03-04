---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 9e06e6eaaea72b0fab9b3333291b29bdc09469d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887223"
---
# <span data-ttu-id="755cf-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="755cf-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="755cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755cf-102">SYNOPSIS</span></span>
<span data-ttu-id="755cf-103">Cria um novo Espaço-Chave de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="755cf-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="755cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="755cf-104">SYNTAX</span></span>

### <span data-ttu-id="755cf-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="755cf-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="755cf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="755cf-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="755cf-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="755cf-107">DESCRIPTION</span></span>
<span data-ttu-id="755cf-108">Cria um novo Espaço-Chave de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="755cf-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="755cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="755cf-109">EXAMPLES</span></span>

### <span data-ttu-id="755cf-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="755cf-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="755cf-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="755cf-111">PARAMETERS</span></span>

### <span data-ttu-id="755cf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="755cf-112">-AccountName</span></span>
<span data-ttu-id="755cf-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="755cf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="755cf-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="755cf-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="755cf-115">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="755cf-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="755cf-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="755cf-116">-Confirm</span></span>
<span data-ttu-id="755cf-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="755cf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755cf-118">-DefaultProfile</span></span>
<span data-ttu-id="755cf-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="755cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755cf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="755cf-120">-Name</span></span>
<span data-ttu-id="755cf-121">Nome do Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="755cf-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="755cf-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="755cf-122">-ParentObject</span></span>
<span data-ttu-id="755cf-123">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="755cf-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="755cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="755cf-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="755cf-125">Name of resource group.</span></span>

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

### <span data-ttu-id="755cf-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="755cf-126">-Throughput</span></span>
<span data-ttu-id="755cf-127">A produtividade de Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="755cf-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="755cf-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="755cf-128">Default value is 400.</span></span>

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

### <span data-ttu-id="755cf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755cf-129">-WhatIf</span></span>
<span data-ttu-id="755cf-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="755cf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755cf-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="755cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755cf-132">CommonParameters</span></span>
<span data-ttu-id="755cf-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755cf-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="755cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755cf-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="755cf-135">INPUTS</span></span>

### <span data-ttu-id="755cf-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="755cf-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="755cf-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="755cf-137">OUTPUTS</span></span>

### <span data-ttu-id="755cf-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="755cf-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="755cf-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="755cf-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="755cf-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="755cf-140">NOTES</span></span>

## <span data-ttu-id="755cf-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="755cf-141">RELATED LINKS</span></span>
