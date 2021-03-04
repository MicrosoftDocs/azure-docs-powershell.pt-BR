---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: bbe2cc26eb5f57e31457023285d8f27a1d326321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887998"
---
# <span data-ttu-id="c3d10-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c3d10-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="c3d10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d10-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d10-103">Use isso para migrar a produtividade de escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="c3d10-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c3d10-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c3d10-104">SYNTAX</span></span>

### <span data-ttu-id="c3d10-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c3d10-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3d10-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d10-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d10-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d10-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d10-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3d10-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d10-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="c3d10-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c3d10-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3d10-110">EXAMPLES</span></span>

### <span data-ttu-id="c3d10-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3d10-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```

## <span data-ttu-id="c3d10-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c3d10-112">PARAMETERS</span></span>

### <span data-ttu-id="c3d10-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c3d10-113">-AccountName</span></span>
<span data-ttu-id="c3d10-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="c3d10-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c3d10-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3d10-115">-Confirm</span></span>
<span data-ttu-id="c3d10-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3d10-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d10-117">-DefaultProfile</span></span>
<span data-ttu-id="c3d10-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d10-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d10-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d10-119">-InputObject</span></span>
<span data-ttu-id="c3d10-120">Objeto Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="c3d10-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="c3d10-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c3d10-121">-Name</span></span>
<span data-ttu-id="c3d10-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c3d10-122">Database name.</span></span>

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

### <span data-ttu-id="c3d10-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c3d10-123">-ParentObject</span></span>
<span data-ttu-id="c3d10-124">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c3d10-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c3d10-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d10-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3d10-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c3d10-126">Name of resource group.</span></span>

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

### <span data-ttu-id="c3d10-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="c3d10-127">-ThroughputType</span></span>
<span data-ttu-id="c3d10-128">Tipo de transferência para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="c3d10-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="c3d10-129">Os valores possíveis são: Escala automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="c3d10-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="c3d10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d10-130">-WhatIf</span></span>
<span data-ttu-id="c3d10-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3d10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d10-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3d10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d10-133">CommonParameters</span></span>
<span data-ttu-id="c3d10-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d10-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3d10-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d10-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3d10-136">INPUTS</span></span>

### <span data-ttu-id="c3d10-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="c3d10-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="c3d10-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c3d10-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="c3d10-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c3d10-139">OUTPUTS</span></span>

### <span data-ttu-id="c3d10-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c3d10-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c3d10-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="c3d10-141">NOTES</span></span>

## <span data-ttu-id="c3d10-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3d10-142">RELATED LINKS</span></span>
