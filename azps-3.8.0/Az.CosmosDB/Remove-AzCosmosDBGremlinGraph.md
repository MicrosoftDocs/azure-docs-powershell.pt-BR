---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943622"
---
# <span data-ttu-id="4166d-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="4166d-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="4166d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4166d-102">SYNOPSIS</span></span>
<span data-ttu-id="4166d-103">Exclui um gráfico de Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4166d-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="4166d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4166d-104">SYNTAX</span></span>

### <span data-ttu-id="4166d-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4166d-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4166d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4166d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4166d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4166d-107">DESCRIPTION</span></span>
<span data-ttu-id="4166d-108">O cmdlet **Remove-AzCosmosDBGremlinGraph** exclui um gráfico de Gremlin de CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4166d-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="4166d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4166d-109">EXAMPLES</span></span>

### <span data-ttu-id="4166d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4166d-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="4166d-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4166d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="4166d-112">OS</span><span class="sxs-lookup"><span data-stu-id="4166d-112">PARAMETERS</span></span>

### <span data-ttu-id="4166d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4166d-113">-AccountName</span></span>
<span data-ttu-id="4166d-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="4166d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4166d-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4166d-115">-Confirm</span></span>
<span data-ttu-id="4166d-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4166d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4166d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4166d-117">-DatabaseName</span></span>
<span data-ttu-id="4166d-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4166d-118">Database name.</span></span>

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

### <span data-ttu-id="4166d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4166d-119">-DefaultProfile</span></span>
<span data-ttu-id="4166d-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4166d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4166d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4166d-121">-InputObject</span></span>
<span data-ttu-id="4166d-122">Objeto de gráfico Gremlin.</span><span class="sxs-lookup"><span data-stu-id="4166d-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4166d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4166d-123">-Name</span></span>
<span data-ttu-id="4166d-124">Gremlin o nome do gráfico.</span><span class="sxs-lookup"><span data-stu-id="4166d-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="4166d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4166d-125">-PassThru</span></span>
<span data-ttu-id="4166d-126">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="4166d-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4166d-127">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="4166d-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4166d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4166d-128">-ResourceGroupName</span></span>
<span data-ttu-id="4166d-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4166d-129">Name of resource group.</span></span>

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

### <span data-ttu-id="4166d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4166d-130">-WhatIf</span></span>
<span data-ttu-id="4166d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4166d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4166d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4166d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4166d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4166d-133">CommonParameters</span></span>
<span data-ttu-id="4166d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4166d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4166d-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4166d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4166d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4166d-136">INPUTS</span></span>

### <span data-ttu-id="4166d-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="4166d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="4166d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4166d-138">OUTPUTS</span></span>

### <span data-ttu-id="4166d-139">System. void</span><span class="sxs-lookup"><span data-stu-id="4166d-139">System.Void</span></span>

### <span data-ttu-id="4166d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4166d-140">System.Boolean</span></span>

## <span data-ttu-id="4166d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4166d-141">NOTES</span></span>

## <span data-ttu-id="4166d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4166d-142">RELATED LINKS</span></span>
