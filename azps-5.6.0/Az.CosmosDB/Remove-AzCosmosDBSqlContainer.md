---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: ab64359e8db417c3c87a49a773fe56c3dcc5334b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886065"
---
# <span data-ttu-id="74dba-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="74dba-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="74dba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74dba-102">SYNOPSIS</span></span>
<span data-ttu-id="74dba-103">Exclui o Contêiner Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="74dba-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="74dba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="74dba-104">SYNTAX</span></span>

### <span data-ttu-id="74dba-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="74dba-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74dba-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74dba-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74dba-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="74dba-107">DESCRIPTION</span></span>
<span data-ttu-id="74dba-108">O cmdlet **Remove-AzCosmosDBSqlContainer** exclui o Contêiner Sql do CosmosDB correspondente ao ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="74dba-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="74dba-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74dba-109">EXAMPLES</span></span>

### <span data-ttu-id="74dba-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74dba-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="74dba-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="74dba-111">PARAMETERS</span></span>

### <span data-ttu-id="74dba-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74dba-112">-AccountName</span></span>
<span data-ttu-id="74dba-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="74dba-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="74dba-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74dba-114">-Confirm</span></span>
<span data-ttu-id="74dba-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74dba-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74dba-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74dba-116">-DatabaseName</span></span>
<span data-ttu-id="74dba-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="74dba-117">Database name.</span></span>

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

### <span data-ttu-id="74dba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74dba-118">-DefaultProfile</span></span>
<span data-ttu-id="74dba-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74dba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74dba-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74dba-120">-InputObject</span></span>
<span data-ttu-id="74dba-121">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="74dba-121">Sql Container object.</span></span>

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

### <span data-ttu-id="74dba-122">-Name</span><span class="sxs-lookup"><span data-stu-id="74dba-122">-Name</span></span>
<span data-ttu-id="74dba-123">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="74dba-123">Container name.</span></span>

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

### <span data-ttu-id="74dba-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74dba-124">-PassThru</span></span>
<span data-ttu-id="74dba-125">Para ser definido como true se o usuário quiser receber uma saída.</span><span class="sxs-lookup"><span data-stu-id="74dba-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="74dba-126">A saída será true se a operação tiver sido bem-sucedida e um erro for lançado, caso não seja.</span><span class="sxs-lookup"><span data-stu-id="74dba-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="74dba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74dba-127">-ResourceGroupName</span></span>
<span data-ttu-id="74dba-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74dba-128">Name of resource group.</span></span>

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

### <span data-ttu-id="74dba-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74dba-129">-WhatIf</span></span>
<span data-ttu-id="74dba-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74dba-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74dba-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74dba-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74dba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74dba-132">CommonParameters</span></span>
<span data-ttu-id="74dba-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74dba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74dba-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74dba-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74dba-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74dba-135">INPUTS</span></span>

### <span data-ttu-id="74dba-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="74dba-136">None</span></span>

## <span data-ttu-id="74dba-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="74dba-137">OUTPUTS</span></span>

### <span data-ttu-id="74dba-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="74dba-138">System.Void</span></span>

### <span data-ttu-id="74dba-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74dba-139">System.Boolean</span></span>

## <span data-ttu-id="74dba-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="74dba-140">NOTES</span></span>

## <span data-ttu-id="74dba-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74dba-141">RELATED LINKS</span></span>
