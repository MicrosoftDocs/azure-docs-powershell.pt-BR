---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: 4e17e8fc2ee3b9fa82881387fa4422616b25551c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115935"
---
# <span data-ttu-id="66052-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="66052-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="66052-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66052-102">SYNOPSIS</span></span>
<span data-ttu-id="66052-103">Use-a para migrar a produtividade em escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="66052-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="66052-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66052-104">SYNTAX</span></span>

### <span data-ttu-id="66052-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66052-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66052-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66052-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66052-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66052-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66052-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="66052-108">DESCRIPTION</span></span>
<span data-ttu-id="66052-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="66052-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="66052-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66052-110">EXAMPLES</span></span>

### <span data-ttu-id="66052-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66052-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="66052-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66052-112">PARAMETERS</span></span>

### <span data-ttu-id="66052-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="66052-113">-AccountName</span></span>
<span data-ttu-id="66052-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="66052-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66052-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="66052-115">-Confirm</span></span>
<span data-ttu-id="66052-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66052-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66052-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66052-117">-DefaultProfile</span></span>
<span data-ttu-id="66052-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66052-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66052-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66052-119">-InputObject</span></span>
<span data-ttu-id="66052-120">Objeto Table Desarmado.</span><span class="sxs-lookup"><span data-stu-id="66052-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="66052-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="66052-121">-KeyspaceName</span></span>
<span data-ttu-id="66052-122">Nome do Espaço de Teclas Descaroçador.</span><span class="sxs-lookup"><span data-stu-id="66052-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="66052-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="66052-123">-Name</span></span>
<span data-ttu-id="66052-124">Nome da tabela Desarmá.</span><span class="sxs-lookup"><span data-stu-id="66052-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="66052-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="66052-125">-ParentObject</span></span>
<span data-ttu-id="66052-126">Objeto Desa Keyspace.</span><span class="sxs-lookup"><span data-stu-id="66052-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="66052-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66052-127">-ResourceGroupName</span></span>
<span data-ttu-id="66052-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66052-128">Name of resource group.</span></span>

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

### <span data-ttu-id="66052-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="66052-129">-ThroughputType</span></span>
<span data-ttu-id="66052-130">Tipo de produtividade para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="66052-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="66052-131">Os valores possíveis são: Escala Automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="66052-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="66052-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66052-132">-WhatIf</span></span>
<span data-ttu-id="66052-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="66052-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66052-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66052-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66052-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66052-135">CommonParameters</span></span>
<span data-ttu-id="66052-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66052-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66052-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66052-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66052-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="66052-138">INPUTS</span></span>

### <span data-ttu-id="66052-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="66052-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="66052-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCasstableGetResults</span><span class="sxs-lookup"><span data-stu-id="66052-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="66052-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="66052-141">OUTPUTS</span></span>

### <span data-ttu-id="66052-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="66052-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="66052-143">Notas</span><span class="sxs-lookup"><span data-stu-id="66052-143">NOTES</span></span>

## <span data-ttu-id="66052-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66052-144">RELATED LINKS</span></span>
