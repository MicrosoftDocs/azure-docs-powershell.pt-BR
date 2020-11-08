---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115082"
---
# <span data-ttu-id="0f6eb-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="0f6eb-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="0f6eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6eb-103">Exclui uma tabela CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="0f6eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f6eb-104">SYNTAX</span></span>

### <span data-ttu-id="0f6eb-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0f6eb-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f6eb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f6eb-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f6eb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f6eb-107">DESCRIPTION</span></span>
<span data-ttu-id="0f6eb-108">**Remove-AzCosmosDBCassandraTable** exclui uma tabela Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="0f6eb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f6eb-109">EXAMPLES</span></span>

### <span data-ttu-id="0f6eb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f6eb-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="0f6eb-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="0f6eb-112">OS</span><span class="sxs-lookup"><span data-stu-id="0f6eb-112">PARAMETERS</span></span>

### <span data-ttu-id="0f6eb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0f6eb-113">-AccountName</span></span>
<span data-ttu-id="0f6eb-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0f6eb-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f6eb-115">-Confirm</span></span>
<span data-ttu-id="0f6eb-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f6eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6eb-117">-DefaultProfile</span></span>
<span data-ttu-id="0f6eb-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f6eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f6eb-119">-InputObject</span></span>
<span data-ttu-id="0f6eb-120">Objeto da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="0f6eb-121">-Keyspacename</span><span class="sxs-lookup"><span data-stu-id="0f6eb-121">-KeyspaceName</span></span>
<span data-ttu-id="0f6eb-122">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0f6eb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f6eb-123">-Name</span></span>
<span data-ttu-id="0f6eb-124">Nome da tabela Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="0f6eb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f6eb-125">-PassThru</span></span>
<span data-ttu-id="0f6eb-126">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="0f6eb-127">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="0f6eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f6eb-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-129">Name of resource group.</span></span>

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

### <span data-ttu-id="0f6eb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6eb-130">-WhatIf</span></span>
<span data-ttu-id="0f6eb-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f6eb-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f6eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6eb-133">CommonParameters</span></span>
<span data-ttu-id="0f6eb-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6eb-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f6eb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6eb-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f6eb-136">INPUTS</span></span>

### <span data-ttu-id="0f6eb-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="0f6eb-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="0f6eb-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f6eb-138">OUTPUTS</span></span>

### <span data-ttu-id="0f6eb-139">System. void</span><span class="sxs-lookup"><span data-stu-id="0f6eb-139">System.Void</span></span>

### <span data-ttu-id="0f6eb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f6eb-140">System.Boolean</span></span>

## <span data-ttu-id="0f6eb-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f6eb-141">NOTES</span></span>

## <span data-ttu-id="0f6eb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f6eb-142">RELATED LINKS</span></span>
