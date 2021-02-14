---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116450"
---
# <span data-ttu-id="34090-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="34090-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="34090-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34090-102">SYNOPSIS</span></span>
<span data-ttu-id="34090-103">Atualiza a Tabela Desarmádia DaLMDB.</span><span class="sxs-lookup"><span data-stu-id="34090-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="34090-104">Executa uma operação de patch do lado do cliente lendo a Tabela existente.</span><span class="sxs-lookup"><span data-stu-id="34090-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="34090-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34090-105">SYNTAX</span></span>

### <span data-ttu-id="34090-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34090-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34090-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34090-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34090-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34090-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34090-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="34090-109">DESCRIPTION</span></span>
<span data-ttu-id="34090-110">Atualiza a Tabela Desarmádia DaLMDB.</span><span class="sxs-lookup"><span data-stu-id="34090-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="34090-111">Executa uma operação de patch do lado do cliente lendo a Tabela existente.</span><span class="sxs-lookup"><span data-stu-id="34090-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="34090-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34090-112">EXAMPLES</span></span>

### <span data-ttu-id="34090-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34090-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="34090-114">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="34090-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="34090-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34090-115">PARAMETERS</span></span>

### <span data-ttu-id="34090-116">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="34090-116">-AccountName</span></span>
<span data-ttu-id="34090-117">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="34090-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34090-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="34090-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="34090-119">TTL de Armazenamento Analítico.</span><span class="sxs-lookup"><span data-stu-id="34090-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="34090-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="34090-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="34090-121">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="34090-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="34090-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="34090-122">-Confirm</span></span>
<span data-ttu-id="34090-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34090-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34090-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34090-124">-DefaultProfile</span></span>
<span data-ttu-id="34090-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34090-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34090-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34090-126">-InputObject</span></span>
<span data-ttu-id="34090-127">Objeto Table Desarmado.</span><span class="sxs-lookup"><span data-stu-id="34090-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="34090-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="34090-128">-KeyspaceName</span></span>
<span data-ttu-id="34090-129">Nome do Espaço de Teclas Descaroçador.</span><span class="sxs-lookup"><span data-stu-id="34090-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="34090-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="34090-130">-Name</span></span>
<span data-ttu-id="34090-131">Nome da tabela Desarmá.</span><span class="sxs-lookup"><span data-stu-id="34090-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="34090-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34090-132">-ParentObject</span></span>
<span data-ttu-id="34090-133">Objeto Desa Keyspace.</span><span class="sxs-lookup"><span data-stu-id="34090-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="34090-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34090-134">-ResourceGroupName</span></span>
<span data-ttu-id="34090-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34090-135">Name of resource group.</span></span>

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

### <span data-ttu-id="34090-136">-Esquema</span><span class="sxs-lookup"><span data-stu-id="34090-136">-Schema</span></span>
<span data-ttu-id="34090-137">Objeto PSCasschema.</span><span class="sxs-lookup"><span data-stu-id="34090-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="34090-138">Use New-AzCosmosDBCassandraSchema para criar este objeto.</span><span class="sxs-lookup"><span data-stu-id="34090-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="34090-139">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="34090-139">-Throughput</span></span>
<span data-ttu-id="34090-140">A produtividade de Guida Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="34090-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="34090-141">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="34090-141">Default value is 400.</span></span>

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

### <span data-ttu-id="34090-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="34090-142">-TtlInSeconds</span></span>
<span data-ttu-id="34090-143">Ttl padrão em segundos.</span><span class="sxs-lookup"><span data-stu-id="34090-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="34090-144">Se o valor estiver ausente ou definido como - 1, os itens não expiram.</span><span class="sxs-lookup"><span data-stu-id="34090-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="34090-145">Se o valor estiver definido como n, os itens expiram n segundos após o tempo da última modificação.</span><span class="sxs-lookup"><span data-stu-id="34090-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="34090-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34090-146">-WhatIf</span></span>
<span data-ttu-id="34090-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="34090-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34090-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34090-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34090-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34090-149">CommonParameters</span></span>
<span data-ttu-id="34090-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34090-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34090-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34090-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34090-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="34090-152">INPUTS</span></span>

### <span data-ttu-id="34090-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCasschema</span><span class="sxs-lookup"><span data-stu-id="34090-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="34090-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="34090-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="34090-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCasstableGetResults</span><span class="sxs-lookup"><span data-stu-id="34090-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="34090-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="34090-156">OUTPUTS</span></span>

### <span data-ttu-id="34090-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCasstableGetResults</span><span class="sxs-lookup"><span data-stu-id="34090-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="34090-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="34090-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="34090-159">Notas</span><span class="sxs-lookup"><span data-stu-id="34090-159">NOTES</span></span>

## <span data-ttu-id="34090-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34090-160">RELATED LINKS</span></span>
