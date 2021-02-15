---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112052"
---
# <span data-ttu-id="5edd3-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="5edd3-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="5edd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5edd3-102">SYNOPSIS</span></span>
<span data-ttu-id="5edd3-103">Use isso para migrar a produtividade em escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="5edd3-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="5edd3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5edd3-104">SYNTAX</span></span>

### <span data-ttu-id="5edd3-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5edd3-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5edd3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edd3-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5edd3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edd3-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5edd3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5edd3-108">DESCRIPTION</span></span>
<span data-ttu-id="5edd3-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="5edd3-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="5edd3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5edd3-110">EXAMPLES</span></span>

### <span data-ttu-id="5edd3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5edd3-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="5edd3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5edd3-112">PARAMETERS</span></span>

### <span data-ttu-id="5edd3-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="5edd3-113">-AccountName</span></span>
<span data-ttu-id="5edd3-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="5edd3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5edd3-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5edd3-115">-Confirm</span></span>
<span data-ttu-id="5edd3-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5edd3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5edd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edd3-117">-DefaultProfile</span></span>
<span data-ttu-id="5edd3-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5edd3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5edd3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5edd3-119">-InputObject</span></span>
<span data-ttu-id="5edd3-120">Objeto Desa Keyspace.</span><span class="sxs-lookup"><span data-stu-id="5edd3-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="5edd3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5edd3-121">-Name</span></span>
<span data-ttu-id="5edd3-122">Nome do Espaço de Teclas Descaroçador.</span><span class="sxs-lookup"><span data-stu-id="5edd3-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5edd3-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5edd3-123">-ParentObject</span></span>
<span data-ttu-id="5edd3-124">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="5edd3-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5edd3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5edd3-125">-ResourceGroupName</span></span>
<span data-ttu-id="5edd3-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5edd3-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5edd3-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="5edd3-127">-ThroughputType</span></span>
<span data-ttu-id="5edd3-128">Tipo de produtividade para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="5edd3-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="5edd3-129">Os valores possíveis são: Escala Automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="5edd3-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="5edd3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5edd3-130">-WhatIf</span></span>
<span data-ttu-id="5edd3-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5edd3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5edd3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edd3-133">CommonParameters</span></span>
<span data-ttu-id="5edd3-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5edd3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edd3-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5edd3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edd3-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="5edd3-136">INPUTS</span></span>

### <span data-ttu-id="5edd3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="5edd3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="5edd3-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5edd3-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5edd3-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="5edd3-139">OUTPUTS</span></span>

### <span data-ttu-id="5edd3-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5edd3-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5edd3-141">Notas</span><span class="sxs-lookup"><span data-stu-id="5edd3-141">NOTES</span></span>

## <span data-ttu-id="5edd3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5edd3-142">RELATED LINKS</span></span>
