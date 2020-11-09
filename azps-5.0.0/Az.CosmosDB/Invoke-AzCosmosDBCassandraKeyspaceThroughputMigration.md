---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281365"
---
# <span data-ttu-id="88446-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="88446-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="88446-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88446-102">SYNOPSIS</span></span>
<span data-ttu-id="88446-103">Use isso para migrar a produtividade de AutoEscala para a taxa de transferência manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="88446-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="88446-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88446-104">SYNTAX</span></span>

### <span data-ttu-id="88446-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="88446-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88446-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88446-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88446-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88446-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88446-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88446-108">DESCRIPTION</span></span>
<span data-ttu-id="88446-109">O parâmetro ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="88446-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="88446-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88446-110">EXAMPLES</span></span>

### <span data-ttu-id="88446-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88446-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="88446-112">OS</span><span class="sxs-lookup"><span data-stu-id="88446-112">PARAMETERS</span></span>

### <span data-ttu-id="88446-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88446-113">-AccountName</span></span>
<span data-ttu-id="88446-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="88446-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="88446-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88446-115">-Confirm</span></span>
<span data-ttu-id="88446-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88446-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88446-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88446-117">-DefaultProfile</span></span>
<span data-ttu-id="88446-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88446-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88446-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88446-119">-InputObject</span></span>
<span data-ttu-id="88446-120">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="88446-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88446-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="88446-121">-Name</span></span>
<span data-ttu-id="88446-122">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="88446-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="88446-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="88446-123">-ParentObject</span></span>
<span data-ttu-id="88446-124">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="88446-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="88446-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88446-125">-ResourceGroupName</span></span>
<span data-ttu-id="88446-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="88446-126">Name of resource group.</span></span>

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

### <span data-ttu-id="88446-127">-Throughputtype</span><span class="sxs-lookup"><span data-stu-id="88446-127">-ThroughputType</span></span>
<span data-ttu-id="88446-128">Tipo de produtividade para migração.</span><span class="sxs-lookup"><span data-stu-id="88446-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="88446-129">Os valores possíveis são: autoescala, manual.</span><span class="sxs-lookup"><span data-stu-id="88446-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="88446-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88446-130">-WhatIf</span></span>
<span data-ttu-id="88446-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88446-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88446-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88446-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88446-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88446-133">CommonParameters</span></span>
<span data-ttu-id="88446-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88446-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88446-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88446-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88446-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88446-136">INPUTS</span></span>

### <span data-ttu-id="88446-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="88446-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="88446-138">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="88446-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="88446-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88446-139">OUTPUTS</span></span>

### <span data-ttu-id="88446-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="88446-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="88446-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88446-141">NOTES</span></span>

## <span data-ttu-id="88446-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88446-142">RELATED LINKS</span></span>
