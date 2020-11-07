---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944439"
---
# <span data-ttu-id="5c0a9-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="5c0a9-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="5c0a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0a9-103">Define a tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="5c0a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c0a9-104">SYNTAX</span></span>

### <span data-ttu-id="5c0a9-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5c0a9-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c0a9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c0a9-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c0a9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c0a9-107">DESCRIPTION</span></span>
<span data-ttu-id="5c0a9-108">O cmdlet **set-AzCosmosDBCassandraTable** define o espaço de keyCosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5c0a9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c0a9-109">EXAMPLES</span></span>

### <span data-ttu-id="5c0a9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c0a9-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="5c0a9-111">Objeto de recurso contém os valores das propriedades _rid, _ts, _etag, DefaultTtl e esquema.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="5c0a9-112">OS</span><span class="sxs-lookup"><span data-stu-id="5c0a9-112">PARAMETERS</span></span>

### <span data-ttu-id="5c0a9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c0a9-113">-AccountName</span></span>
<span data-ttu-id="5c0a9-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5c0a9-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c0a9-115">-Confirm</span></span>
<span data-ttu-id="5c0a9-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c0a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0a9-117">-DefaultProfile</span></span>
<span data-ttu-id="5c0a9-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c0a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c0a9-119">-InputObject</span></span>
<span data-ttu-id="5c0a9-120">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="5c0a9-121">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="5c0a9-121">-KeyspaceName</span></span>
<span data-ttu-id="5c0a9-122">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5c0a9-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c0a9-123">-Name</span></span>
<span data-ttu-id="5c0a9-124">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="5c0a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c0a9-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5c0a9-127">-Esquema</span><span class="sxs-lookup"><span data-stu-id="5c0a9-127">-Schema</span></span>
<span data-ttu-id="5c0a9-128">Objeto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="5c0a9-129">Use New-AzCosmosDBCassandraSchema para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c0a9-130">-Throughput</span><span class="sxs-lookup"><span data-stu-id="5c0a9-130">-Throughput</span></span>
<span data-ttu-id="5c0a9-131">A taxa de transferência do espaço de Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5c0a9-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="5c0a9-132">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-132">Default value is 400.</span></span>

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

### <span data-ttu-id="5c0a9-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5c0a9-133">-TtlInSeconds</span></span>
<span data-ttu-id="5c0a9-134">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="5c0a9-135">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="5c0a9-136">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="5c0a9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c0a9-137">-WhatIf</span></span>
<span data-ttu-id="5c0a9-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c0a9-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c0a9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0a9-140">CommonParameters</span></span>
<span data-ttu-id="5c0a9-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c0a9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0a9-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c0a9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0a9-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c0a9-143">INPUTS</span></span>

### <span data-ttu-id="5c0a9-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="5c0a9-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="5c0a9-145">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5c0a9-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5c0a9-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c0a9-146">OUTPUTS</span></span>

### <span data-ttu-id="5c0a9-147">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="5c0a9-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="5c0a9-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c0a9-148">NOTES</span></span>

## <span data-ttu-id="5c0a9-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c0a9-149">RELATED LINKS</span></span>
