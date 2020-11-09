---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281364"
---
# <span data-ttu-id="c490f-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c490f-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="c490f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c490f-102">SYNOPSIS</span></span>
<span data-ttu-id="c490f-103">Use isso para migrar a produtividade de AutoEscala para a taxa de transferência manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="c490f-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c490f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c490f-104">SYNTAX</span></span>

### <span data-ttu-id="c490f-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c490f-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c490f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c490f-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c490f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c490f-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c490f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c490f-108">DESCRIPTION</span></span>
<span data-ttu-id="c490f-109">O parâmetro ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="c490f-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c490f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c490f-110">EXAMPLES</span></span>

### <span data-ttu-id="c490f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c490f-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="c490f-112">OS</span><span class="sxs-lookup"><span data-stu-id="c490f-112">PARAMETERS</span></span>

### <span data-ttu-id="c490f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c490f-113">-AccountName</span></span>
<span data-ttu-id="c490f-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c490f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c490f-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c490f-115">-Confirm</span></span>
<span data-ttu-id="c490f-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c490f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c490f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c490f-117">-DefaultProfile</span></span>
<span data-ttu-id="c490f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c490f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c490f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c490f-119">-InputObject</span></span>
<span data-ttu-id="c490f-120">Objeto da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c490f-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="c490f-121">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="c490f-121">-KeyspaceName</span></span>
<span data-ttu-id="c490f-122">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c490f-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c490f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c490f-123">-Name</span></span>
<span data-ttu-id="c490f-124">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c490f-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="c490f-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c490f-125">-ParentObject</span></span>
<span data-ttu-id="c490f-126">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="c490f-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c490f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c490f-127">-ResourceGroupName</span></span>
<span data-ttu-id="c490f-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c490f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="c490f-129">-Throughputtype</span><span class="sxs-lookup"><span data-stu-id="c490f-129">-ThroughputType</span></span>
<span data-ttu-id="c490f-130">Tipo de produtividade para migração.</span><span class="sxs-lookup"><span data-stu-id="c490f-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="c490f-131">Os valores possíveis são: autoescala, manual.</span><span class="sxs-lookup"><span data-stu-id="c490f-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="c490f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c490f-132">-WhatIf</span></span>
<span data-ttu-id="c490f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c490f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c490f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c490f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c490f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c490f-135">CommonParameters</span></span>
<span data-ttu-id="c490f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c490f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c490f-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c490f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c490f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c490f-138">INPUTS</span></span>

### <span data-ttu-id="c490f-139">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c490f-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="c490f-140">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="c490f-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="c490f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c490f-141">OUTPUTS</span></span>

### <span data-ttu-id="c490f-142">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c490f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c490f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c490f-143">NOTES</span></span>

## <span data-ttu-id="c490f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c490f-144">RELATED LINKS</span></span>
