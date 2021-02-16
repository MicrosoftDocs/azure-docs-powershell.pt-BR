---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117778"
---
# <span data-ttu-id="ba2d3-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="ba2d3-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="ba2d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2d3-103">Exclui o Sql StoredProcedure do SqlDb.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="ba2d3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba2d3-104">SYNTAX</span></span>

### <span data-ttu-id="ba2d3-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba2d3-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba2d3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba2d3-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba2d3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba2d3-107">DESCRIPTION</span></span>
<span data-ttu-id="ba2d3-108">O cmdlet **Remove-AzCosmosDBSqlStoredProcedure** exclui o Sql Sql StoredProcedure correspondente ao determinado ResourceGroupName, AccountName e DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="ba2d3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ba2d3-109">EXAMPLES</span></span>

### <span data-ttu-id="ba2d3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba2d3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="ba2d3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba2d3-111">PARAMETERS</span></span>

### <span data-ttu-id="ba2d3-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="ba2d3-112">-AccountName</span></span>
<span data-ttu-id="ba2d3-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ba2d3-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ba2d3-114">-Confirm</span></span>
<span data-ttu-id="ba2d3-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba2d3-116">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="ba2d3-116">-ContainerName</span></span>
<span data-ttu-id="ba2d3-117">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-117">Container name.</span></span>

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

### <span data-ttu-id="ba2d3-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="ba2d3-118">-DatabaseName</span></span>
<span data-ttu-id="ba2d3-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-119">Database name.</span></span>

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

### <span data-ttu-id="ba2d3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2d3-120">-DefaultProfile</span></span>
<span data-ttu-id="ba2d3-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba2d3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba2d3-122">-InputObject</span></span>
<span data-ttu-id="ba2d3-123">Objeto banco de dados sql.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba2d3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba2d3-124">-Name</span></span>
<span data-ttu-id="ba2d3-125">Nome prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="ba2d3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba2d3-126">-PassThru</span></span>
<span data-ttu-id="ba2d3-127">Para ser definido como verdadeiro se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ba2d3-128">A saída será verdadeira se a operação tiver sido bem-sucedida e um erro for lançado caso não seja.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ba2d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba2d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba2d3-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-130">Name of resource group.</span></span>

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

### <span data-ttu-id="ba2d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba2d3-131">-WhatIf</span></span>
<span data-ttu-id="ba2d3-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba2d3-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba2d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2d3-134">CommonParameters</span></span>
<span data-ttu-id="ba2d3-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba2d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2d3-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba2d3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2d3-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="ba2d3-137">INPUTS</span></span>

### <span data-ttu-id="ba2d3-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ba2d3-138">None</span></span>

## <span data-ttu-id="ba2d3-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="ba2d3-139">OUTPUTS</span></span>

### <span data-ttu-id="ba2d3-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="ba2d3-140">System.Void</span></span>

### <span data-ttu-id="ba2d3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba2d3-141">System.Boolean</span></span>

## <span data-ttu-id="ba2d3-142">Notas</span><span class="sxs-lookup"><span data-stu-id="ba2d3-142">NOTES</span></span>

## <span data-ttu-id="ba2d3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba2d3-143">RELATED LINKS</span></span>
