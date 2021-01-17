---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430088"
---
# <span data-ttu-id="6e505-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="6e505-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="6e505-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e505-102">SYNOPSIS</span></span>
<span data-ttu-id="6e505-103">Obtém a taxa de transferência de um gráfico de Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6e505-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="6e505-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e505-104">SYNTAX</span></span>

### <span data-ttu-id="6e505-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e505-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e505-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e505-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e505-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e505-107">DESCRIPTION</span></span>
<span data-ttu-id="6e505-108">O cmdlet **Get-AzCosmosDBGremlinGraphThroughput** Obtém a taxa de transferência de um gráfico de Gremlin de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6e505-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="6e505-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e505-109">EXAMPLES</span></span>

### <span data-ttu-id="6e505-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e505-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="6e505-111">OS</span><span class="sxs-lookup"><span data-stu-id="6e505-111">PARAMETERS</span></span>

### <span data-ttu-id="6e505-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e505-112">-AccountName</span></span>
<span data-ttu-id="6e505-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="6e505-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6e505-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e505-114">-Confirm</span></span>
<span data-ttu-id="6e505-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e505-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e505-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e505-116">-DatabaseName</span></span>
<span data-ttu-id="6e505-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6e505-117">Database name.</span></span>

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

### <span data-ttu-id="6e505-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e505-118">-DefaultProfile</span></span>
<span data-ttu-id="6e505-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e505-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e505-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e505-120">-InputObject</span></span>
<span data-ttu-id="6e505-121">Objeto de gráfico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="6e505-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e505-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e505-122">-Name</span></span>
<span data-ttu-id="6e505-123">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="6e505-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="6e505-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e505-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e505-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e505-125">Name of resource group.</span></span>

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

### <span data-ttu-id="6e505-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e505-126">-WhatIf</span></span>
<span data-ttu-id="6e505-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e505-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e505-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e505-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e505-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e505-129">CommonParameters</span></span>
<span data-ttu-id="6e505-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e505-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e505-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e505-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e505-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e505-132">INPUTS</span></span>

### <span data-ttu-id="6e505-133">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="6e505-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="6e505-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e505-134">OUTPUTS</span></span>

### <span data-ttu-id="6e505-135">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6e505-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6e505-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e505-136">NOTES</span></span>

## <span data-ttu-id="6e505-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e505-137">RELATED LINKS</span></span>
