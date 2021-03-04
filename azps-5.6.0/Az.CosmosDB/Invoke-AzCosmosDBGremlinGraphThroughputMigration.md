---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 4fc0c28293484b2f3791145591576d4110ac2974
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890285"
---
# <span data-ttu-id="287cc-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="287cc-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="287cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287cc-102">SYNOPSIS</span></span>
<span data-ttu-id="287cc-103">Use isso para migrar a produtividade de escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="287cc-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="287cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="287cc-104">SYNTAX</span></span>

### <span data-ttu-id="287cc-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="287cc-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="287cc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="287cc-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="287cc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="287cc-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="287cc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="287cc-108">DESCRIPTION</span></span>
<span data-ttu-id="287cc-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="287cc-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="287cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="287cc-110">EXAMPLES</span></span>

### <span data-ttu-id="287cc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="287cc-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="287cc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="287cc-112">PARAMETERS</span></span>

### <span data-ttu-id="287cc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="287cc-113">-AccountName</span></span>
<span data-ttu-id="287cc-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="287cc-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="287cc-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="287cc-115">-Confirm</span></span>
<span data-ttu-id="287cc-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="287cc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="287cc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="287cc-117">-DatabaseName</span></span>
<span data-ttu-id="287cc-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="287cc-118">Database name.</span></span>

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

### <span data-ttu-id="287cc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287cc-119">-DefaultProfile</span></span>
<span data-ttu-id="287cc-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="287cc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="287cc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="287cc-121">-InputObject</span></span>
<span data-ttu-id="287cc-122">Objeto Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="287cc-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="287cc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="287cc-123">-Name</span></span>
<span data-ttu-id="287cc-124">Nome do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="287cc-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="287cc-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="287cc-125">-ParentObject</span></span>
<span data-ttu-id="287cc-126">Objeto Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="287cc-126">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="287cc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287cc-127">-ResourceGroupName</span></span>
<span data-ttu-id="287cc-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="287cc-128">Name of resource group.</span></span>

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

### <span data-ttu-id="287cc-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="287cc-129">-ThroughputType</span></span>
<span data-ttu-id="287cc-130">Tipo de transferência para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="287cc-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="287cc-131">Os valores possíveis são: Escala automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="287cc-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="287cc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287cc-132">-WhatIf</span></span>
<span data-ttu-id="287cc-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="287cc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="287cc-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="287cc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="287cc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287cc-135">CommonParameters</span></span>
<span data-ttu-id="287cc-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287cc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287cc-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="287cc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287cc-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="287cc-138">INPUTS</span></span>

### <span data-ttu-id="287cc-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="287cc-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="287cc-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="287cc-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="287cc-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="287cc-141">OUTPUTS</span></span>

### <span data-ttu-id="287cc-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="287cc-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="287cc-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="287cc-143">NOTES</span></span>

## <span data-ttu-id="287cc-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="287cc-144">RELATED LINKS</span></span>
