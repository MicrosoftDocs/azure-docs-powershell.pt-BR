---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430005"
---
# <span data-ttu-id="7aa66-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="7aa66-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="7aa66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7aa66-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa66-103">Atualiza o valor de produtividade de uma coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="7aa66-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7aa66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7aa66-104">SYNTAX</span></span>

### <span data-ttu-id="7aa66-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7aa66-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aa66-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aa66-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aa66-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aa66-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aa66-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7aa66-108">DESCRIPTION</span></span>
<span data-ttu-id="7aa66-109">Atualiza o valor de produtividade de uma coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="7aa66-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7aa66-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7aa66-110">EXAMPLES</span></span>

### <span data-ttu-id="7aa66-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7aa66-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="7aa66-112">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="7aa66-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="7aa66-113">OS</span><span class="sxs-lookup"><span data-stu-id="7aa66-113">PARAMETERS</span></span>

### <span data-ttu-id="7aa66-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7aa66-114">-AccountName</span></span>
<span data-ttu-id="7aa66-115">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="7aa66-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7aa66-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7aa66-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7aa66-117">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="7aa66-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7aa66-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7aa66-118">-Confirm</span></span>
<span data-ttu-id="7aa66-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7aa66-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aa66-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7aa66-120">-DatabaseName</span></span>
<span data-ttu-id="7aa66-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7aa66-121">Database name.</span></span>

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

### <span data-ttu-id="7aa66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa66-122">-DefaultProfile</span></span>
<span data-ttu-id="7aa66-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7aa66-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aa66-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7aa66-124">-InputObject</span></span>
<span data-ttu-id="7aa66-125">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="7aa66-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="7aa66-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7aa66-126">-Name</span></span>
<span data-ttu-id="7aa66-127">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="7aa66-127">Collection name.</span></span>

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

### <span data-ttu-id="7aa66-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7aa66-128">-ParentObject</span></span>
<span data-ttu-id="7aa66-129">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="7aa66-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="7aa66-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa66-130">-ResourceGroupName</span></span>
<span data-ttu-id="7aa66-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7aa66-131">Name of resource group.</span></span>

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

### <span data-ttu-id="7aa66-132">-Throughput</span><span class="sxs-lookup"><span data-stu-id="7aa66-132">-Throughput</span></span>
<span data-ttu-id="7aa66-133">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="7aa66-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="7aa66-134">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="7aa66-134">Default value is 400.</span></span>

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

### <span data-ttu-id="7aa66-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa66-135">-WhatIf</span></span>
<span data-ttu-id="7aa66-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7aa66-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aa66-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7aa66-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aa66-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa66-138">CommonParameters</span></span>
<span data-ttu-id="7aa66-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa66-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa66-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7aa66-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa66-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7aa66-141">INPUTS</span></span>

### <span data-ttu-id="7aa66-142">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7aa66-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="7aa66-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7aa66-143">OUTPUTS</span></span>

### <span data-ttu-id="7aa66-144">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7aa66-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7aa66-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7aa66-145">NOTES</span></span>

## <span data-ttu-id="7aa66-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7aa66-146">RELATED LINKS</span></span>
