---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434033"
---
# <span data-ttu-id="d38ac-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="d38ac-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="d38ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d38ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d38ac-103">Exclui um banco de dados do CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="d38ac-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="d38ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d38ac-104">SYNTAX</span></span>

### <span data-ttu-id="d38ac-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d38ac-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d38ac-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d38ac-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d38ac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d38ac-107">DESCRIPTION</span></span>
<span data-ttu-id="d38ac-108">O cmdlet **Remove-AzCosmosDBMongoDBDatabase** exclui um banco de dados do MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d38ac-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="d38ac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d38ac-109">EXAMPLES</span></span>

### <span data-ttu-id="d38ac-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d38ac-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="d38ac-111">O cmdlet retorna um objeto do tipo bool (quando-PassThru é passado) que é verdadeiro, se a exclusão tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d38ac-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="d38ac-112">OS</span><span class="sxs-lookup"><span data-stu-id="d38ac-112">PARAMETERS</span></span>

### <span data-ttu-id="d38ac-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d38ac-113">-AccountName</span></span>
<span data-ttu-id="d38ac-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="d38ac-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d38ac-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d38ac-115">-Confirm</span></span>
<span data-ttu-id="d38ac-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d38ac-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d38ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d38ac-117">-DefaultProfile</span></span>
<span data-ttu-id="d38ac-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d38ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d38ac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d38ac-119">-InputObject</span></span>
<span data-ttu-id="d38ac-120">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="d38ac-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="d38ac-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d38ac-121">-Name</span></span>
<span data-ttu-id="d38ac-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d38ac-122">Database name.</span></span>

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

### <span data-ttu-id="d38ac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d38ac-123">-PassThru</span></span>
<span data-ttu-id="d38ac-124">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="d38ac-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d38ac-125">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="d38ac-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d38ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d38ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="d38ac-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d38ac-127">Name of resource group.</span></span>

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

### <span data-ttu-id="d38ac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d38ac-128">-WhatIf</span></span>
<span data-ttu-id="d38ac-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d38ac-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d38ac-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d38ac-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d38ac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d38ac-131">CommonParameters</span></span>
<span data-ttu-id="d38ac-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d38ac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d38ac-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d38ac-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d38ac-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d38ac-134">INPUTS</span></span>

### <span data-ttu-id="d38ac-135">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d38ac-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="d38ac-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d38ac-136">OUTPUTS</span></span>

### <span data-ttu-id="d38ac-137">System. void</span><span class="sxs-lookup"><span data-stu-id="d38ac-137">System.Void</span></span>

### <span data-ttu-id="d38ac-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d38ac-138">System.Boolean</span></span>

## <span data-ttu-id="d38ac-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d38ac-139">NOTES</span></span>

## <span data-ttu-id="d38ac-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d38ac-140">RELATED LINKS</span></span>
