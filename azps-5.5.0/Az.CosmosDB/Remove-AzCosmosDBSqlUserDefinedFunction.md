---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117774"
---
# <span data-ttu-id="109a9-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="109a9-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="109a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="109a9-102">SYNOPSIS</span></span>
<span data-ttu-id="109a9-103">Exclui o Sql UserDefinedFunction do Sql.</span><span class="sxs-lookup"><span data-stu-id="109a9-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="109a9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="109a9-104">SYNTAX</span></span>

### <span data-ttu-id="109a9-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="109a9-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="109a9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="109a9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="109a9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="109a9-107">DESCRIPTION</span></span>
<span data-ttu-id="109a9-108">O cmdlet **Remove-AzCosmosDBSqlUserDefinedFunction** exclui o Sql UserDefinedFunction do Sql Sql correspondente ao resourceGroupName, AccountName e DatabaseName determinados.</span><span class="sxs-lookup"><span data-stu-id="109a9-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="109a9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="109a9-109">EXAMPLES</span></span>

### <span data-ttu-id="109a9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="109a9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="109a9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="109a9-111">PARAMETERS</span></span>

### <span data-ttu-id="109a9-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="109a9-112">-AccountName</span></span>
<span data-ttu-id="109a9-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="109a9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="109a9-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="109a9-114">-Confirm</span></span>
<span data-ttu-id="109a9-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="109a9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="109a9-116">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="109a9-116">-ContainerName</span></span>
<span data-ttu-id="109a9-117">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="109a9-117">Container name.</span></span>

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

### <span data-ttu-id="109a9-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="109a9-118">-DatabaseName</span></span>
<span data-ttu-id="109a9-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="109a9-119">Database name.</span></span>

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

### <span data-ttu-id="109a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="109a9-120">-DefaultProfile</span></span>
<span data-ttu-id="109a9-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="109a9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="109a9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="109a9-122">-InputObject</span></span>
<span data-ttu-id="109a9-123">Objeto de função definida pelo usuário sql</span><span class="sxs-lookup"><span data-stu-id="109a9-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="109a9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="109a9-124">-Name</span></span>
<span data-ttu-id="109a9-125">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="109a9-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="109a9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="109a9-126">-PassThru</span></span>
<span data-ttu-id="109a9-127">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="109a9-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="109a9-128">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="109a9-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="109a9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="109a9-129">-ResourceGroupName</span></span>
<span data-ttu-id="109a9-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="109a9-130">Name of resource group.</span></span>

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

### <span data-ttu-id="109a9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="109a9-131">-WhatIf</span></span>
<span data-ttu-id="109a9-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="109a9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="109a9-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="109a9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="109a9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="109a9-134">CommonParameters</span></span>
<span data-ttu-id="109a9-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="109a9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="109a9-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="109a9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="109a9-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="109a9-137">INPUTS</span></span>

### <span data-ttu-id="109a9-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="109a9-138">None</span></span>

## <span data-ttu-id="109a9-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="109a9-139">OUTPUTS</span></span>

### <span data-ttu-id="109a9-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="109a9-140">System.Void</span></span>

### <span data-ttu-id="109a9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="109a9-141">System.Boolean</span></span>

## <span data-ttu-id="109a9-142">Notas</span><span class="sxs-lookup"><span data-stu-id="109a9-142">NOTES</span></span>

## <span data-ttu-id="109a9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="109a9-143">RELATED LINKS</span></span>
