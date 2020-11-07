---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955676"
---
# <span data-ttu-id="4d1c4-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="4d1c4-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="4d1c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1c4-103">Exclui um banco de dados do CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="4d1c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d1c4-104">SYNTAX</span></span>

### <span data-ttu-id="4d1c4-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d1c4-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d1c4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d1c4-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d1c4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d1c4-107">DESCRIPTION</span></span>
<span data-ttu-id="4d1c4-108">O cmdlet **Remove-AzCosmosDBGremlinDatabase** exclui um banco de dados do CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="4d1c4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d1c4-109">EXAMPLES</span></span>

### <span data-ttu-id="4d1c4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d1c4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="4d1c4-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="4d1c4-112">OS</span><span class="sxs-lookup"><span data-stu-id="4d1c4-112">PARAMETERS</span></span>

### <span data-ttu-id="4d1c4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d1c4-113">-AccountName</span></span>
<span data-ttu-id="4d1c4-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4d1c4-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4d1c4-115">-Confirm</span></span>
<span data-ttu-id="4d1c4-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1c4-117">-DefaultProfile</span></span>
<span data-ttu-id="4d1c4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d1c4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d1c4-119">-InputObject</span></span>
<span data-ttu-id="4d1c4-120">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d1c4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d1c4-121">-Name</span></span>
<span data-ttu-id="4d1c4-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-122">Database name.</span></span>

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

### <span data-ttu-id="4d1c4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d1c4-123">-PassThru</span></span>
<span data-ttu-id="4d1c4-124">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4d1c4-125">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4d1c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d1c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d1c4-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-127">Name of resource group.</span></span>

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

### <span data-ttu-id="4d1c4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1c4-128">-WhatIf</span></span>
<span data-ttu-id="4d1c4-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1c4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1c4-131">CommonParameters</span></span>
<span data-ttu-id="4d1c4-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1c4-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d1c4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1c4-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d1c4-134">INPUTS</span></span>

### <span data-ttu-id="4d1c4-135">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4d1c4-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="4d1c4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d1c4-136">OUTPUTS</span></span>

### <span data-ttu-id="4d1c4-137">System. void</span><span class="sxs-lookup"><span data-stu-id="4d1c4-137">System.Void</span></span>

### <span data-ttu-id="4d1c4-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d1c4-138">System.Boolean</span></span>

## <span data-ttu-id="4d1c4-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d1c4-139">NOTES</span></span>

## <span data-ttu-id="4d1c4-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d1c4-140">RELATED LINKS</span></span>
