---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112372"
---
# <span data-ttu-id="4ec3e-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="4ec3e-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="4ec3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ec3e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec3e-103">Atualiza o espaço de CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="4ec3e-104">Executa uma operação de correção de cliente ao ler o espaço de recurso existente.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="4ec3e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ec3e-105">SYNTAX</span></span>

### <span data-ttu-id="4ec3e-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ec3e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec3e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ec3e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ec3e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ec3e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ec3e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ec3e-109">DESCRIPTION</span></span>
<span data-ttu-id="4ec3e-110">Atualiza o espaço de CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="4ec3e-111">Executa uma operação de correção de cliente ao ler o espaço de recurso existente.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="4ec3e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ec3e-112">EXAMPLES</span></span>

### <span data-ttu-id="4ec3e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ec3e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="4ec3e-114">OS</span><span class="sxs-lookup"><span data-stu-id="4ec3e-114">PARAMETERS</span></span>

### <span data-ttu-id="4ec3e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4ec3e-115">-AccountName</span></span>
<span data-ttu-id="4ec3e-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4ec3e-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4ec3e-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4ec3e-118">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="4ec3e-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ec3e-119">-Confirm</span></span>
<span data-ttu-id="4ec3e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec3e-121">-DefaultProfile</span></span>
<span data-ttu-id="4ec3e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ec3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ec3e-123">-InputObject</span></span>
<span data-ttu-id="4ec3e-124">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="4ec3e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ec3e-125">-Name</span></span>
<span data-ttu-id="4ec3e-126">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4ec3e-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4ec3e-127">-ParentObject</span></span>
<span data-ttu-id="4ec3e-128">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4ec3e-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4ec3e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec3e-129">-ResourceGroupName</span></span>
<span data-ttu-id="4ec3e-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="4ec3e-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="4ec3e-131">-Throughput</span></span>
<span data-ttu-id="4ec3e-132">A taxa de transferência do espaço de Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="4ec3e-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="4ec3e-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-133">Default value is 400.</span></span>

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

### <span data-ttu-id="4ec3e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec3e-134">-WhatIf</span></span>
<span data-ttu-id="4ec3e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec3e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec3e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec3e-137">CommonParameters</span></span>
<span data-ttu-id="4ec3e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ec3e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec3e-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ec3e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec3e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ec3e-140">INPUTS</span></span>

### <span data-ttu-id="4ec3e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4ec3e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="4ec3e-142">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4ec3e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="4ec3e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ec3e-143">OUTPUTS</span></span>

### <span data-ttu-id="4ec3e-144">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4ec3e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="4ec3e-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="4ec3e-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="4ec3e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ec3e-146">NOTES</span></span>

## <span data-ttu-id="4ec3e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ec3e-147">RELATED LINKS</span></span>
