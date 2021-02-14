---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116453"
---
# <span data-ttu-id="280b7-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="280b7-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="280b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="280b7-102">SYNOPSIS</span></span>
<span data-ttu-id="280b7-103">Exclui uma Tabela DesarmadoDb.</span><span class="sxs-lookup"><span data-stu-id="280b7-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="280b7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="280b7-104">SYNTAX</span></span>

### <span data-ttu-id="280b7-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="280b7-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="280b7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="280b7-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="280b7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="280b7-107">DESCRIPTION</span></span>
<span data-ttu-id="280b7-108">A **Tabela Remove-AzCosmosDBCasstable** exclui uma Tabela DesarmadoDb.</span><span class="sxs-lookup"><span data-stu-id="280b7-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="280b7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="280b7-109">EXAMPLES</span></span>

### <span data-ttu-id="280b7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="280b7-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="280b7-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="280b7-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="280b7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="280b7-112">PARAMETERS</span></span>

### <span data-ttu-id="280b7-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="280b7-113">-AccountName</span></span>
<span data-ttu-id="280b7-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="280b7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="280b7-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="280b7-115">-Confirm</span></span>
<span data-ttu-id="280b7-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="280b7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="280b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280b7-117">-DefaultProfile</span></span>
<span data-ttu-id="280b7-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="280b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="280b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="280b7-119">-InputObject</span></span>
<span data-ttu-id="280b7-120">Objeto Table Desarmado.</span><span class="sxs-lookup"><span data-stu-id="280b7-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="280b7-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="280b7-121">-KeyspaceName</span></span>
<span data-ttu-id="280b7-122">Nome do Espaço de Teclas Descaroçador.</span><span class="sxs-lookup"><span data-stu-id="280b7-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="280b7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="280b7-123">-Name</span></span>
<span data-ttu-id="280b7-124">Nome da tabela Desarmá.</span><span class="sxs-lookup"><span data-stu-id="280b7-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="280b7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="280b7-125">-PassThru</span></span>
<span data-ttu-id="280b7-126">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="280b7-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="280b7-127">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="280b7-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="280b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="280b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="280b7-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="280b7-129">Name of resource group.</span></span>

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

### <span data-ttu-id="280b7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="280b7-130">-WhatIf</span></span>
<span data-ttu-id="280b7-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="280b7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="280b7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="280b7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="280b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280b7-133">CommonParameters</span></span>
<span data-ttu-id="280b7-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="280b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280b7-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="280b7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280b7-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="280b7-136">INPUTS</span></span>

### <span data-ttu-id="280b7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCasstableGetResults</span><span class="sxs-lookup"><span data-stu-id="280b7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="280b7-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="280b7-138">OUTPUTS</span></span>

### <span data-ttu-id="280b7-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="280b7-139">System.Void</span></span>

### <span data-ttu-id="280b7-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="280b7-140">System.Boolean</span></span>

## <span data-ttu-id="280b7-141">Notas</span><span class="sxs-lookup"><span data-stu-id="280b7-141">NOTES</span></span>

## <span data-ttu-id="280b7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="280b7-142">RELATED LINKS</span></span>
