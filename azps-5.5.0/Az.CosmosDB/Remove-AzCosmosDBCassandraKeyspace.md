---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116456"
---
# <span data-ttu-id="e4c2d-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="e4c2d-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="e4c2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c2d-103">Exclui um Espaço de Keyspace da CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="e4c2d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4c2d-104">SYNTAX</span></span>

### <span data-ttu-id="e4c2d-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4c2d-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4c2d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4c2d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4c2d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4c2d-107">DESCRIPTION</span></span>
<span data-ttu-id="e4c2d-108">O cmdlet **Remove-AzCosmosDBCasskeyspace** exclui um Espaço de Keyspace existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="e4c2d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4c2d-109">EXAMPLES</span></span>

### <span data-ttu-id="e4c2d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4c2d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="e4c2d-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é verdadeiro se a exclusão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="e4c2d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4c2d-112">PARAMETERS</span></span>

### <span data-ttu-id="e4c2d-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="e4c2d-113">-AccountName</span></span>
<span data-ttu-id="e4c2d-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e4c2d-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e4c2d-115">-Confirm</span></span>
<span data-ttu-id="e4c2d-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c2d-117">-DefaultProfile</span></span>
<span data-ttu-id="e4c2d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c2d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4c2d-119">-InputObject</span></span>
<span data-ttu-id="e4c2d-120">Objeto Desarmado Keyspace.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="e4c2d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4c2d-121">-Name</span></span>
<span data-ttu-id="e4c2d-122">Nome do Espaço de Teclas Denúm.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="e4c2d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4c2d-123">-PassThru</span></span>
<span data-ttu-id="e4c2d-124">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e4c2d-125">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e4c2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4c2d-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-127">Name of resource group.</span></span>

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

### <span data-ttu-id="e4c2d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c2d-128">-WhatIf</span></span>
<span data-ttu-id="e4c2d-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c2d-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c2d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c2d-131">CommonParameters</span></span>
<span data-ttu-id="e4c2d-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c2d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c2d-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4c2d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c2d-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4c2d-134">INPUTS</span></span>

### <span data-ttu-id="e4c2d-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCasskeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e4c2d-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e4c2d-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4c2d-136">OUTPUTS</span></span>

### <span data-ttu-id="e4c2d-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="e4c2d-137">System.Void</span></span>

### <span data-ttu-id="e4c2d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4c2d-138">System.Boolean</span></span>

## <span data-ttu-id="e4c2d-139">Notas</span><span class="sxs-lookup"><span data-stu-id="e4c2d-139">NOTES</span></span>

## <span data-ttu-id="e4c2d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4c2d-140">RELATED LINKS</span></span>
