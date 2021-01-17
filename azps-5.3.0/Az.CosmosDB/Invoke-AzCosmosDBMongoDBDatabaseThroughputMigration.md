---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434079"
---
# <span data-ttu-id="90dc4-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="90dc4-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="90dc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="90dc4-103">Use isso para migrar a produtividade de AutoEscala para a taxa de transferência manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="90dc4-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="90dc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90dc4-104">SYNTAX</span></span>

### <span data-ttu-id="90dc4-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="90dc4-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90dc4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90dc4-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90dc4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90dc4-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90dc4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90dc4-108">DESCRIPTION</span></span>
<span data-ttu-id="90dc4-109">O parâmetro ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="90dc4-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="90dc4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90dc4-110">EXAMPLES</span></span>

### <span data-ttu-id="90dc4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90dc4-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="90dc4-112">OS</span><span class="sxs-lookup"><span data-stu-id="90dc4-112">PARAMETERS</span></span>

### <span data-ttu-id="90dc4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="90dc4-113">-AccountName</span></span>
<span data-ttu-id="90dc4-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="90dc4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="90dc4-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="90dc4-115">-Confirm</span></span>
<span data-ttu-id="90dc4-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90dc4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90dc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90dc4-117">-DefaultProfile</span></span>
<span data-ttu-id="90dc4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90dc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90dc4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90dc4-119">-InputObject</span></span>
<span data-ttu-id="90dc4-120">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="90dc4-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90dc4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="90dc4-121">-Name</span></span>
<span data-ttu-id="90dc4-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="90dc4-122">Database name.</span></span>

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

### <span data-ttu-id="90dc4-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="90dc4-123">-ParentObject</span></span>
<span data-ttu-id="90dc4-124">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="90dc4-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dc4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90dc4-125">-ResourceGroupName</span></span>
<span data-ttu-id="90dc4-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90dc4-126">Name of resource group.</span></span>

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

### <span data-ttu-id="90dc4-127">-Throughputtype</span><span class="sxs-lookup"><span data-stu-id="90dc4-127">-ThroughputType</span></span>
<span data-ttu-id="90dc4-128">Tipo de produtividade para migração.</span><span class="sxs-lookup"><span data-stu-id="90dc4-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="90dc4-129">Os valores possíveis são: autoescala, manual.</span><span class="sxs-lookup"><span data-stu-id="90dc4-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="90dc4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90dc4-130">-WhatIf</span></span>
<span data-ttu-id="90dc4-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90dc4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90dc4-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90dc4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90dc4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90dc4-133">CommonParameters</span></span>
<span data-ttu-id="90dc4-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90dc4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90dc4-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90dc4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90dc4-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90dc4-136">INPUTS</span></span>

### <span data-ttu-id="90dc4-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="90dc4-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="90dc4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90dc4-138">OUTPUTS</span></span>

### <span data-ttu-id="90dc4-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="90dc4-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="90dc4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90dc4-140">NOTES</span></span>

## <span data-ttu-id="90dc4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90dc4-141">RELATED LINKS</span></span>
