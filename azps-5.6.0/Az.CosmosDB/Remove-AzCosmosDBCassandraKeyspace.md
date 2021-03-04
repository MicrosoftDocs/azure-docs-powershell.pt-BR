---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 849f716787c01c5810af74c37e97bbdb0bd2ef13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885730"
---
# <span data-ttu-id="bb224-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="bb224-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="bb224-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb224-102">SYNOPSIS</span></span>
<span data-ttu-id="bb224-103">Exclui um Espaço-Chave de Cassandra de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="bb224-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="bb224-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb224-104">SYNTAX</span></span>

### <span data-ttu-id="bb224-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb224-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb224-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb224-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb224-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb224-107">DESCRIPTION</span></span>
<span data-ttu-id="bb224-108">O cmdlet **Remove-AzCosmosDBCassandraKeyspace** exclui um Espaço-Chave existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="bb224-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="bb224-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb224-109">EXAMPLES</span></span>

### <span data-ttu-id="bb224-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb224-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="bb224-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é true se a exclusão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bb224-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="bb224-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb224-112">PARAMETERS</span></span>

### <span data-ttu-id="bb224-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bb224-113">-AccountName</span></span>
<span data-ttu-id="bb224-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="bb224-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bb224-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb224-115">-Confirm</span></span>
<span data-ttu-id="bb224-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb224-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb224-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb224-117">-DefaultProfile</span></span>
<span data-ttu-id="bb224-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb224-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb224-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb224-119">-InputObject</span></span>
<span data-ttu-id="bb224-120">Objeto Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bb224-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="bb224-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bb224-121">-Name</span></span>
<span data-ttu-id="bb224-122">Nome do Keyspace de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bb224-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="bb224-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb224-123">-PassThru</span></span>
<span data-ttu-id="bb224-124">Para ser definido como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="bb224-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="bb224-125">A saída será true se a operação tiver sido bem-sucedida e um erro for lançado, caso não seja.</span><span class="sxs-lookup"><span data-stu-id="bb224-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb224-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb224-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb224-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb224-127">Name of resource group.</span></span>

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

### <span data-ttu-id="bb224-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb224-128">-WhatIf</span></span>
<span data-ttu-id="bb224-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb224-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb224-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb224-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb224-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb224-131">CommonParameters</span></span>
<span data-ttu-id="bb224-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb224-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb224-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb224-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb224-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb224-134">INPUTS</span></span>

### <span data-ttu-id="bb224-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="bb224-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="bb224-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb224-136">OUTPUTS</span></span>

### <span data-ttu-id="bb224-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="bb224-137">System.Void</span></span>

### <span data-ttu-id="bb224-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb224-138">System.Boolean</span></span>

## <span data-ttu-id="bb224-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb224-139">NOTES</span></span>

## <span data-ttu-id="bb224-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb224-140">RELATED LINKS</span></span>
