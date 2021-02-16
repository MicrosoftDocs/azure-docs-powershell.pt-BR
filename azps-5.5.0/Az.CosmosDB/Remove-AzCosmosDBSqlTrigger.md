---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117775"
---
# <span data-ttu-id="b3cc5-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="b3cc5-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="b3cc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cc5-103">Exclui o Gatilho Sql Do Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="b3cc5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3cc5-104">SYNTAX</span></span>

### <span data-ttu-id="b3cc5-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3cc5-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3cc5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3cc5-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3cc5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3cc5-107">DESCRIPTION</span></span>
<span data-ttu-id="b3cc5-108">O cmdlet **Remove-AzCosmosDBSqlTrigroup** exclui o Gatilho Sql Sql do Sql correspondente ao ResourceGroupName, AccountName e DatabaseName determinados.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="b3cc5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b3cc5-109">EXAMPLES</span></span>

### <span data-ttu-id="b3cc5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b3cc5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="b3cc5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3cc5-111">PARAMETERS</span></span>

### <span data-ttu-id="b3cc5-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="b3cc5-112">-AccountName</span></span>
<span data-ttu-id="b3cc5-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b3cc5-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b3cc5-114">-Confirm</span></span>
<span data-ttu-id="b3cc5-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3cc5-116">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="b3cc5-116">-ContainerName</span></span>
<span data-ttu-id="b3cc5-117">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-117">Container name.</span></span>

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

### <span data-ttu-id="b3cc5-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="b3cc5-118">-DatabaseName</span></span>
<span data-ttu-id="b3cc5-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-119">Database name.</span></span>

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

### <span data-ttu-id="b3cc5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cc5-120">-DefaultProfile</span></span>
<span data-ttu-id="b3cc5-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3cc5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3cc5-122">-InputObject</span></span>
<span data-ttu-id="b3cc5-123">Objeto de gatilho sql</span><span class="sxs-lookup"><span data-stu-id="b3cc5-123">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cc5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3cc5-124">-Name</span></span>
<span data-ttu-id="b3cc5-125">Nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-125">Trigger name.</span></span>

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

### <span data-ttu-id="b3cc5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3cc5-126">-PassThru</span></span>
<span data-ttu-id="b3cc5-127">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b3cc5-128">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b3cc5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3cc5-129">-ResourceGroupName</span></span>
<span data-ttu-id="b3cc5-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b3cc5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3cc5-131">-WhatIf</span></span>
<span data-ttu-id="b3cc5-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3cc5-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3cc5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cc5-134">CommonParameters</span></span>
<span data-ttu-id="b3cc5-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cc5-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3cc5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cc5-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="b3cc5-137">INPUTS</span></span>

### <span data-ttu-id="b3cc5-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b3cc5-138">None</span></span>

## <span data-ttu-id="b3cc5-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="b3cc5-139">OUTPUTS</span></span>

### <span data-ttu-id="b3cc5-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b3cc5-140">System.Void</span></span>

### <span data-ttu-id="b3cc5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3cc5-141">System.Boolean</span></span>

## <span data-ttu-id="b3cc5-142">Notas</span><span class="sxs-lookup"><span data-stu-id="b3cc5-142">NOTES</span></span>

## <span data-ttu-id="b3cc5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3cc5-143">RELATED LINKS</span></span>
