---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: aa5934de20812a8f8a5ebf76c4b23e01cb59d2b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891049"
---
# <span data-ttu-id="d2004-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="d2004-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="d2004-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2004-102">SYNOPSIS</span></span>
<span data-ttu-id="d2004-103">Exclui um banco de dados MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d2004-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="d2004-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2004-104">SYNTAX</span></span>

### <span data-ttu-id="d2004-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2004-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2004-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2004-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2004-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2004-107">DESCRIPTION</span></span>
<span data-ttu-id="d2004-108">O cmdlet **Remove-AzCosmosDBMongoDBDatabase** exclui um banco de dados MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d2004-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="d2004-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2004-109">EXAMPLES</span></span>

### <span data-ttu-id="d2004-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2004-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="d2004-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é true, se a exclusão foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d2004-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="d2004-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2004-112">PARAMETERS</span></span>

### <span data-ttu-id="d2004-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2004-113">-AccountName</span></span>
<span data-ttu-id="d2004-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="d2004-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d2004-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2004-115">-Confirm</span></span>
<span data-ttu-id="d2004-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2004-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2004-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2004-117">-DefaultProfile</span></span>
<span data-ttu-id="d2004-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2004-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2004-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2004-119">-InputObject</span></span>
<span data-ttu-id="d2004-120">Objeto Mongo Database.</span><span class="sxs-lookup"><span data-stu-id="d2004-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2004-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d2004-121">-Name</span></span>
<span data-ttu-id="d2004-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d2004-122">Database name.</span></span>

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

### <span data-ttu-id="d2004-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2004-123">-PassThru</span></span>
<span data-ttu-id="d2004-124">Para ser definido como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="d2004-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d2004-125">A saída será true se a operação tiver sido bem-sucedida e um erro for lançado, caso não seja.</span><span class="sxs-lookup"><span data-stu-id="d2004-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d2004-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2004-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2004-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2004-127">Name of resource group.</span></span>

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

### <span data-ttu-id="d2004-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2004-128">-WhatIf</span></span>
<span data-ttu-id="d2004-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2004-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2004-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2004-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2004-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2004-131">CommonParameters</span></span>
<span data-ttu-id="d2004-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2004-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2004-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2004-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2004-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2004-134">INPUTS</span></span>

### <span data-ttu-id="d2004-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d2004-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="d2004-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2004-136">OUTPUTS</span></span>

### <span data-ttu-id="d2004-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="d2004-137">System.Void</span></span>

### <span data-ttu-id="d2004-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2004-138">System.Boolean</span></span>

## <span data-ttu-id="d2004-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2004-139">NOTES</span></span>

## <span data-ttu-id="d2004-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2004-140">RELATED LINKS</span></span>
