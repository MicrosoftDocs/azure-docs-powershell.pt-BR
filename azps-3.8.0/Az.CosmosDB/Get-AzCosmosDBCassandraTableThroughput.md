---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944126"
---
# <span data-ttu-id="2a0d3-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="2a0d3-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="2a0d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0d3-103">Obtém o valor de produtividade da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="2a0d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a0d3-104">SYNTAX</span></span>

### <span data-ttu-id="2a0d3-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a0d3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a0d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a0d3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a0d3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a0d3-107">DESCRIPTION</span></span>
<span data-ttu-id="2a0d3-108">O cmdlet **Get-AzCosmosDBCassandraTableThroughput** Obtém o objeto de taxa de transferência correspondente a um espaço de espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="2a0d3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a0d3-109">EXAMPLES</span></span>

### <span data-ttu-id="2a0d3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a0d3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="2a0d3-111">OS</span><span class="sxs-lookup"><span data-stu-id="2a0d3-111">PARAMETERS</span></span>

### <span data-ttu-id="2a0d3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2a0d3-112">-AccountName</span></span>
<span data-ttu-id="2a0d3-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2a0d3-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a0d3-114">-Confirm</span></span>
<span data-ttu-id="2a0d3-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a0d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0d3-116">-DefaultProfile</span></span>
<span data-ttu-id="2a0d3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a0d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a0d3-118">-InputObject</span></span>
<span data-ttu-id="2a0d3-119">Objeto da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="2a0d3-120">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="2a0d3-120">-KeyspaceName</span></span>
<span data-ttu-id="2a0d3-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-121">Database name.</span></span>

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

### <span data-ttu-id="2a0d3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a0d3-122">-Name</span></span>
<span data-ttu-id="2a0d3-123">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="2a0d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a0d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a0d3-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2a0d3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0d3-126">-WhatIf</span></span>
<span data-ttu-id="2a0d3-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a0d3-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a0d3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0d3-129">CommonParameters</span></span>
<span data-ttu-id="2a0d3-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0d3-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a0d3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0d3-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a0d3-132">INPUTS</span></span>

### <span data-ttu-id="2a0d3-133">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="2a0d3-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="2a0d3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a0d3-134">OUTPUTS</span></span>

### <span data-ttu-id="2a0d3-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2a0d3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2a0d3-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a0d3-136">NOTES</span></span>

## <span data-ttu-id="2a0d3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a0d3-137">RELATED LINKS</span></span>
