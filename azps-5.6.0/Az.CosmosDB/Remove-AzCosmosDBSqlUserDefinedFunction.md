---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 7e7ffd7c06217b4e2d12aaf75684c85f8ab12e9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889293"
---
# <span data-ttu-id="b8459-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="b8459-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="b8459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8459-102">SYNOPSIS</span></span>
<span data-ttu-id="b8459-103">Exclui o UserDefinedFunction do Sql Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b8459-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="b8459-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8459-104">SYNTAX</span></span>

### <span data-ttu-id="b8459-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8459-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8459-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8459-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8459-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8459-107">DESCRIPTION</span></span>
<span data-ttu-id="b8459-108">O cmdlet **Remove-AzCosmosDBSqlUserDefinedFunction** exclui o UserDefinedFunction sql do CosmosDB correspondente ao ResourceGroupName, AccountName e DatabaseName determinado.</span><span class="sxs-lookup"><span data-stu-id="b8459-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="b8459-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8459-109">EXAMPLES</span></span>

### <span data-ttu-id="b8459-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8459-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="b8459-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8459-111">PARAMETERS</span></span>

### <span data-ttu-id="b8459-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b8459-112">-AccountName</span></span>
<span data-ttu-id="b8459-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="b8459-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b8459-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8459-114">-Confirm</span></span>
<span data-ttu-id="b8459-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8459-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8459-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b8459-116">-ContainerName</span></span>
<span data-ttu-id="b8459-117">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="b8459-117">Container name.</span></span>

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

### <span data-ttu-id="b8459-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8459-118">-DatabaseName</span></span>
<span data-ttu-id="b8459-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b8459-119">Database name.</span></span>

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

### <span data-ttu-id="b8459-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8459-120">-DefaultProfile</span></span>
<span data-ttu-id="b8459-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8459-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8459-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8459-122">-InputObject</span></span>
<span data-ttu-id="b8459-123">Objeto de função definida pelo usuário sql</span><span class="sxs-lookup"><span data-stu-id="b8459-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8459-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b8459-124">-Name</span></span>
<span data-ttu-id="b8459-125">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b8459-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="b8459-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8459-126">-PassThru</span></span>
<span data-ttu-id="b8459-127">Para ser definido como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="b8459-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b8459-128">A saída será true se a operação tiver sido bem-sucedida e um erro for lançado, caso não seja.</span><span class="sxs-lookup"><span data-stu-id="b8459-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b8459-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8459-129">-ResourceGroupName</span></span>
<span data-ttu-id="b8459-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8459-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b8459-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8459-131">-WhatIf</span></span>
<span data-ttu-id="b8459-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8459-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8459-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8459-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8459-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8459-134">CommonParameters</span></span>
<span data-ttu-id="b8459-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8459-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8459-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8459-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8459-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8459-137">INPUTS</span></span>

### <span data-ttu-id="b8459-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b8459-138">None</span></span>

## <span data-ttu-id="b8459-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8459-139">OUTPUTS</span></span>

### <span data-ttu-id="b8459-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b8459-140">System.Void</span></span>

### <span data-ttu-id="b8459-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8459-141">System.Boolean</span></span>

## <span data-ttu-id="b8459-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8459-142">NOTES</span></span>

## <span data-ttu-id="b8459-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8459-143">RELATED LINKS</span></span>
