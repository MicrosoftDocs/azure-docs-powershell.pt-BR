---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264392"
---
# <span data-ttu-id="1fae8-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="1fae8-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="1fae8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fae8-102">SYNOPSIS</span></span>
<span data-ttu-id="1fae8-103">Atualiza a coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="1fae8-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="1fae8-104">Executa uma operação de patch do lado do cliente lendo a coleção existente.</span><span class="sxs-lookup"><span data-stu-id="1fae8-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="1fae8-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fae8-105">SYNTAX</span></span>

### <span data-ttu-id="1fae8-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1fae8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fae8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fae8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fae8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fae8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1fae8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fae8-109">DESCRIPTION</span></span>
<span data-ttu-id="1fae8-110">Atualiza a coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="1fae8-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="1fae8-111">Executa uma operação de patch do lado do cliente lendo a coleção existente.</span><span class="sxs-lookup"><span data-stu-id="1fae8-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="1fae8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fae8-112">EXAMPLES</span></span>

### <span data-ttu-id="1fae8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fae8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="1fae8-114">OS</span><span class="sxs-lookup"><span data-stu-id="1fae8-114">PARAMETERS</span></span>

### <span data-ttu-id="1fae8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1fae8-115">-AccountName</span></span>
<span data-ttu-id="1fae8-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="1fae8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1fae8-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="1fae8-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="1fae8-118">TTL para armazenamento analítico.</span><span class="sxs-lookup"><span data-stu-id="1fae8-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="1fae8-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1fae8-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1fae8-120">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="1fae8-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1fae8-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1fae8-121">-Confirm</span></span>
<span data-ttu-id="1fae8-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fae8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fae8-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fae8-123">-DatabaseName</span></span>
<span data-ttu-id="1fae8-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1fae8-124">Database name.</span></span>

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

### <span data-ttu-id="1fae8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fae8-125">-DefaultProfile</span></span>
<span data-ttu-id="1fae8-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fae8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fae8-127">-Índice</span><span class="sxs-lookup"><span data-stu-id="1fae8-127">-Index</span></span>
<span data-ttu-id="1fae8-128">Matriz de objetos PSMongoIndex.</span><span class="sxs-lookup"><span data-stu-id="1fae8-128">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fae8-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fae8-129">-InputObject</span></span>
<span data-ttu-id="1fae8-130">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="1fae8-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fae8-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fae8-131">-Name</span></span>
<span data-ttu-id="1fae8-132">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="1fae8-132">Collection name.</span></span>

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

### <span data-ttu-id="1fae8-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1fae8-133">-ParentObject</span></span>
<span data-ttu-id="1fae8-134">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="1fae8-134">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fae8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fae8-135">-ResourceGroupName</span></span>
<span data-ttu-id="1fae8-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fae8-136">Name of resource group.</span></span>

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

### <span data-ttu-id="1fae8-137">-Fragmentos</span><span class="sxs-lookup"><span data-stu-id="1fae8-137">-Shard</span></span>
<span data-ttu-id="1fae8-138">Caminho da chave de fragmentação.</span><span class="sxs-lookup"><span data-stu-id="1fae8-138">Sharding key path.</span></span>

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

### <span data-ttu-id="1fae8-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="1fae8-139">-Throughput</span></span>
<span data-ttu-id="1fae8-140">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1fae8-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="1fae8-141">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="1fae8-141">Default value is 400.</span></span>

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

### <span data-ttu-id="1fae8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fae8-142">-WhatIf</span></span>
<span data-ttu-id="1fae8-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1fae8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fae8-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fae8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fae8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fae8-145">CommonParameters</span></span>
<span data-ttu-id="1fae8-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fae8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fae8-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fae8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fae8-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fae8-148">INPUTS</span></span>

### <span data-ttu-id="1fae8-149">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1fae8-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="1fae8-150">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="1fae8-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="1fae8-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fae8-151">OUTPUTS</span></span>

### <span data-ttu-id="1fae8-152">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="1fae8-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="1fae8-153">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1fae8-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1fae8-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fae8-154">NOTES</span></span>

## <span data-ttu-id="1fae8-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fae8-155">RELATED LINKS</span></span>
