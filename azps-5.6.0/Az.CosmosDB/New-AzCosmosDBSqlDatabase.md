---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8195179599d98fbc3fd8954361ba142706460886
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893183"
---
# <span data-ttu-id="8141c-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8141c-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="8141c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8141c-102">SYNOPSIS</span></span>
<span data-ttu-id="8141c-103">Cria um novo Banco de Dados Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8141c-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="8141c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8141c-104">SYNTAX</span></span>

### <span data-ttu-id="8141c-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8141c-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8141c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8141c-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8141c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8141c-107">DESCRIPTION</span></span>
<span data-ttu-id="8141c-108">Cria um novo Banco de Dados Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8141c-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="8141c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8141c-109">EXAMPLES</span></span>

### <span data-ttu-id="8141c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8141c-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="8141c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8141c-111">PARAMETERS</span></span>

### <span data-ttu-id="8141c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8141c-112">-AccountName</span></span>
<span data-ttu-id="8141c-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="8141c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8141c-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8141c-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8141c-115">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="8141c-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8141c-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8141c-116">-Confirm</span></span>
<span data-ttu-id="8141c-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8141c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8141c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8141c-118">-DefaultProfile</span></span>
<span data-ttu-id="8141c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8141c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8141c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8141c-120">-Name</span></span>
<span data-ttu-id="8141c-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8141c-121">Database name.</span></span>

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

### <span data-ttu-id="8141c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8141c-122">-ParentObject</span></span>
<span data-ttu-id="8141c-123">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8141c-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8141c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8141c-124">-ResourceGroupName</span></span>
<span data-ttu-id="8141c-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8141c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="8141c-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="8141c-126">-Throughput</span></span>
<span data-ttu-id="8141c-127">A produtividade do SQL de dados (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8141c-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="8141c-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="8141c-128">Default value is 400.</span></span>

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

### <span data-ttu-id="8141c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8141c-129">-WhatIf</span></span>
<span data-ttu-id="8141c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8141c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8141c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8141c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8141c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8141c-132">CommonParameters</span></span>
<span data-ttu-id="8141c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8141c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8141c-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8141c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8141c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8141c-135">INPUTS</span></span>

### <span data-ttu-id="8141c-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8141c-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8141c-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8141c-137">OUTPUTS</span></span>

### <span data-ttu-id="8141c-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8141c-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="8141c-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="8141c-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="8141c-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="8141c-140">NOTES</span></span>

## <span data-ttu-id="8141c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8141c-141">RELATED LINKS</span></span>
