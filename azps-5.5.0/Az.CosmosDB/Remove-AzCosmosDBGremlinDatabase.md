---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116451"
---
# <span data-ttu-id="9f64f-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="9f64f-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="9f64f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f64f-102">SYNOPSIS</span></span>
<span data-ttu-id="9f64f-103">Exclui um Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9f64f-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="9f64f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f64f-104">SYNTAX</span></span>

### <span data-ttu-id="9f64f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f64f-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f64f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f64f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f64f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f64f-107">DESCRIPTION</span></span>
<span data-ttu-id="9f64f-108">O cmdlet **Remove-AzCosmosDBGremlinDatabase** exclui um Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9f64f-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="9f64f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f64f-109">EXAMPLES</span></span>

### <span data-ttu-id="9f64f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f64f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="9f64f-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9f64f-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="9f64f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f64f-112">PARAMETERS</span></span>

### <span data-ttu-id="9f64f-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="9f64f-113">-AccountName</span></span>
<span data-ttu-id="9f64f-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="9f64f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9f64f-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9f64f-115">-Confirm</span></span>
<span data-ttu-id="9f64f-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f64f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f64f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f64f-117">-DefaultProfile</span></span>
<span data-ttu-id="9f64f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f64f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f64f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f64f-119">-InputObject</span></span>
<span data-ttu-id="9f64f-120">Objeto de Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9f64f-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="9f64f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f64f-121">-Name</span></span>
<span data-ttu-id="9f64f-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9f64f-122">Database name.</span></span>

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

### <span data-ttu-id="9f64f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f64f-123">-PassThru</span></span>
<span data-ttu-id="9f64f-124">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="9f64f-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="9f64f-125">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="9f64f-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="9f64f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f64f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f64f-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f64f-127">Name of resource group.</span></span>

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

### <span data-ttu-id="9f64f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f64f-128">-WhatIf</span></span>
<span data-ttu-id="9f64f-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9f64f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f64f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f64f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f64f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f64f-131">CommonParameters</span></span>
<span data-ttu-id="9f64f-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f64f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f64f-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f64f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f64f-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f64f-134">INPUTS</span></span>

### <span data-ttu-id="9f64f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9f64f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="9f64f-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f64f-136">OUTPUTS</span></span>

### <span data-ttu-id="9f64f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="9f64f-137">System.Void</span></span>

### <span data-ttu-id="9f64f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f64f-138">System.Boolean</span></span>

## <span data-ttu-id="9f64f-139">Notas</span><span class="sxs-lookup"><span data-stu-id="9f64f-139">NOTES</span></span>

## <span data-ttu-id="9f64f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f64f-140">RELATED LINKS</span></span>
