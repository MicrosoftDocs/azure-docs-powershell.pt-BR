---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 4a9a5595345b44eaf3a3b44d9d9ba1d8895a6376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888567"
---
# <span data-ttu-id="f68d8-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="f68d8-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="f68d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f68d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f68d8-103">Atualiza o Espaço-Chave de Cassandra de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f68d8-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="f68d8-104">Executa uma operação de patch do lado do cliente lendo o Keyspace existente.</span><span class="sxs-lookup"><span data-stu-id="f68d8-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="f68d8-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f68d8-105">SYNTAX</span></span>

### <span data-ttu-id="f68d8-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f68d8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f68d8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f68d8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f68d8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f68d8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f68d8-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f68d8-109">DESCRIPTION</span></span>
<span data-ttu-id="f68d8-110">Atualiza o Espaço-Chave de Cassandra de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f68d8-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="f68d8-111">Executa uma operação de patch do lado do cliente lendo o Keyspace existente.</span><span class="sxs-lookup"><span data-stu-id="f68d8-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="f68d8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f68d8-112">EXAMPLES</span></span>

### <span data-ttu-id="f68d8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f68d8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="f68d8-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f68d8-114">PARAMETERS</span></span>

### <span data-ttu-id="f68d8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f68d8-115">-AccountName</span></span>
<span data-ttu-id="f68d8-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="f68d8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f68d8-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f68d8-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f68d8-118">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="f68d8-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f68d8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f68d8-119">-Confirm</span></span>
<span data-ttu-id="f68d8-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f68d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f68d8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f68d8-121">-DefaultProfile</span></span>
<span data-ttu-id="f68d8-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f68d8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f68d8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f68d8-123">-InputObject</span></span>
<span data-ttu-id="f68d8-124">Objeto Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f68d8-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="f68d8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f68d8-125">-Name</span></span>
<span data-ttu-id="f68d8-126">Nome do Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="f68d8-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f68d8-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f68d8-127">-ParentObject</span></span>
<span data-ttu-id="f68d8-128">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f68d8-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f68d8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f68d8-129">-ResourceGroupName</span></span>
<span data-ttu-id="f68d8-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f68d8-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f68d8-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f68d8-131">-Throughput</span></span>
<span data-ttu-id="f68d8-132">A produtividade de Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f68d8-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="f68d8-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="f68d8-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f68d8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f68d8-134">-WhatIf</span></span>
<span data-ttu-id="f68d8-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f68d8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f68d8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f68d8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f68d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68d8-137">CommonParameters</span></span>
<span data-ttu-id="f68d8-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f68d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68d8-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f68d8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68d8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f68d8-140">INPUTS</span></span>

### <span data-ttu-id="f68d8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f68d8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="f68d8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f68d8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="f68d8-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f68d8-143">OUTPUTS</span></span>

### <span data-ttu-id="f68d8-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f68d8-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="f68d8-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f68d8-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f68d8-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="f68d8-146">NOTES</span></span>

## <span data-ttu-id="f68d8-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f68d8-147">RELATED LINKS</span></span>
