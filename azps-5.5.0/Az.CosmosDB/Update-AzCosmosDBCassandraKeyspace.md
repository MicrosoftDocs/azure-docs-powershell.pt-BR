---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111022"
---
# <span data-ttu-id="c7d84-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="c7d84-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="c7d84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7d84-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d84-103">Atualiza oSpace de Keyspace da CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c7d84-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="c7d84-104">Executa uma operação de patch do lado do cliente lendo o Espaço de Teclas existente.</span><span class="sxs-lookup"><span data-stu-id="c7d84-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="c7d84-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7d84-105">SYNTAX</span></span>

### <span data-ttu-id="c7d84-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c7d84-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7d84-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7d84-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7d84-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7d84-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7d84-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7d84-109">DESCRIPTION</span></span>
<span data-ttu-id="c7d84-110">Atualiza oSpace de Keyspace da CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c7d84-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="c7d84-111">Executa uma operação de patch do lado do cliente lendo o Espaço de Teclas existente.</span><span class="sxs-lookup"><span data-stu-id="c7d84-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="c7d84-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c7d84-112">EXAMPLES</span></span>

### <span data-ttu-id="c7d84-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7d84-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="c7d84-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7d84-114">PARAMETERS</span></span>

### <span data-ttu-id="c7d84-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="c7d84-115">-AccountName</span></span>
<span data-ttu-id="c7d84-116">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="c7d84-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c7d84-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c7d84-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c7d84-118">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="c7d84-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c7d84-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c7d84-119">-Confirm</span></span>
<span data-ttu-id="c7d84-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7d84-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7d84-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d84-121">-DefaultProfile</span></span>
<span data-ttu-id="c7d84-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d84-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7d84-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7d84-123">-InputObject</span></span>
<span data-ttu-id="c7d84-124">Objeto Desarmado Keyspace.</span><span class="sxs-lookup"><span data-stu-id="c7d84-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c7d84-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7d84-125">-Name</span></span>
<span data-ttu-id="c7d84-126">Nome do Espaço de Teclas Denúm.</span><span class="sxs-lookup"><span data-stu-id="c7d84-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c7d84-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c7d84-127">-ParentObject</span></span>
<span data-ttu-id="c7d84-128">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="c7d84-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c7d84-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d84-129">-ResourceGroupName</span></span>
<span data-ttu-id="c7d84-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7d84-130">Name of resource group.</span></span>

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

### <span data-ttu-id="c7d84-131">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="c7d84-131">-Throughput</span></span>
<span data-ttu-id="c7d84-132">A produtividade de Guida Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c7d84-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="c7d84-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="c7d84-133">Default value is 400.</span></span>

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

### <span data-ttu-id="c7d84-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7d84-134">-WhatIf</span></span>
<span data-ttu-id="c7d84-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c7d84-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7d84-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7d84-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7d84-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d84-137">CommonParameters</span></span>
<span data-ttu-id="c7d84-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d84-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d84-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7d84-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d84-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="c7d84-140">INPUTS</span></span>

### <span data-ttu-id="c7d84-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c7d84-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="c7d84-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c7d84-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="c7d84-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="c7d84-143">OUTPUTS</span></span>

### <span data-ttu-id="c7d84-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c7d84-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="c7d84-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c7d84-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c7d84-146">Notas</span><span class="sxs-lookup"><span data-stu-id="c7d84-146">NOTES</span></span>

## <span data-ttu-id="c7d84-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7d84-147">RELATED LINKS</span></span>
