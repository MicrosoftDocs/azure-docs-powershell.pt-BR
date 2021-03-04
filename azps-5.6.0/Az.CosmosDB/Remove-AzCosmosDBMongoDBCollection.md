---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1b4d205460992843e6801ecee13605effb351b77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886241"
---
# <span data-ttu-id="17de9-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="17de9-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="17de9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17de9-102">SYNOPSIS</span></span>
<span data-ttu-id="17de9-103">Exclui uma coleção MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="17de9-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="17de9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17de9-104">SYNTAX</span></span>

### <span data-ttu-id="17de9-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17de9-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17de9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17de9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17de9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17de9-107">DESCRIPTION</span></span>
<span data-ttu-id="17de9-108">O cmdlet **Remove-AzCosmosDBMongoDBCollection** exclui uma coleção MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="17de9-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="17de9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17de9-109">EXAMPLES</span></span>

### <span data-ttu-id="17de9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17de9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="17de9-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é true, se a exclusão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="17de9-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="17de9-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17de9-112">PARAMETERS</span></span>

### <span data-ttu-id="17de9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="17de9-113">-AccountName</span></span>
<span data-ttu-id="17de9-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="17de9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="17de9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17de9-115">-Confirm</span></span>
<span data-ttu-id="17de9-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17de9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17de9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="17de9-117">-DatabaseName</span></span>
<span data-ttu-id="17de9-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17de9-118">Database name.</span></span>

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

### <span data-ttu-id="17de9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17de9-119">-DefaultProfile</span></span>
<span data-ttu-id="17de9-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17de9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17de9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17de9-121">-InputObject</span></span>
<span data-ttu-id="17de9-122">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="17de9-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17de9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="17de9-123">-Name</span></span>
<span data-ttu-id="17de9-124">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="17de9-124">Collection name.</span></span>

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

### <span data-ttu-id="17de9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17de9-125">-PassThru</span></span>
<span data-ttu-id="17de9-126">Para ser definido como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="17de9-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="17de9-127">A saída será true se a operação tiver sido bem-sucedida e um erro for lançado, caso não seja.</span><span class="sxs-lookup"><span data-stu-id="17de9-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="17de9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17de9-128">-ResourceGroupName</span></span>
<span data-ttu-id="17de9-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17de9-129">Name of resource group.</span></span>

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

### <span data-ttu-id="17de9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17de9-130">-WhatIf</span></span>
<span data-ttu-id="17de9-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17de9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17de9-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17de9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17de9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17de9-133">CommonParameters</span></span>
<span data-ttu-id="17de9-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17de9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17de9-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17de9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17de9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17de9-136">INPUTS</span></span>

### <span data-ttu-id="17de9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="17de9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="17de9-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17de9-138">OUTPUTS</span></span>

### <span data-ttu-id="17de9-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="17de9-139">System.Void</span></span>

### <span data-ttu-id="17de9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17de9-140">System.Boolean</span></span>

## <span data-ttu-id="17de9-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="17de9-141">NOTES</span></span>

## <span data-ttu-id="17de9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17de9-142">RELATED LINKS</span></span>
