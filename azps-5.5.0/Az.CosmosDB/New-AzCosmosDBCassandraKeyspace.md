---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112047"
---
# <span data-ttu-id="4538d-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="4538d-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="4538d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4538d-102">SYNOPSIS</span></span>
<span data-ttu-id="4538d-103">Cria um novoSpace de Keyspace da YorkDB.</span><span class="sxs-lookup"><span data-stu-id="4538d-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4538d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4538d-104">SYNTAX</span></span>

### <span data-ttu-id="4538d-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4538d-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4538d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4538d-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4538d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4538d-107">DESCRIPTION</span></span>
<span data-ttu-id="4538d-108">Cria um novoSpace de Keyspace da YorkDB.</span><span class="sxs-lookup"><span data-stu-id="4538d-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4538d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4538d-109">EXAMPLES</span></span>

### <span data-ttu-id="4538d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4538d-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="4538d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4538d-111">PARAMETERS</span></span>

### <span data-ttu-id="4538d-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="4538d-112">-AccountName</span></span>
<span data-ttu-id="4538d-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="4538d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4538d-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4538d-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4538d-115">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="4538d-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4538d-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4538d-116">-Confirm</span></span>
<span data-ttu-id="4538d-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4538d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4538d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4538d-118">-DefaultProfile</span></span>
<span data-ttu-id="4538d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4538d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4538d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4538d-120">-Name</span></span>
<span data-ttu-id="4538d-121">Nome do Espaço de Teclas Descaroçador.</span><span class="sxs-lookup"><span data-stu-id="4538d-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4538d-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4538d-122">-ParentObject</span></span>
<span data-ttu-id="4538d-123">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="4538d-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4538d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4538d-124">-ResourceGroupName</span></span>
<span data-ttu-id="4538d-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4538d-125">Name of resource group.</span></span>

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

### <span data-ttu-id="4538d-126">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="4538d-126">-Throughput</span></span>
<span data-ttu-id="4538d-127">A produtividade de Guida Keyspace (RU/s).</span><span class="sxs-lookup"><span data-stu-id="4538d-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="4538d-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="4538d-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4538d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4538d-129">-WhatIf</span></span>
<span data-ttu-id="4538d-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4538d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4538d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4538d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4538d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4538d-132">CommonParameters</span></span>
<span data-ttu-id="4538d-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4538d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4538d-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4538d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4538d-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="4538d-135">INPUTS</span></span>

### <span data-ttu-id="4538d-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4538d-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4538d-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="4538d-137">OUTPUTS</span></span>

### <span data-ttu-id="4538d-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4538d-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="4538d-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="4538d-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="4538d-140">Notas</span><span class="sxs-lookup"><span data-stu-id="4538d-140">NOTES</span></span>

## <span data-ttu-id="4538d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4538d-141">RELATED LINKS</span></span>
