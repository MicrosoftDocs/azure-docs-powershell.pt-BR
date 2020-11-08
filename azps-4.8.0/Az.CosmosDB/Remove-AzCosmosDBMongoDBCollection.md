---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114613"
---
# <span data-ttu-id="0be9a-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="0be9a-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="0be9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0be9a-102">SYNOPSIS</span></span>
<span data-ttu-id="0be9a-103">Exclui uma coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="0be9a-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="0be9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0be9a-104">SYNTAX</span></span>

### <span data-ttu-id="0be9a-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0be9a-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0be9a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0be9a-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0be9a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0be9a-107">DESCRIPTION</span></span>
<span data-ttu-id="0be9a-108">O cmdlet **Remove-AzCosmosDBMongoDBCollection** exclui uma coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="0be9a-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="0be9a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0be9a-109">EXAMPLES</span></span>

### <span data-ttu-id="0be9a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0be9a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="0be9a-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0be9a-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="0be9a-112">OS</span><span class="sxs-lookup"><span data-stu-id="0be9a-112">PARAMETERS</span></span>

### <span data-ttu-id="0be9a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0be9a-113">-AccountName</span></span>
<span data-ttu-id="0be9a-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="0be9a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0be9a-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0be9a-115">-Confirm</span></span>
<span data-ttu-id="0be9a-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0be9a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0be9a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0be9a-117">-DatabaseName</span></span>
<span data-ttu-id="0be9a-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0be9a-118">Database name.</span></span>

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

### <span data-ttu-id="0be9a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be9a-119">-DefaultProfile</span></span>
<span data-ttu-id="0be9a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0be9a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be9a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0be9a-121">-InputObject</span></span>
<span data-ttu-id="0be9a-122">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="0be9a-122">Sql Container object.</span></span>

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

### <span data-ttu-id="0be9a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0be9a-123">-Name</span></span>
<span data-ttu-id="0be9a-124">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="0be9a-124">Collection name.</span></span>

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

### <span data-ttu-id="0be9a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0be9a-125">-PassThru</span></span>
<span data-ttu-id="0be9a-126">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="0be9a-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="0be9a-127">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="0be9a-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="0be9a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be9a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0be9a-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0be9a-129">Name of resource group.</span></span>

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

### <span data-ttu-id="0be9a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0be9a-130">-WhatIf</span></span>
<span data-ttu-id="0be9a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0be9a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0be9a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0be9a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0be9a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be9a-133">CommonParameters</span></span>
<span data-ttu-id="0be9a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0be9a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be9a-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0be9a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be9a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0be9a-136">INPUTS</span></span>

### <span data-ttu-id="0be9a-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="0be9a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="0be9a-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0be9a-138">OUTPUTS</span></span>

### <span data-ttu-id="0be9a-139">System. void</span><span class="sxs-lookup"><span data-stu-id="0be9a-139">System.Void</span></span>

### <span data-ttu-id="0be9a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0be9a-140">System.Boolean</span></span>

## <span data-ttu-id="0be9a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0be9a-141">NOTES</span></span>

## <span data-ttu-id="0be9a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0be9a-142">RELATED LINKS</span></span>
