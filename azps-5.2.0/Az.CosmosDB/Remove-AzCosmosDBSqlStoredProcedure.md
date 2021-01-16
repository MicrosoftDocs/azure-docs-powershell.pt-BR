---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258770"
---
# <span data-ttu-id="27d9b-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="27d9b-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="27d9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="27d9b-103">Exclui o StoredProcedure do SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="27d9b-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="27d9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27d9b-104">SYNTAX</span></span>

### <span data-ttu-id="27d9b-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27d9b-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d9b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27d9b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27d9b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27d9b-107">DESCRIPTION</span></span>
<span data-ttu-id="27d9b-108">O cmdlet **Remove-AzCosmosDBSqlStoredProcedure** exclui o StoredProcedure SQL CosmosDB correspondente a ResourceGroupName, AccountName e DatabaseName fornecidos.</span><span class="sxs-lookup"><span data-stu-id="27d9b-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="27d9b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27d9b-109">EXAMPLES</span></span>

### <span data-ttu-id="27d9b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="27d9b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="27d9b-111">OS</span><span class="sxs-lookup"><span data-stu-id="27d9b-111">PARAMETERS</span></span>

### <span data-ttu-id="27d9b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="27d9b-112">-AccountName</span></span>
<span data-ttu-id="27d9b-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="27d9b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="27d9b-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27d9b-114">-Confirm</span></span>
<span data-ttu-id="27d9b-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27d9b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27d9b-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="27d9b-116">-ContainerName</span></span>
<span data-ttu-id="27d9b-117">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="27d9b-117">Container name.</span></span>

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

### <span data-ttu-id="27d9b-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27d9b-118">-DatabaseName</span></span>
<span data-ttu-id="27d9b-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="27d9b-119">Database name.</span></span>

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

### <span data-ttu-id="27d9b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d9b-120">-DefaultProfile</span></span>
<span data-ttu-id="27d9b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27d9b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27d9b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27d9b-122">-InputObject</span></span>
<span data-ttu-id="27d9b-123">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="27d9b-123">Sql Database object.</span></span>

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

### <span data-ttu-id="27d9b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="27d9b-124">-Name</span></span>
<span data-ttu-id="27d9b-125">Nome Prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="27d9b-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="27d9b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27d9b-126">-PassThru</span></span>
<span data-ttu-id="27d9b-127">Seja definida como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="27d9b-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="27d9b-128">A saída será true se a operação tiver sido bem-sucedida e um erro será acionado se não.</span><span class="sxs-lookup"><span data-stu-id="27d9b-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="27d9b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27d9b-129">-ResourceGroupName</span></span>
<span data-ttu-id="27d9b-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27d9b-130">Name of resource group.</span></span>

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

### <span data-ttu-id="27d9b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27d9b-131">-WhatIf</span></span>
<span data-ttu-id="27d9b-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27d9b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27d9b-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27d9b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27d9b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d9b-134">CommonParameters</span></span>
<span data-ttu-id="27d9b-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27d9b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d9b-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27d9b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d9b-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27d9b-137">INPUTS</span></span>

### <span data-ttu-id="27d9b-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="27d9b-138">None</span></span>

## <span data-ttu-id="27d9b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27d9b-139">OUTPUTS</span></span>

### <span data-ttu-id="27d9b-140">System. void</span><span class="sxs-lookup"><span data-stu-id="27d9b-140">System.Void</span></span>

### <span data-ttu-id="27d9b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27d9b-141">System.Boolean</span></span>

## <span data-ttu-id="27d9b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27d9b-142">NOTES</span></span>

## <span data-ttu-id="27d9b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27d9b-143">RELATED LINKS</span></span>
