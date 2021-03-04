---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 66ca19099d4562da3add57411a16be1a0573ea02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888548"
---
# <span data-ttu-id="1eb72-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="1eb72-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="1eb72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb72-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb72-103">Atualiza o valor de produtividade de uma coleção MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1eb72-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="1eb72-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1eb72-104">SYNTAX</span></span>

### <span data-ttu-id="1eb72-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1eb72-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb72-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb72-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb72-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb72-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb72-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1eb72-108">DESCRIPTION</span></span>
<span data-ttu-id="1eb72-109">Atualiza o valor de produtividade de uma coleção MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1eb72-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="1eb72-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eb72-110">EXAMPLES</span></span>

### <span data-ttu-id="1eb72-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1eb72-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="1eb72-112">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="1eb72-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="1eb72-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1eb72-113">PARAMETERS</span></span>

### <span data-ttu-id="1eb72-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1eb72-114">-AccountName</span></span>
<span data-ttu-id="1eb72-115">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="1eb72-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1eb72-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1eb72-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1eb72-117">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="1eb72-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1eb72-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb72-118">-Confirm</span></span>
<span data-ttu-id="1eb72-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eb72-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb72-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1eb72-120">-DatabaseName</span></span>
<span data-ttu-id="1eb72-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1eb72-121">Database name.</span></span>

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

### <span data-ttu-id="1eb72-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb72-122">-DefaultProfile</span></span>
<span data-ttu-id="1eb72-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb72-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb72-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eb72-124">-InputObject</span></span>
<span data-ttu-id="1eb72-125">Objeto Mongo Database.</span><span class="sxs-lookup"><span data-stu-id="1eb72-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="1eb72-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1eb72-126">-Name</span></span>
<span data-ttu-id="1eb72-127">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="1eb72-127">Collection name.</span></span>

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

### <span data-ttu-id="1eb72-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1eb72-128">-ParentObject</span></span>
<span data-ttu-id="1eb72-129">Objeto Mongo Database.</span><span class="sxs-lookup"><span data-stu-id="1eb72-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="1eb72-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb72-130">-ResourceGroupName</span></span>
<span data-ttu-id="1eb72-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1eb72-131">Name of resource group.</span></span>

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

### <span data-ttu-id="1eb72-132">-Throughput</span><span class="sxs-lookup"><span data-stu-id="1eb72-132">-Throughput</span></span>
<span data-ttu-id="1eb72-133">A produtividade de SQL contêiner (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1eb72-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="1eb72-134">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="1eb72-134">Default value is 400.</span></span>

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

### <span data-ttu-id="1eb72-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb72-135">-WhatIf</span></span>
<span data-ttu-id="1eb72-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1eb72-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb72-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1eb72-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb72-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb72-138">CommonParameters</span></span>
<span data-ttu-id="1eb72-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb72-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb72-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eb72-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb72-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1eb72-141">INPUTS</span></span>

### <span data-ttu-id="1eb72-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1eb72-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="1eb72-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1eb72-143">OUTPUTS</span></span>

### <span data-ttu-id="1eb72-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1eb72-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1eb72-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="1eb72-145">NOTES</span></span>

## <span data-ttu-id="1eb72-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eb72-146">RELATED LINKS</span></span>
