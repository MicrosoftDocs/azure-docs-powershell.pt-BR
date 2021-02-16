---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117785"
---
# <span data-ttu-id="d7ae9-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="d7ae9-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="d7ae9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ae9-103">Exclui o Contêiner Sql do Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="d7ae9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7ae9-104">SYNTAX</span></span>

### <span data-ttu-id="d7ae9-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7ae9-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7ae9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7ae9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7ae9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7ae9-107">DESCRIPTION</span></span>
<span data-ttu-id="d7ae9-108">O cmdlet **Remove-AzCosmosDBSqlContainer** exclui o Contêiner Sql Do Sql DaLMdb correspondente ao ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="d7ae9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7ae9-109">EXAMPLES</span></span>

### <span data-ttu-id="d7ae9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7ae9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="d7ae9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7ae9-111">PARAMETERS</span></span>

### <span data-ttu-id="d7ae9-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="d7ae9-112">-AccountName</span></span>
<span data-ttu-id="d7ae9-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d7ae9-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d7ae9-114">-Confirm</span></span>
<span data-ttu-id="d7ae9-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ae9-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="d7ae9-116">-DatabaseName</span></span>
<span data-ttu-id="d7ae9-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-117">Database name.</span></span>

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

### <span data-ttu-id="d7ae9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ae9-118">-DefaultProfile</span></span>
<span data-ttu-id="d7ae9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7ae9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7ae9-120">-InputObject</span></span>
<span data-ttu-id="d7ae9-121">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7ae9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7ae9-122">-Name</span></span>
<span data-ttu-id="d7ae9-123">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-123">Container name.</span></span>

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

### <span data-ttu-id="d7ae9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7ae9-124">-PassThru</span></span>
<span data-ttu-id="d7ae9-125">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d7ae9-126">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d7ae9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ae9-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7ae9-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d7ae9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ae9-129">-WhatIf</span></span>
<span data-ttu-id="d7ae9-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7ae9-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ae9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ae9-132">CommonParameters</span></span>
<span data-ttu-id="d7ae9-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ae9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ae9-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7ae9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ae9-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7ae9-135">INPUTS</span></span>

### <span data-ttu-id="d7ae9-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d7ae9-136">None</span></span>

## <span data-ttu-id="d7ae9-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7ae9-137">OUTPUTS</span></span>

### <span data-ttu-id="d7ae9-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="d7ae9-138">System.Void</span></span>

### <span data-ttu-id="d7ae9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7ae9-139">System.Boolean</span></span>

## <span data-ttu-id="d7ae9-140">Notas</span><span class="sxs-lookup"><span data-stu-id="d7ae9-140">NOTES</span></span>

## <span data-ttu-id="d7ae9-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7ae9-141">RELATED LINKS</span></span>
