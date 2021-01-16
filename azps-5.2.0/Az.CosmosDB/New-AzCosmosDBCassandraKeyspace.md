---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263027"
---
# <span data-ttu-id="df289-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="df289-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="df289-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df289-102">SYNOPSIS</span></span>
<span data-ttu-id="df289-103">Cria um novo espaço de CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="df289-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="df289-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df289-104">SYNTAX</span></span>

### <span data-ttu-id="df289-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="df289-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df289-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df289-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df289-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df289-107">DESCRIPTION</span></span>
<span data-ttu-id="df289-108">Cria um novo espaço de CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="df289-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="df289-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df289-109">EXAMPLES</span></span>

### <span data-ttu-id="df289-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df289-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="df289-111">OS</span><span class="sxs-lookup"><span data-stu-id="df289-111">PARAMETERS</span></span>

### <span data-ttu-id="df289-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df289-112">-AccountName</span></span>
<span data-ttu-id="df289-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="df289-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="df289-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="df289-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="df289-115">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="df289-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="df289-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df289-116">-Confirm</span></span>
<span data-ttu-id="df289-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df289-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df289-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df289-118">-DefaultProfile</span></span>
<span data-ttu-id="df289-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df289-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df289-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="df289-120">-Name</span></span>
<span data-ttu-id="df289-121">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="df289-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="df289-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="df289-122">-ParentObject</span></span>
<span data-ttu-id="df289-123">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="df289-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="df289-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df289-124">-ResourceGroupName</span></span>
<span data-ttu-id="df289-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df289-125">Name of resource group.</span></span>

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

### <span data-ttu-id="df289-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="df289-126">-Throughput</span></span>
<span data-ttu-id="df289-127">A taxa de transferência do espaço de Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="df289-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="df289-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="df289-128">Default value is 400.</span></span>

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

### <span data-ttu-id="df289-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df289-129">-WhatIf</span></span>
<span data-ttu-id="df289-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df289-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df289-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df289-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df289-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df289-132">CommonParameters</span></span>
<span data-ttu-id="df289-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df289-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df289-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df289-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df289-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df289-135">INPUTS</span></span>

### <span data-ttu-id="df289-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="df289-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="df289-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df289-137">OUTPUTS</span></span>

### <span data-ttu-id="df289-138">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="df289-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="df289-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="df289-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="df289-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df289-140">NOTES</span></span>

## <span data-ttu-id="df289-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df289-141">RELATED LINKS</span></span>
