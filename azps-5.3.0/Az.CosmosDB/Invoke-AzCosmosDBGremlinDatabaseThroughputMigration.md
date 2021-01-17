---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 84039f883937354cf8c8fae3c99bfbc6f73bb574
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430073"
---
# <span data-ttu-id="6687e-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="6687e-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="6687e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6687e-102">SYNOPSIS</span></span>
<span data-ttu-id="6687e-103">Use isso para migrar a produtividade de AutoEscala para a taxa de transferência manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="6687e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="6687e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6687e-104">SYNTAX</span></span>

### <span data-ttu-id="6687e-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6687e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6687e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6687e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6687e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6687e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6687e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6687e-108">DESCRIPTION</span></span>
<span data-ttu-id="6687e-109">O parâmetro ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="6687e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="6687e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6687e-110">EXAMPLES</span></span>

### <span data-ttu-id="6687e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6687e-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```


## <span data-ttu-id="6687e-112">OS</span><span class="sxs-lookup"><span data-stu-id="6687e-112">PARAMETERS</span></span>

### <span data-ttu-id="6687e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6687e-113">-AccountName</span></span>
<span data-ttu-id="6687e-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="6687e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6687e-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6687e-115">-Confirm</span></span>
<span data-ttu-id="6687e-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6687e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6687e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6687e-117">-DefaultProfile</span></span>
<span data-ttu-id="6687e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6687e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6687e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6687e-119">-InputObject</span></span>
<span data-ttu-id="6687e-120">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6687e-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6687e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6687e-121">-Name</span></span>
<span data-ttu-id="6687e-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6687e-122">Database name.</span></span>

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

### <span data-ttu-id="6687e-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6687e-123">-ParentObject</span></span>
<span data-ttu-id="6687e-124">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6687e-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6687e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6687e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6687e-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6687e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="6687e-127">-Throughputtype</span><span class="sxs-lookup"><span data-stu-id="6687e-127">-ThroughputType</span></span>
<span data-ttu-id="6687e-128">Tipo de produtividade para migração.</span><span class="sxs-lookup"><span data-stu-id="6687e-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="6687e-129">Os valores possíveis são: autoescala, manual.</span><span class="sxs-lookup"><span data-stu-id="6687e-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="6687e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6687e-130">-WhatIf</span></span>
<span data-ttu-id="6687e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6687e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6687e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6687e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6687e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6687e-133">CommonParameters</span></span>
<span data-ttu-id="6687e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6687e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6687e-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6687e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6687e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6687e-136">INPUTS</span></span>

### <span data-ttu-id="6687e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="6687e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="6687e-138">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6687e-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="6687e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6687e-139">OUTPUTS</span></span>

### <span data-ttu-id="6687e-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6687e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6687e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6687e-141">NOTES</span></span>

## <span data-ttu-id="6687e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6687e-142">RELATED LINKS</span></span>
