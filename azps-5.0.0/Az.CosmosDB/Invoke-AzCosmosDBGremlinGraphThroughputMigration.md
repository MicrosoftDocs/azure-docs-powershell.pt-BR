---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281360"
---
# <span data-ttu-id="b0a60-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="b0a60-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="b0a60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0a60-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a60-103">Use isso para migrar a produtividade de AutoEscala para a taxa de transferência manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="b0a60-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="b0a60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0a60-104">SYNTAX</span></span>

### <span data-ttu-id="b0a60-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0a60-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a60-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a60-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a60-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a60-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0a60-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0a60-108">DESCRIPTION</span></span>
<span data-ttu-id="b0a60-109">O parâmetro ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="b0a60-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="b0a60-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0a60-110">EXAMPLES</span></span>

### <span data-ttu-id="b0a60-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b0a60-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="b0a60-112">OS</span><span class="sxs-lookup"><span data-stu-id="b0a60-112">PARAMETERS</span></span>

### <span data-ttu-id="b0a60-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0a60-113">-AccountName</span></span>
<span data-ttu-id="b0a60-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="b0a60-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b0a60-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0a60-115">-Confirm</span></span>
<span data-ttu-id="b0a60-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0a60-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a60-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0a60-117">-DatabaseName</span></span>
<span data-ttu-id="b0a60-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0a60-118">Database name.</span></span>

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

### <span data-ttu-id="b0a60-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a60-119">-DefaultProfile</span></span>
<span data-ttu-id="b0a60-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a60-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a60-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0a60-121">-InputObject</span></span>
<span data-ttu-id="b0a60-122">Objeto de gráfico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b0a60-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="b0a60-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0a60-123">-Name</span></span>
<span data-ttu-id="b0a60-124">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="b0a60-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b0a60-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b0a60-125">-ParentObject</span></span>
<span data-ttu-id="b0a60-126">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b0a60-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b0a60-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a60-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0a60-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0a60-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b0a60-129">-Throughputtype</span><span class="sxs-lookup"><span data-stu-id="b0a60-129">-ThroughputType</span></span>
<span data-ttu-id="b0a60-130">Tipo de produtividade para migração.</span><span class="sxs-lookup"><span data-stu-id="b0a60-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="b0a60-131">Os valores possíveis são: autoescala, manual.</span><span class="sxs-lookup"><span data-stu-id="b0a60-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="b0a60-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a60-132">-WhatIf</span></span>
<span data-ttu-id="b0a60-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0a60-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0a60-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0a60-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0a60-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a60-135">CommonParameters</span></span>
<span data-ttu-id="b0a60-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a60-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a60-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0a60-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a60-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0a60-138">INPUTS</span></span>

### <span data-ttu-id="b0a60-139">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b0a60-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="b0a60-140">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b0a60-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="b0a60-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0a60-141">OUTPUTS</span></span>

### <span data-ttu-id="b0a60-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b0a60-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b0a60-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0a60-143">NOTES</span></span>

## <span data-ttu-id="b0a60-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0a60-144">RELATED LINKS</span></span>
