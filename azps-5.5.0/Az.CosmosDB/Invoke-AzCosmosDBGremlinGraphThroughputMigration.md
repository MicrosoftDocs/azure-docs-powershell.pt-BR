---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16817d4af40ddd27a8838f40618758686af26a58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115931"
---
# <span data-ttu-id="2e766-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="2e766-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="2e766-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e766-102">SYNOPSIS</span></span>
<span data-ttu-id="2e766-103">Use isso para migrar a produtividade em escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="2e766-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="2e766-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e766-104">SYNTAX</span></span>

### <span data-ttu-id="2e766-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2e766-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e766-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e766-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e766-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e766-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e766-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e766-108">DESCRIPTION</span></span>
<span data-ttu-id="2e766-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="2e766-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="2e766-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e766-110">EXAMPLES</span></span>

### <span data-ttu-id="2e766-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e766-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="2e766-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e766-112">PARAMETERS</span></span>

### <span data-ttu-id="2e766-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="2e766-113">-AccountName</span></span>
<span data-ttu-id="2e766-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="2e766-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2e766-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2e766-115">-Confirm</span></span>
<span data-ttu-id="2e766-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e766-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e766-117">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="2e766-117">-DatabaseName</span></span>
<span data-ttu-id="2e766-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2e766-118">Database name.</span></span>

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

### <span data-ttu-id="2e766-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e766-119">-DefaultProfile</span></span>
<span data-ttu-id="2e766-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e766-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e766-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e766-121">-InputObject</span></span>
<span data-ttu-id="2e766-122">Objeto Do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2e766-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="2e766-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e766-123">-Name</span></span>
<span data-ttu-id="2e766-124">Nome do Gráfico de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2e766-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="2e766-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e766-125">-ParentObject</span></span>
<span data-ttu-id="2e766-126">Objeto de Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="2e766-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="2e766-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e766-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e766-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e766-128">Name of resource group.</span></span>

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

### <span data-ttu-id="2e766-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="2e766-129">-ThroughputType</span></span>
<span data-ttu-id="2e766-130">Tipo de produtividade para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="2e766-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="2e766-131">Os valores possíveis são: Escala Automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="2e766-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="2e766-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e766-132">-WhatIf</span></span>
<span data-ttu-id="2e766-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2e766-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e766-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e766-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e766-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e766-135">CommonParameters</span></span>
<span data-ttu-id="2e766-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e766-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e766-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e766-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e766-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="2e766-138">INPUTS</span></span>

### <span data-ttu-id="2e766-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2e766-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="2e766-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="2e766-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="2e766-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="2e766-141">OUTPUTS</span></span>

### <span data-ttu-id="2e766-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2e766-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2e766-143">Notas</span><span class="sxs-lookup"><span data-stu-id="2e766-143">NOTES</span></span>

## <span data-ttu-id="2e766-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e766-144">RELATED LINKS</span></span>
