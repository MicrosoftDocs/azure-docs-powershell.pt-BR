---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 605998d6bc5ae8b647b3644dc71b8063f0881910
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942184"
---
# <span data-ttu-id="34d2f-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="34d2f-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="34d2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="34d2f-103">Atualiza o valor de produtividade de uma coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="34d2f-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="34d2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34d2f-104">SYNTAX</span></span>

### <span data-ttu-id="34d2f-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="34d2f-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34d2f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34d2f-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34d2f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34d2f-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34d2f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34d2f-108">EXAMPLES</span></span>

### <span data-ttu-id="34d2f-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34d2f-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="34d2f-110">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="34d2f-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="34d2f-111">OS</span><span class="sxs-lookup"><span data-stu-id="34d2f-111">PARAMETERS</span></span>

### <span data-ttu-id="34d2f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="34d2f-112">-AccountName</span></span>
<span data-ttu-id="34d2f-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="34d2f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="34d2f-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34d2f-114">-Confirm</span></span>
<span data-ttu-id="34d2f-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34d2f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34d2f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34d2f-116">-DatabaseName</span></span>
<span data-ttu-id="34d2f-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="34d2f-117">Database name.</span></span>

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

### <span data-ttu-id="34d2f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d2f-118">-DefaultProfile</span></span>
<span data-ttu-id="34d2f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34d2f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d2f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34d2f-120">-InputObject</span></span>
<span data-ttu-id="34d2f-121">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="34d2f-121">Mongo Database object.</span></span>

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

### <span data-ttu-id="34d2f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="34d2f-122">-Name</span></span>
<span data-ttu-id="34d2f-123">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="34d2f-123">Collection name.</span></span>

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

### <span data-ttu-id="34d2f-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34d2f-124">-ParentObject</span></span>
<span data-ttu-id="34d2f-125">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="34d2f-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="34d2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="34d2f-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34d2f-127">Name of resource group.</span></span>

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

### <span data-ttu-id="34d2f-128">-Throughput</span><span class="sxs-lookup"><span data-stu-id="34d2f-128">-Throughput</span></span>
<span data-ttu-id="34d2f-129">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="34d2f-129">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="34d2f-130">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="34d2f-130">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d2f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d2f-131">-WhatIf</span></span>
<span data-ttu-id="34d2f-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34d2f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d2f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34d2f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34d2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d2f-134">CommonParameters</span></span>
<span data-ttu-id="34d2f-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d2f-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34d2f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d2f-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34d2f-137">INPUTS</span></span>

### <span data-ttu-id="34d2f-138">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="34d2f-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="34d2f-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34d2f-139">OUTPUTS</span></span>

### <span data-ttu-id="34d2f-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="34d2f-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="34d2f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34d2f-141">NOTES</span></span>

## <span data-ttu-id="34d2f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34d2f-142">RELATED LINKS</span></span>
