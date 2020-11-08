---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114608"
---
# <span data-ttu-id="734ba-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="734ba-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="734ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="734ba-102">SYNOPSIS</span></span>
<span data-ttu-id="734ba-103">Atualiza a tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="734ba-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="734ba-104">Executa uma operação de patch do lado do cliente lendo a tabela existente.</span><span class="sxs-lookup"><span data-stu-id="734ba-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="734ba-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="734ba-105">SYNTAX</span></span>

### <span data-ttu-id="734ba-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="734ba-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="734ba-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="734ba-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="734ba-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="734ba-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="734ba-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="734ba-109">DESCRIPTION</span></span>
<span data-ttu-id="734ba-110">Atualiza a tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="734ba-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="734ba-111">Executa uma operação de patch do lado do cliente lendo a tabela existente.</span><span class="sxs-lookup"><span data-stu-id="734ba-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="734ba-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="734ba-112">EXAMPLES</span></span>

### <span data-ttu-id="734ba-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="734ba-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="734ba-114">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="734ba-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="734ba-115">OS</span><span class="sxs-lookup"><span data-stu-id="734ba-115">PARAMETERS</span></span>

### <span data-ttu-id="734ba-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="734ba-116">-AccountName</span></span>
<span data-ttu-id="734ba-117">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="734ba-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="734ba-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="734ba-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="734ba-119">TTL de armazenamento analítico.</span><span class="sxs-lookup"><span data-stu-id="734ba-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="734ba-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="734ba-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="734ba-121">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="734ba-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="734ba-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="734ba-122">-Confirm</span></span>
<span data-ttu-id="734ba-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="734ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734ba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734ba-124">-DefaultProfile</span></span>
<span data-ttu-id="734ba-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="734ba-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="734ba-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="734ba-126">-InputObject</span></span>
<span data-ttu-id="734ba-127">Objeto da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="734ba-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="734ba-128">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="734ba-128">-KeyspaceName</span></span>
<span data-ttu-id="734ba-129">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="734ba-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="734ba-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="734ba-130">-Name</span></span>
<span data-ttu-id="734ba-131">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="734ba-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="734ba-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="734ba-132">-ParentObject</span></span>
<span data-ttu-id="734ba-133">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="734ba-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="734ba-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="734ba-134">-ResourceGroupName</span></span>
<span data-ttu-id="734ba-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="734ba-135">Name of resource group.</span></span>

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

### <span data-ttu-id="734ba-136">-Esquema</span><span class="sxs-lookup"><span data-stu-id="734ba-136">-Schema</span></span>
<span data-ttu-id="734ba-137">Objeto PSCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="734ba-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="734ba-138">Use New-AzCosmosDBCassandraSchema para criar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="734ba-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="734ba-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="734ba-139">-Throughput</span></span>
<span data-ttu-id="734ba-140">A taxa de transferência do espaço de Cassandra (RU/s).</span><span class="sxs-lookup"><span data-stu-id="734ba-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="734ba-141">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="734ba-141">Default value is 400.</span></span>

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

### <span data-ttu-id="734ba-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="734ba-142">-TtlInSeconds</span></span>
<span data-ttu-id="734ba-143">TTL padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="734ba-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="734ba-144">Se o valor estiver ausente ou definido como-1, os itens não expirarão.</span><span class="sxs-lookup"><span data-stu-id="734ba-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="734ba-145">Se o valor for definido como n, os itens vencerão n segundos após o último período de modificação.</span><span class="sxs-lookup"><span data-stu-id="734ba-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="734ba-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="734ba-146">-WhatIf</span></span>
<span data-ttu-id="734ba-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="734ba-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="734ba-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="734ba-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734ba-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734ba-149">CommonParameters</span></span>
<span data-ttu-id="734ba-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734ba-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734ba-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="734ba-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734ba-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="734ba-152">INPUTS</span></span>

### <span data-ttu-id="734ba-153">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="734ba-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="734ba-154">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="734ba-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="734ba-155">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="734ba-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="734ba-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="734ba-156">OUTPUTS</span></span>

### <span data-ttu-id="734ba-157">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="734ba-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="734ba-158">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="734ba-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="734ba-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="734ba-159">NOTES</span></span>

## <span data-ttu-id="734ba-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="734ba-160">RELATED LINKS</span></span>
