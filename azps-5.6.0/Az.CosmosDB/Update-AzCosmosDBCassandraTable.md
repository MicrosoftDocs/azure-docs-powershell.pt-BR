---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 3f41c44c6abffaf5147ffba17fe3ec84561315b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888564"
---
# <span data-ttu-id="15996-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="15996-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="15996-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15996-102">SYNOPSIS</span></span>
<span data-ttu-id="15996-103">Atualiza a Tabela de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="15996-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="15996-104">Executa uma operação de patch do lado do cliente lendo a Tabela existente.</span><span class="sxs-lookup"><span data-stu-id="15996-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="15996-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="15996-105">SYNTAX</span></span>

### <span data-ttu-id="15996-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="15996-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15996-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15996-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15996-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15996-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15996-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="15996-109">DESCRIPTION</span></span>
<span data-ttu-id="15996-110">Atualiza a Tabela de Cassandra do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="15996-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="15996-111">Executa uma operação de patch do lado do cliente lendo a Tabela existente.</span><span class="sxs-lookup"><span data-stu-id="15996-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="15996-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15996-112">EXAMPLES</span></span>

### <span data-ttu-id="15996-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15996-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="15996-114">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="15996-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="15996-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="15996-115">PARAMETERS</span></span>

### <span data-ttu-id="15996-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15996-116">-AccountName</span></span>
<span data-ttu-id="15996-117">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="15996-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="15996-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="15996-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="15996-119">TTL de Armazenamento Analítico.</span><span class="sxs-lookup"><span data-stu-id="15996-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="15996-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="15996-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="15996-121">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="15996-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="15996-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15996-122">-Confirm</span></span>
<span data-ttu-id="15996-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15996-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15996-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15996-124">-DefaultProfile</span></span>
<span data-ttu-id="15996-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15996-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15996-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15996-126">-InputObject</span></span>
<span data-ttu-id="15996-127">Objeto Table de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="15996-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="15996-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="15996-128">-KeyspaceName</span></span>
<span data-ttu-id="15996-129">Nome do Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="15996-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="15996-130">-Name</span><span class="sxs-lookup"><span data-stu-id="15996-130">-Name</span></span>
<span data-ttu-id="15996-131">Nome da tabela de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="15996-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="15996-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15996-132">-ParentObject</span></span>
<span data-ttu-id="15996-133">Objeto Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="15996-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="15996-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15996-134">-ResourceGroupName</span></span>
<span data-ttu-id="15996-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15996-135">Name of resource group.</span></span>

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

### <span data-ttu-id="15996-136">-Esquema</span><span class="sxs-lookup"><span data-stu-id="15996-136">-Schema</span></span>
<span data-ttu-id="15996-137">Objeto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="15996-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="15996-138">Use New-AzCosmosDBCassandraSchema para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="15996-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15996-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="15996-139">-Throughput</span></span>
<span data-ttu-id="15996-140">A produtividade de Cassandra Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="15996-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="15996-141">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="15996-141">Default value is 400.</span></span>

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

### <span data-ttu-id="15996-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="15996-142">-TtlInSeconds</span></span>
<span data-ttu-id="15996-143">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="15996-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="15996-144">Se o valor estiver faltando ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="15996-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="15996-145">Se o valor for definido como n, os itens expiram n segundos após o último tempo modificado.</span><span class="sxs-lookup"><span data-stu-id="15996-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="15996-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15996-146">-WhatIf</span></span>
<span data-ttu-id="15996-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15996-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15996-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15996-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15996-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15996-149">CommonParameters</span></span>
<span data-ttu-id="15996-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15996-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15996-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15996-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15996-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15996-152">INPUTS</span></span>

### <span data-ttu-id="15996-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="15996-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="15996-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="15996-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="15996-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="15996-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="15996-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="15996-156">OUTPUTS</span></span>

### <span data-ttu-id="15996-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="15996-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="15996-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="15996-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="15996-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="15996-159">NOTES</span></span>

## <span data-ttu-id="15996-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15996-160">RELATED LINKS</span></span>
