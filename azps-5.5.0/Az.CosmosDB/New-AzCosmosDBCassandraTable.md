---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116459"
---
# <span data-ttu-id="db001-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="db001-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="db001-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db001-102">SYNOPSIS</span></span>
<span data-ttu-id="db001-103">Cria uma nova Tabela de YorkDB.</span><span class="sxs-lookup"><span data-stu-id="db001-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="db001-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db001-104">SYNTAX</span></span>

### <span data-ttu-id="db001-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db001-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db001-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db001-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db001-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="db001-107">DESCRIPTION</span></span>
<span data-ttu-id="db001-108">Cria uma nova Tabela de YorkDB.</span><span class="sxs-lookup"><span data-stu-id="db001-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="db001-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db001-109">EXAMPLES</span></span>

### <span data-ttu-id="db001-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db001-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="db001-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db001-111">PARAMETERS</span></span>

### <span data-ttu-id="db001-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="db001-112">-AccountName</span></span>
<span data-ttu-id="db001-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="db001-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="db001-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="db001-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="db001-115">TTL de Armazenamento Analítico.</span><span class="sxs-lookup"><span data-stu-id="db001-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="db001-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="db001-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="db001-117">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="db001-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="db001-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db001-118">-Confirm</span></span>
<span data-ttu-id="db001-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db001-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db001-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db001-120">-DefaultProfile</span></span>
<span data-ttu-id="db001-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db001-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db001-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="db001-122">-KeyspaceName</span></span>
<span data-ttu-id="db001-123">Nome do Espaço de Teclas Denúm.</span><span class="sxs-lookup"><span data-stu-id="db001-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="db001-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="db001-124">-Name</span></span>
<span data-ttu-id="db001-125">Nome da tabela Desarmá.</span><span class="sxs-lookup"><span data-stu-id="db001-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="db001-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="db001-126">-ParentObject</span></span>
<span data-ttu-id="db001-127">Objeto Desarmado Keyspace.</span><span class="sxs-lookup"><span data-stu-id="db001-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="db001-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db001-128">-ResourceGroupName</span></span>
<span data-ttu-id="db001-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db001-129">Name of resource group.</span></span>

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

### <span data-ttu-id="db001-130">-Esquema</span><span class="sxs-lookup"><span data-stu-id="db001-130">-Schema</span></span>
<span data-ttu-id="db001-131">Objeto PSCasschema.</span><span class="sxs-lookup"><span data-stu-id="db001-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="db001-132">Use New-AzCosmosDBCassandraSchema para criar este objeto.</span><span class="sxs-lookup"><span data-stu-id="db001-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="db001-133">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="db001-133">-Throughput</span></span>
<span data-ttu-id="db001-134">A produtividade de Guida Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="db001-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="db001-135">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="db001-135">Default value is 400.</span></span>

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

### <span data-ttu-id="db001-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="db001-136">-TtlInSeconds</span></span>
<span data-ttu-id="db001-137">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="db001-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="db001-138">Se o valor estiver ausente ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="db001-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="db001-139">Se o valor estiver definido como n, os itens expiram n segundos após o tempo da última modificação.</span><span class="sxs-lookup"><span data-stu-id="db001-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="db001-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db001-140">-WhatIf</span></span>
<span data-ttu-id="db001-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db001-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db001-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db001-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db001-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db001-143">CommonParameters</span></span>
<span data-ttu-id="db001-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db001-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db001-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db001-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db001-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="db001-146">INPUTS</span></span>

### <span data-ttu-id="db001-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCasschema</span><span class="sxs-lookup"><span data-stu-id="db001-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="db001-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="db001-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="db001-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="db001-149">OUTPUTS</span></span>

### <span data-ttu-id="db001-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCasstableGetResults</span><span class="sxs-lookup"><span data-stu-id="db001-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="db001-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="db001-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="db001-152">Notas</span><span class="sxs-lookup"><span data-stu-id="db001-152">NOTES</span></span>

## <span data-ttu-id="db001-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db001-153">RELATED LINKS</span></span>
