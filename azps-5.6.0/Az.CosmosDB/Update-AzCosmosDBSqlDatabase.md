---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1bfb0ec8392c0ddcce20db839f1817688e8feb7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888536"
---
# <span data-ttu-id="847cc-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="847cc-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="847cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="847cc-102">SYNOPSIS</span></span>
<span data-ttu-id="847cc-103">Atualiza o Banco de Dados Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="847cc-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="847cc-104">Executa uma operação de patch do lado do cliente lendo o Banco de Dados existente.</span><span class="sxs-lookup"><span data-stu-id="847cc-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="847cc-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="847cc-105">SYNTAX</span></span>

### <span data-ttu-id="847cc-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="847cc-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="847cc-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="847cc-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="847cc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="847cc-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="847cc-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="847cc-109">DESCRIPTION</span></span>
<span data-ttu-id="847cc-110">Atualiza o Banco de Dados Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="847cc-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="847cc-111">Executa uma operação de patch do lado do cliente lendo o Banco de Dados existente.</span><span class="sxs-lookup"><span data-stu-id="847cc-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="847cc-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="847cc-112">EXAMPLES</span></span>

### <span data-ttu-id="847cc-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="847cc-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="847cc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="847cc-114">PARAMETERS</span></span>

### <span data-ttu-id="847cc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="847cc-115">-AccountName</span></span>
<span data-ttu-id="847cc-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="847cc-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="847cc-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="847cc-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="847cc-118">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="847cc-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="847cc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="847cc-119">-Confirm</span></span>
<span data-ttu-id="847cc-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="847cc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="847cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847cc-121">-DefaultProfile</span></span>
<span data-ttu-id="847cc-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="847cc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="847cc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="847cc-123">-InputObject</span></span>
<span data-ttu-id="847cc-124">Objeto Sql Database.</span><span class="sxs-lookup"><span data-stu-id="847cc-124">Sql Database object.</span></span>

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

### <span data-ttu-id="847cc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="847cc-125">-Name</span></span>
<span data-ttu-id="847cc-126">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="847cc-126">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847cc-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="847cc-127">-ParentObject</span></span>
<span data-ttu-id="847cc-128">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="847cc-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="847cc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="847cc-129">-ResourceGroupName</span></span>
<span data-ttu-id="847cc-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="847cc-130">Name of resource group.</span></span>

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

### <span data-ttu-id="847cc-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="847cc-131">-Throughput</span></span>
<span data-ttu-id="847cc-132">A produtividade do SQL de dados (RU/s).</span><span class="sxs-lookup"><span data-stu-id="847cc-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="847cc-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="847cc-133">Default value is 400.</span></span>

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

### <span data-ttu-id="847cc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="847cc-134">-WhatIf</span></span>
<span data-ttu-id="847cc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="847cc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="847cc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="847cc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="847cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847cc-137">CommonParameters</span></span>
<span data-ttu-id="847cc-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="847cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847cc-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="847cc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847cc-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="847cc-140">INPUTS</span></span>

### <span data-ttu-id="847cc-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="847cc-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="847cc-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="847cc-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="847cc-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="847cc-143">OUTPUTS</span></span>

### <span data-ttu-id="847cc-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="847cc-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="847cc-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="847cc-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="847cc-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="847cc-146">NOTES</span></span>

## <span data-ttu-id="847cc-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="847cc-147">RELATED LINKS</span></span>
