---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127047"
---
# <span data-ttu-id="d63f1-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d63f1-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d63f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d63f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d63f1-103">Cria um novo Banco de Dados Sql do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="d63f1-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d63f1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d63f1-104">SYNTAX</span></span>

### <span data-ttu-id="d63f1-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d63f1-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d63f1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d63f1-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d63f1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d63f1-107">DESCRIPTION</span></span>
<span data-ttu-id="d63f1-108">Cria um novo Banco de Dados Sql do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="d63f1-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d63f1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d63f1-109">EXAMPLES</span></span>

### <span data-ttu-id="d63f1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d63f1-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="d63f1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d63f1-111">PARAMETERS</span></span>

### <span data-ttu-id="d63f1-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="d63f1-112">-AccountName</span></span>
<span data-ttu-id="d63f1-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="d63f1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d63f1-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d63f1-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d63f1-115">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="d63f1-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d63f1-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d63f1-116">-Confirm</span></span>
<span data-ttu-id="d63f1-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d63f1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d63f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d63f1-118">-DefaultProfile</span></span>
<span data-ttu-id="d63f1-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d63f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d63f1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d63f1-120">-Name</span></span>
<span data-ttu-id="d63f1-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d63f1-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d63f1-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d63f1-122">-ParentObject</span></span>
<span data-ttu-id="d63f1-123">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="d63f1-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d63f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d63f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="d63f1-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d63f1-125">Name of resource group.</span></span>

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

### <span data-ttu-id="d63f1-126">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="d63f1-126">-Throughput</span></span>
<span data-ttu-id="d63f1-127">A produtividade do banco de dados SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d63f1-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="d63f1-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="d63f1-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d63f1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d63f1-129">-WhatIf</span></span>
<span data-ttu-id="d63f1-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d63f1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d63f1-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d63f1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d63f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d63f1-132">CommonParameters</span></span>
<span data-ttu-id="d63f1-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d63f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d63f1-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d63f1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d63f1-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="d63f1-135">INPUTS</span></span>

### <span data-ttu-id="d63f1-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d63f1-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d63f1-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="d63f1-137">OUTPUTS</span></span>

### <span data-ttu-id="d63f1-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d63f1-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d63f1-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="d63f1-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="d63f1-140">Notas</span><span class="sxs-lookup"><span data-stu-id="d63f1-140">NOTES</span></span>

## <span data-ttu-id="d63f1-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d63f1-141">RELATED LINKS</span></span>
