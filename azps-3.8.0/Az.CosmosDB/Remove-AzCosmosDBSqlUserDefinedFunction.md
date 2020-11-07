---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944442"
---
# <span data-ttu-id="c4a3e-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="c4a3e-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="c4a3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a3e-103">Exclui o CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="c4a3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4a3e-104">SYNTAX</span></span>

### <span data-ttu-id="c4a3e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a3e-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4a3e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a3e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a3e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4a3e-107">DESCRIPTION</span></span>
<span data-ttu-id="c4a3e-108">O cmdlet **Remove-AzCosmosDBSqlUserDefinedFunction** exclui o CosmosDB SQL UserDefinedFunction correspondente ao ResourceGroupName, AccountName e DatabaseName fornecido.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="c4a3e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4a3e-109">EXAMPLES</span></span>

### <span data-ttu-id="c4a3e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c4a3e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="c4a3e-111">OS</span><span class="sxs-lookup"><span data-stu-id="c4a3e-111">PARAMETERS</span></span>

### <span data-ttu-id="c4a3e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4a3e-112">-AccountName</span></span>
<span data-ttu-id="c4a3e-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c4a3e-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4a3e-114">-Confirm</span></span>
<span data-ttu-id="c4a3e-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a3e-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c4a3e-116">-ContainerName</span></span>
<span data-ttu-id="c4a3e-117">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-117">Container name.</span></span>

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

### <span data-ttu-id="c4a3e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4a3e-118">-DatabaseName</span></span>
<span data-ttu-id="c4a3e-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-119">Database name.</span></span>

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

### <span data-ttu-id="c4a3e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a3e-120">-DefaultProfile</span></span>
<span data-ttu-id="c4a3e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a3e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4a3e-122">-InputObject</span></span>
<span data-ttu-id="c4a3e-123">Objeto de função definido pelo usuário SQL</span><span class="sxs-lookup"><span data-stu-id="c4a3e-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="c4a3e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4a3e-124">-Name</span></span>
<span data-ttu-id="c4a3e-125">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="c4a3e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4a3e-126">-PassThru</span></span>
<span data-ttu-id="c4a3e-127">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c4a3e-128">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c4a3e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a3e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c4a3e-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="c4a3e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a3e-131">-WhatIf</span></span>
<span data-ttu-id="c4a3e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a3e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a3e-134">CommonParameters</span></span>
<span data-ttu-id="c4a3e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a3e-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4a3e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a3e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4a3e-137">INPUTS</span></span>

### <span data-ttu-id="c4a3e-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c4a3e-138">None</span></span>

## <span data-ttu-id="c4a3e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4a3e-139">OUTPUTS</span></span>

### <span data-ttu-id="c4a3e-140">System. void</span><span class="sxs-lookup"><span data-stu-id="c4a3e-140">System.Void</span></span>

### <span data-ttu-id="c4a3e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4a3e-141">System.Boolean</span></span>

## <span data-ttu-id="c4a3e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4a3e-142">NOTES</span></span>

## <span data-ttu-id="c4a3e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4a3e-143">RELATED LINKS</span></span>
