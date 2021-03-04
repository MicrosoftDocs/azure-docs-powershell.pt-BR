---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: c502040c2d4b11302c158cffb66bf6fd01e148ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891216"
---
# <span data-ttu-id="337a2-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="337a2-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="337a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="337a2-102">SYNOPSIS</span></span>
<span data-ttu-id="337a2-103">Use isso para migrar a produtividade de escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="337a2-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="337a2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="337a2-104">SYNTAX</span></span>

### <span data-ttu-id="337a2-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="337a2-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="337a2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="337a2-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="337a2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="337a2-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="337a2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="337a2-108">DESCRIPTION</span></span>
<span data-ttu-id="337a2-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="337a2-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="337a2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="337a2-110">EXAMPLES</span></span>

### <span data-ttu-id="337a2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="337a2-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="337a2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="337a2-112">PARAMETERS</span></span>

### <span data-ttu-id="337a2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="337a2-113">-AccountName</span></span>
<span data-ttu-id="337a2-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="337a2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="337a2-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="337a2-115">-Confirm</span></span>
<span data-ttu-id="337a2-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="337a2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="337a2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="337a2-117">-DatabaseName</span></span>
<span data-ttu-id="337a2-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="337a2-118">Database name.</span></span>

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

### <span data-ttu-id="337a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337a2-119">-DefaultProfile</span></span>
<span data-ttu-id="337a2-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="337a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="337a2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="337a2-121">-InputObject</span></span>
<span data-ttu-id="337a2-122">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="337a2-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="337a2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="337a2-123">-Name</span></span>
<span data-ttu-id="337a2-124">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="337a2-124">Container name.</span></span>

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

### <span data-ttu-id="337a2-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="337a2-125">-ParentObject</span></span>
<span data-ttu-id="337a2-126">Objeto Sql Database.</span><span class="sxs-lookup"><span data-stu-id="337a2-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="337a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="337a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="337a2-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="337a2-128">Name of resource group.</span></span>

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

### <span data-ttu-id="337a2-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="337a2-129">-ThroughputType</span></span>
<span data-ttu-id="337a2-130">Tipo de transferência para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="337a2-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="337a2-131">Os valores possíveis são: Escala automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="337a2-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="337a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="337a2-132">-WhatIf</span></span>
<span data-ttu-id="337a2-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="337a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="337a2-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="337a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="337a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337a2-135">CommonParameters</span></span>
<span data-ttu-id="337a2-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337a2-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="337a2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337a2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="337a2-138">INPUTS</span></span>

### <span data-ttu-id="337a2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="337a2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="337a2-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="337a2-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="337a2-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="337a2-141">OUTPUTS</span></span>

### <span data-ttu-id="337a2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="337a2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="337a2-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="337a2-143">NOTES</span></span>

## <span data-ttu-id="337a2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="337a2-144">RELATED LINKS</span></span>
