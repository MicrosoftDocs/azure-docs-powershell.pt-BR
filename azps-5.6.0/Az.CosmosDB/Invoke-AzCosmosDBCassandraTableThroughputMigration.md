---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: 65b1cbaebdf4118b5e22a7d1f9672273281ba55b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890641"
---
# <span data-ttu-id="ee07a-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="ee07a-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="ee07a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee07a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee07a-103">Use isso para migrar a produtividade de escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="ee07a-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="ee07a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ee07a-104">SYNTAX</span></span>

### <span data-ttu-id="ee07a-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee07a-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07a-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee07a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee07a-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee07a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ee07a-108">DESCRIPTION</span></span>
<span data-ttu-id="ee07a-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="ee07a-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="ee07a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee07a-110">EXAMPLES</span></span>

### <span data-ttu-id="ee07a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee07a-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="ee07a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ee07a-112">PARAMETERS</span></span>

### <span data-ttu-id="ee07a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ee07a-113">-AccountName</span></span>
<span data-ttu-id="ee07a-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="ee07a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ee07a-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee07a-115">-Confirm</span></span>
<span data-ttu-id="ee07a-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee07a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee07a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee07a-117">-DefaultProfile</span></span>
<span data-ttu-id="ee07a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee07a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee07a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee07a-119">-InputObject</span></span>
<span data-ttu-id="ee07a-120">Objeto Table de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ee07a-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee07a-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="ee07a-121">-KeyspaceName</span></span>
<span data-ttu-id="ee07a-122">Nome do Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ee07a-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="ee07a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ee07a-123">-Name</span></span>
<span data-ttu-id="ee07a-124">Nome da tabela de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ee07a-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="ee07a-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ee07a-125">-ParentObject</span></span>
<span data-ttu-id="ee07a-126">Objeto Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ee07a-126">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee07a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee07a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ee07a-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee07a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ee07a-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="ee07a-129">-ThroughputType</span></span>
<span data-ttu-id="ee07a-130">Tipo de transferência para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="ee07a-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="ee07a-131">Os valores possíveis são: Escala automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="ee07a-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="ee07a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee07a-132">-WhatIf</span></span>
<span data-ttu-id="ee07a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee07a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee07a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee07a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee07a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee07a-135">CommonParameters</span></span>
<span data-ttu-id="ee07a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee07a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee07a-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee07a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee07a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee07a-138">INPUTS</span></span>

### <span data-ttu-id="ee07a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="ee07a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="ee07a-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="ee07a-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="ee07a-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ee07a-141">OUTPUTS</span></span>

### <span data-ttu-id="ee07a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ee07a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ee07a-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="ee07a-143">NOTES</span></span>

## <span data-ttu-id="ee07a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee07a-144">RELATED LINKS</span></span>
