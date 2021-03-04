---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: a56a7a091544bef7c66ab26c66c54aded8bebdf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886779"
---
# <span data-ttu-id="bf849-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bf849-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="bf849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf849-102">SYNOPSIS</span></span>
<span data-ttu-id="bf849-103">Exclui o Banco de Dados Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="bf849-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="bf849-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bf849-104">SYNTAX</span></span>

### <span data-ttu-id="bf849-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf849-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf849-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf849-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf849-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bf849-107">DESCRIPTION</span></span>
<span data-ttu-id="bf849-108">O cmdlet **Remove-AzCosmosDBSqlDatabase** exclui o Banco de Dados Sql do CosmosDB correspondente ao ResourceGroupName, AccountName e DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="bf849-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="bf849-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf849-109">EXAMPLES</span></span>

### <span data-ttu-id="bf849-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf849-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="bf849-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bf849-111">PARAMETERS</span></span>

### <span data-ttu-id="bf849-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf849-112">-AccountName</span></span>
<span data-ttu-id="bf849-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="bf849-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bf849-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf849-114">-Confirm</span></span>
<span data-ttu-id="bf849-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf849-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf849-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf849-116">-DefaultProfile</span></span>
<span data-ttu-id="bf849-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf849-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf849-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf849-118">-InputObject</span></span>
<span data-ttu-id="bf849-119">Objeto Sql Database.</span><span class="sxs-lookup"><span data-stu-id="bf849-119">Sql Database object.</span></span>

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

### <span data-ttu-id="bf849-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bf849-120">-Name</span></span>
<span data-ttu-id="bf849-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bf849-121">Database name.</span></span>

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

### <span data-ttu-id="bf849-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf849-122">-PassThru</span></span>
<span data-ttu-id="bf849-123">Para ser definido como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="bf849-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="bf849-124">A saída será true se a operação tiver sido bem-sucedida e um erro for lançado, caso não seja.</span><span class="sxs-lookup"><span data-stu-id="bf849-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="bf849-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf849-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf849-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf849-126">Name of resource group.</span></span>

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

### <span data-ttu-id="bf849-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf849-127">-WhatIf</span></span>
<span data-ttu-id="bf849-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf849-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf849-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf849-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf849-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf849-130">CommonParameters</span></span>
<span data-ttu-id="bf849-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf849-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf849-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf849-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf849-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf849-133">INPUTS</span></span>

### <span data-ttu-id="bf849-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bf849-134">None</span></span>

## <span data-ttu-id="bf849-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bf849-135">OUTPUTS</span></span>

### <span data-ttu-id="bf849-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="bf849-136">System.Void</span></span>

### <span data-ttu-id="bf849-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf849-137">System.Boolean</span></span>

## <span data-ttu-id="bf849-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="bf849-138">NOTES</span></span>

## <span data-ttu-id="bf849-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf849-139">RELATED LINKS</span></span>
