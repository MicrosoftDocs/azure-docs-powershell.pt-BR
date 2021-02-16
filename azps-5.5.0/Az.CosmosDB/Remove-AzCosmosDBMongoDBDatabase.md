---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127041"
---
# <span data-ttu-id="4f1d5-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="4f1d5-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="4f1d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f1d5-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1d5-103">Exclui um Banco de Dados MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="4f1d5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f1d5-104">SYNTAX</span></span>

### <span data-ttu-id="4f1d5-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f1d5-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f1d5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f1d5-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f1d5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f1d5-107">DESCRIPTION</span></span>
<span data-ttu-id="4f1d5-108">O cmdlet **Remove-AzCosmosDBMongoDBDatabase** exclui um Banco de Dados MongoDB DoDb.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="4f1d5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f1d5-109">EXAMPLES</span></span>

### <span data-ttu-id="4f1d5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f1d5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="4f1d5-111">O cmdlet retorna um objeto do tipo bool(quando -PassThru é passado), que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="4f1d5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f1d5-112">PARAMETERS</span></span>

### <span data-ttu-id="4f1d5-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="4f1d5-113">-AccountName</span></span>
<span data-ttu-id="4f1d5-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4f1d5-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4f1d5-115">-Confirm</span></span>
<span data-ttu-id="4f1d5-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f1d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1d5-117">-DefaultProfile</span></span>
<span data-ttu-id="4f1d5-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f1d5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f1d5-119">-InputObject</span></span>
<span data-ttu-id="4f1d5-120">Objeto banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="4f1d5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f1d5-121">-Name</span></span>
<span data-ttu-id="4f1d5-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-122">Database name.</span></span>

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

### <span data-ttu-id="4f1d5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f1d5-123">-PassThru</span></span>
<span data-ttu-id="4f1d5-124">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4f1d5-125">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4f1d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f1d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f1d5-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-127">Name of resource group.</span></span>

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

### <span data-ttu-id="4f1d5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f1d5-128">-WhatIf</span></span>
<span data-ttu-id="4f1d5-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f1d5-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f1d5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1d5-131">CommonParameters</span></span>
<span data-ttu-id="4f1d5-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1d5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1d5-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f1d5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1d5-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="4f1d5-134">INPUTS</span></span>

### <span data-ttu-id="4f1d5-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4f1d5-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="4f1d5-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="4f1d5-136">OUTPUTS</span></span>

### <span data-ttu-id="4f1d5-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="4f1d5-137">System.Void</span></span>

### <span data-ttu-id="4f1d5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f1d5-138">System.Boolean</span></span>

## <span data-ttu-id="4f1d5-139">Notas</span><span class="sxs-lookup"><span data-stu-id="4f1d5-139">NOTES</span></span>

## <span data-ttu-id="4f1d5-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f1d5-140">RELATED LINKS</span></span>
