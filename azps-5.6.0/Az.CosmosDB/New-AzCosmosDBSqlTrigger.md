---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a6808f6c2640a90006560b16dbfd452167e0d6fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887804"
---
# <span data-ttu-id="d7293-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="d7293-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="d7293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7293-102">SYNOPSIS</span></span>
<span data-ttu-id="d7293-103">Cria um novo Gatilho Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d7293-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="d7293-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d7293-104">SYNTAX</span></span>

### <span data-ttu-id="d7293-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7293-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7293-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7293-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7293-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d7293-107">DESCRIPTION</span></span>
<span data-ttu-id="d7293-108">Cria um novo Gatilho Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d7293-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="d7293-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7293-109">EXAMPLES</span></span>

### <span data-ttu-id="d7293-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7293-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="d7293-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d7293-111">PARAMETERS</span></span>

### <span data-ttu-id="d7293-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7293-112">-AccountName</span></span>
<span data-ttu-id="d7293-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="d7293-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d7293-114">-Body</span><span class="sxs-lookup"><span data-stu-id="d7293-114">-Body</span></span>
<span data-ttu-id="d7293-115">O corpo do Gatilho.</span><span class="sxs-lookup"><span data-stu-id="d7293-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="d7293-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7293-116">-Confirm</span></span>
<span data-ttu-id="d7293-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7293-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7293-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d7293-118">-ContainerName</span></span>
<span data-ttu-id="d7293-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d7293-119">Container name.</span></span>

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

### <span data-ttu-id="d7293-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7293-120">-DatabaseName</span></span>
<span data-ttu-id="d7293-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d7293-121">Database name.</span></span>

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

### <span data-ttu-id="d7293-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7293-122">-DefaultProfile</span></span>
<span data-ttu-id="d7293-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7293-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7293-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d7293-124">-Name</span></span>
<span data-ttu-id="d7293-125">Nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="d7293-125">Trigger name.</span></span>

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

### <span data-ttu-id="d7293-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d7293-126">-ParentObject</span></span>
<span data-ttu-id="d7293-127">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="d7293-127">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7293-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7293-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7293-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7293-129">Name of resource group.</span></span>

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

### <span data-ttu-id="d7293-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="d7293-130">-TriggerOperation</span></span>
<span data-ttu-id="d7293-131">A operação à que o gatilho está associado.</span><span class="sxs-lookup"><span data-stu-id="d7293-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="d7293-132">Os valores possíveis incluem: 'All', 'Create', 'Update', 'Delete', 'Replace'</span><span class="sxs-lookup"><span data-stu-id="d7293-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="d7293-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="d7293-133">-TriggerType</span></span>
<span data-ttu-id="d7293-134">Tipo do Gatilho.</span><span class="sxs-lookup"><span data-stu-id="d7293-134">Type of the Trigger.</span></span>
<span data-ttu-id="d7293-135">Os valores possíveis incluem: 'Pre', 'Post'</span><span class="sxs-lookup"><span data-stu-id="d7293-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="d7293-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7293-136">-WhatIf</span></span>
<span data-ttu-id="d7293-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7293-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7293-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7293-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7293-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7293-139">CommonParameters</span></span>
<span data-ttu-id="d7293-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7293-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7293-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7293-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7293-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7293-142">INPUTS</span></span>

### <span data-ttu-id="d7293-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d7293-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="d7293-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d7293-144">OUTPUTS</span></span>

### <span data-ttu-id="d7293-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="d7293-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="d7293-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="d7293-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="d7293-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="d7293-147">NOTES</span></span>

## <span data-ttu-id="d7293-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7293-148">RELATED LINKS</span></span>
