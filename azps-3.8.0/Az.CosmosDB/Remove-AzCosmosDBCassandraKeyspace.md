---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943713"
---
# <span data-ttu-id="944fd-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="944fd-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="944fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="944fd-102">SYNOPSIS</span></span>
<span data-ttu-id="944fd-103">Exclui um espaço de CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="944fd-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="944fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="944fd-104">SYNTAX</span></span>

### <span data-ttu-id="944fd-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="944fd-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="944fd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="944fd-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="944fd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="944fd-107">DESCRIPTION</span></span>
<span data-ttu-id="944fd-108">O cmdlet **Remove-AzCosmosDBCassandraKeyspace** exclui um espaço de keyCassandra existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="944fd-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="944fd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="944fd-109">EXAMPLES</span></span>

### <span data-ttu-id="944fd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="944fd-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="944fd-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que será true se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="944fd-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="944fd-112">OS</span><span class="sxs-lookup"><span data-stu-id="944fd-112">PARAMETERS</span></span>

### <span data-ttu-id="944fd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="944fd-113">-AccountName</span></span>
<span data-ttu-id="944fd-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="944fd-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="944fd-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="944fd-115">-Confirm</span></span>
<span data-ttu-id="944fd-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="944fd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="944fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944fd-117">-DefaultProfile</span></span>
<span data-ttu-id="944fd-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="944fd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="944fd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="944fd-119">-InputObject</span></span>
<span data-ttu-id="944fd-120">Objeto de espaço Cassandra.</span><span class="sxs-lookup"><span data-stu-id="944fd-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="944fd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="944fd-121">-Name</span></span>
<span data-ttu-id="944fd-122">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="944fd-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="944fd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="944fd-123">-PassThru</span></span>
<span data-ttu-id="944fd-124">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="944fd-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="944fd-125">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="944fd-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="944fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="944fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="944fd-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="944fd-127">Name of resource group.</span></span>

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

### <span data-ttu-id="944fd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="944fd-128">-WhatIf</span></span>
<span data-ttu-id="944fd-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="944fd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="944fd-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="944fd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="944fd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944fd-131">CommonParameters</span></span>
<span data-ttu-id="944fd-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="944fd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944fd-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="944fd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944fd-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="944fd-134">INPUTS</span></span>

### <span data-ttu-id="944fd-135">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="944fd-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="944fd-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="944fd-136">OUTPUTS</span></span>

### <span data-ttu-id="944fd-137">System. void</span><span class="sxs-lookup"><span data-stu-id="944fd-137">System.Void</span></span>

### <span data-ttu-id="944fd-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="944fd-138">System.Boolean</span></span>

## <span data-ttu-id="944fd-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="944fd-139">NOTES</span></span>

## <span data-ttu-id="944fd-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="944fd-140">RELATED LINKS</span></span>
