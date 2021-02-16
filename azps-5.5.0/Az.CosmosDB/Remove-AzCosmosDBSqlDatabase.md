---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117780"
---
# <span data-ttu-id="e0382-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e0382-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="e0382-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0382-102">SYNOPSIS</span></span>
<span data-ttu-id="e0382-103">Exclui o Banco de Dados Sql do Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="e0382-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="e0382-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0382-104">SYNTAX</span></span>

### <span data-ttu-id="e0382-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0382-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0382-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0382-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0382-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0382-107">DESCRIPTION</span></span>
<span data-ttu-id="e0382-108">O cmdlet **Remove-AzCosmosDBSqlDatabase** exclui o Banco de Dados Sql Do Sql Do Sql correspondente ao ResourceGroupName, AccountName e DatabaseName determinados.</span><span class="sxs-lookup"><span data-stu-id="e0382-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="e0382-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0382-109">EXAMPLES</span></span>

### <span data-ttu-id="e0382-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0382-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="e0382-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0382-111">PARAMETERS</span></span>

### <span data-ttu-id="e0382-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="e0382-112">-AccountName</span></span>
<span data-ttu-id="e0382-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="e0382-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e0382-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0382-114">-Confirm</span></span>
<span data-ttu-id="e0382-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0382-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0382-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0382-116">-DefaultProfile</span></span>
<span data-ttu-id="e0382-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0382-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0382-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0382-118">-InputObject</span></span>
<span data-ttu-id="e0382-119">Objeto banco de dados sql.</span><span class="sxs-lookup"><span data-stu-id="e0382-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0382-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0382-120">-Name</span></span>
<span data-ttu-id="e0382-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e0382-121">Database name.</span></span>

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

### <span data-ttu-id="e0382-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0382-122">-PassThru</span></span>
<span data-ttu-id="e0382-123">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="e0382-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e0382-124">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="e0382-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e0382-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0382-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0382-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0382-126">Name of resource group.</span></span>

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

### <span data-ttu-id="e0382-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0382-127">-WhatIf</span></span>
<span data-ttu-id="e0382-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0382-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0382-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0382-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0382-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0382-130">CommonParameters</span></span>
<span data-ttu-id="e0382-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0382-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0382-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0382-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0382-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0382-133">INPUTS</span></span>

### <span data-ttu-id="e0382-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e0382-134">None</span></span>

## <span data-ttu-id="e0382-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0382-135">OUTPUTS</span></span>

### <span data-ttu-id="e0382-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="e0382-136">System.Void</span></span>

### <span data-ttu-id="e0382-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0382-137">System.Boolean</span></span>

## <span data-ttu-id="e0382-138">Notas</span><span class="sxs-lookup"><span data-stu-id="e0382-138">NOTES</span></span>

## <span data-ttu-id="e0382-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0382-139">RELATED LINKS</span></span>
