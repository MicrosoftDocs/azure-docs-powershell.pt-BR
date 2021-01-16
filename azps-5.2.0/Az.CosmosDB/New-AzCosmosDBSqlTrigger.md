---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263621"
---
# <span data-ttu-id="66418-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="66418-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="66418-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66418-102">SYNOPSIS</span></span>
<span data-ttu-id="66418-103">Cria um novo gatilho SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="66418-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="66418-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66418-104">SYNTAX</span></span>

### <span data-ttu-id="66418-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="66418-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66418-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66418-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66418-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66418-107">DESCRIPTION</span></span>
<span data-ttu-id="66418-108">Cria um novo gatilho SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="66418-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="66418-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66418-109">EXAMPLES</span></span>

### <span data-ttu-id="66418-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66418-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="66418-111">OS</span><span class="sxs-lookup"><span data-stu-id="66418-111">PARAMETERS</span></span>

### <span data-ttu-id="66418-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66418-112">-AccountName</span></span>
<span data-ttu-id="66418-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="66418-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66418-114">-Corpo</span><span class="sxs-lookup"><span data-stu-id="66418-114">-Body</span></span>
<span data-ttu-id="66418-115">O corpo do disparador.</span><span class="sxs-lookup"><span data-stu-id="66418-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="66418-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66418-116">-Confirm</span></span>
<span data-ttu-id="66418-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66418-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66418-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="66418-118">-ContainerName</span></span>
<span data-ttu-id="66418-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="66418-119">Container name.</span></span>

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

### <span data-ttu-id="66418-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66418-120">-DatabaseName</span></span>
<span data-ttu-id="66418-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="66418-121">Database name.</span></span>

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

### <span data-ttu-id="66418-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66418-122">-DefaultProfile</span></span>
<span data-ttu-id="66418-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66418-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66418-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="66418-124">-Name</span></span>
<span data-ttu-id="66418-125">Nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="66418-125">Trigger name.</span></span>

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

### <span data-ttu-id="66418-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="66418-126">-ParentObject</span></span>
<span data-ttu-id="66418-127">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="66418-127">Sql Container object.</span></span>

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

### <span data-ttu-id="66418-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66418-128">-ResourceGroupName</span></span>
<span data-ttu-id="66418-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66418-129">Name of resource group.</span></span>

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

### <span data-ttu-id="66418-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="66418-130">-TriggerOperation</span></span>
<span data-ttu-id="66418-131">A operação à qual o gatilho está associado.</span><span class="sxs-lookup"><span data-stu-id="66418-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="66418-132">Os valores possíveis incluem: ' all', ' Create ', ' Update ', ' Delete ', ' replace '</span><span class="sxs-lookup"><span data-stu-id="66418-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="66418-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="66418-133">-TriggerType</span></span>
<span data-ttu-id="66418-134">Tipo de gatilho.</span><span class="sxs-lookup"><span data-stu-id="66418-134">Type of the Trigger.</span></span>
<span data-ttu-id="66418-135">Os valores possíveis incluem: ' pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="66418-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="66418-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66418-136">-WhatIf</span></span>
<span data-ttu-id="66418-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66418-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66418-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66418-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66418-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66418-139">CommonParameters</span></span>
<span data-ttu-id="66418-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66418-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66418-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66418-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66418-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66418-142">INPUTS</span></span>

### <span data-ttu-id="66418-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="66418-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="66418-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66418-144">OUTPUTS</span></span>

### <span data-ttu-id="66418-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="66418-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="66418-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="66418-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="66418-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66418-147">NOTES</span></span>

## <span data-ttu-id="66418-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66418-148">RELATED LINKS</span></span>
