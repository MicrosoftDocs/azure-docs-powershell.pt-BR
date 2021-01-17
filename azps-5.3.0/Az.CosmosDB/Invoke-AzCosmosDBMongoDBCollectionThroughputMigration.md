---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: e2f1449536f9b4db5b743c1a1e352e427ae86821
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430069"
---
# <span data-ttu-id="3578a-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="3578a-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="3578a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3578a-102">SYNOPSIS</span></span>
<span data-ttu-id="3578a-103">Use isso para migrar a produtividade de AutoEscala para a taxa de transferência manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="3578a-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="3578a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3578a-104">SYNTAX</span></span>

### <span data-ttu-id="3578a-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3578a-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3578a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3578a-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3578a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3578a-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3578a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3578a-108">DESCRIPTION</span></span>
<span data-ttu-id="3578a-109">O parâmetro ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="3578a-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="3578a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3578a-110">EXAMPLES</span></span>

### <span data-ttu-id="3578a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3578a-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```


## <span data-ttu-id="3578a-112">OS</span><span class="sxs-lookup"><span data-stu-id="3578a-112">PARAMETERS</span></span>

### <span data-ttu-id="3578a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3578a-113">-AccountName</span></span>
<span data-ttu-id="3578a-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="3578a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3578a-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3578a-115">-Confirm</span></span>
<span data-ttu-id="3578a-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3578a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3578a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3578a-117">-DatabaseName</span></span>
<span data-ttu-id="3578a-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3578a-118">Database name.</span></span>

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

### <span data-ttu-id="3578a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3578a-119">-DefaultProfile</span></span>
<span data-ttu-id="3578a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3578a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3578a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3578a-121">-InputObject</span></span>
<span data-ttu-id="3578a-122">Objeto da coleção Mongo.</span><span class="sxs-lookup"><span data-stu-id="3578a-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="3578a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3578a-123">-Name</span></span>
<span data-ttu-id="3578a-124">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="3578a-124">Collection name.</span></span>

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

### <span data-ttu-id="3578a-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3578a-125">-ParentObject</span></span>
<span data-ttu-id="3578a-126">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="3578a-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="3578a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3578a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3578a-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3578a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="3578a-129">-Throughputtype</span><span class="sxs-lookup"><span data-stu-id="3578a-129">-ThroughputType</span></span>
<span data-ttu-id="3578a-130">Tipo de produtividade para migração.</span><span class="sxs-lookup"><span data-stu-id="3578a-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="3578a-131">Os valores possíveis são: autoescala, manual.</span><span class="sxs-lookup"><span data-stu-id="3578a-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="3578a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3578a-132">-WhatIf</span></span>
<span data-ttu-id="3578a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3578a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3578a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3578a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3578a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3578a-135">CommonParameters</span></span>
<span data-ttu-id="3578a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3578a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3578a-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3578a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3578a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3578a-138">INPUTS</span></span>

### <span data-ttu-id="3578a-139">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3578a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="3578a-140">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="3578a-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="3578a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3578a-141">OUTPUTS</span></span>

### <span data-ttu-id="3578a-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3578a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3578a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3578a-143">NOTES</span></span>

## <span data-ttu-id="3578a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3578a-144">RELATED LINKS</span></span>
