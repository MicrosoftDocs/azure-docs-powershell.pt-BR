---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261124"
---
# <span data-ttu-id="47999-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="47999-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="47999-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47999-102">SYNOPSIS</span></span>
<span data-ttu-id="47999-103">Exclui uma coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="47999-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="47999-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47999-104">SYNTAX</span></span>

### <span data-ttu-id="47999-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="47999-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47999-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47999-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47999-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47999-107">DESCRIPTION</span></span>
<span data-ttu-id="47999-108">O cmdlet **Remove-AzCosmosDBMongoDBCollection** exclui uma coleção CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="47999-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="47999-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47999-109">EXAMPLES</span></span>

### <span data-ttu-id="47999-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47999-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="47999-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="47999-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="47999-112">OS</span><span class="sxs-lookup"><span data-stu-id="47999-112">PARAMETERS</span></span>

### <span data-ttu-id="47999-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="47999-113">-AccountName</span></span>
<span data-ttu-id="47999-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="47999-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="47999-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47999-115">-Confirm</span></span>
<span data-ttu-id="47999-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47999-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47999-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47999-117">-DatabaseName</span></span>
<span data-ttu-id="47999-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="47999-118">Database name.</span></span>

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

### <span data-ttu-id="47999-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47999-119">-DefaultProfile</span></span>
<span data-ttu-id="47999-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47999-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47999-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47999-121">-InputObject</span></span>
<span data-ttu-id="47999-122">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="47999-122">Sql Container object.</span></span>

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

### <span data-ttu-id="47999-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="47999-123">-Name</span></span>
<span data-ttu-id="47999-124">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="47999-124">Collection name.</span></span>

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

### <span data-ttu-id="47999-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47999-125">-PassThru</span></span>
<span data-ttu-id="47999-126">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="47999-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="47999-127">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="47999-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="47999-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47999-128">-ResourceGroupName</span></span>
<span data-ttu-id="47999-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="47999-129">Name of resource group.</span></span>

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

### <span data-ttu-id="47999-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47999-130">-WhatIf</span></span>
<span data-ttu-id="47999-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47999-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47999-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47999-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47999-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47999-133">CommonParameters</span></span>
<span data-ttu-id="47999-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47999-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47999-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47999-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47999-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47999-136">INPUTS</span></span>

### <span data-ttu-id="47999-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="47999-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="47999-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47999-138">OUTPUTS</span></span>

### <span data-ttu-id="47999-139">System. void</span><span class="sxs-lookup"><span data-stu-id="47999-139">System.Void</span></span>

### <span data-ttu-id="47999-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47999-140">System.Boolean</span></span>

## <span data-ttu-id="47999-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47999-141">NOTES</span></span>

## <span data-ttu-id="47999-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47999-142">RELATED LINKS</span></span>
