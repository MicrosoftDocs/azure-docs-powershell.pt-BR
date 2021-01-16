---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258156"
---
# <span data-ttu-id="6a7e7-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="6a7e7-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="6a7e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7e7-103">Obtém as propriedades de produtividade CosmosDB da coleção do MongoDB.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="6a7e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a7e7-104">SYNTAX</span></span>

### <span data-ttu-id="6a7e7-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6a7e7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a7e7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a7e7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a7e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a7e7-107">DESCRIPTION</span></span>
<span data-ttu-id="6a7e7-108">O cmdlet **Get-AzCosmosDBMongoDBCollectionThroughput** Obtém as propriedades de produtividade da coleção do MongoDB.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="6a7e7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a7e7-109">EXAMPLES</span></span>

### <span data-ttu-id="6a7e7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a7e7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="6a7e7-111">OS</span><span class="sxs-lookup"><span data-stu-id="6a7e7-111">PARAMETERS</span></span>

### <span data-ttu-id="6a7e7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6a7e7-112">-AccountName</span></span>
<span data-ttu-id="6a7e7-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6a7e7-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6a7e7-114">-Confirm</span></span>
<span data-ttu-id="6a7e7-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a7e7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a7e7-116">-DatabaseName</span></span>
<span data-ttu-id="6a7e7-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-117">Database name.</span></span>

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

### <span data-ttu-id="6a7e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7e7-118">-DefaultProfile</span></span>
<span data-ttu-id="6a7e7-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a7e7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a7e7-120">-InputObject</span></span>
<span data-ttu-id="6a7e7-121">Se fornecido, o cmdlet retornará a coleção com o valor de produtividade correspondente.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7e7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a7e7-122">-Name</span></span>
<span data-ttu-id="6a7e7-123">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-123">Collection name.</span></span>

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

### <span data-ttu-id="6a7e7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a7e7-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a7e7-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-125">Name of resource group.</span></span>

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

### <span data-ttu-id="6a7e7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a7e7-126">-WhatIf</span></span>
<span data-ttu-id="6a7e7-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a7e7-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a7e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7e7-129">CommonParameters</span></span>
<span data-ttu-id="6a7e7-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7e7-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a7e7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7e7-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a7e7-132">INPUTS</span></span>

### <span data-ttu-id="6a7e7-133">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="6a7e7-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="6a7e7-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a7e7-134">OUTPUTS</span></span>

### <span data-ttu-id="6a7e7-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6a7e7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6a7e7-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a7e7-136">NOTES</span></span>

## <span data-ttu-id="6a7e7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a7e7-137">RELATED LINKS</span></span>
