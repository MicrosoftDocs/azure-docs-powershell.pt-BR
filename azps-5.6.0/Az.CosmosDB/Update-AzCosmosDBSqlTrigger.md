---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: bebf801316d18b29f6444b0b369833ae547e78d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892868"
---
# <span data-ttu-id="42a80-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="42a80-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="42a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42a80-102">SYNOPSIS</span></span>
<span data-ttu-id="42a80-103">Atualiza o Gatilho Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="42a80-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="42a80-104">Executa uma operação de patch do lado do cliente lendo o Gatilho existente.</span><span class="sxs-lookup"><span data-stu-id="42a80-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="42a80-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="42a80-105">SYNTAX</span></span>

### <span data-ttu-id="42a80-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="42a80-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a80-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42a80-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a80-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42a80-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42a80-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="42a80-109">DESCRIPTION</span></span>
<span data-ttu-id="42a80-110">Atualiza o Gatilho Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="42a80-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="42a80-111">Executa uma operação de patch do lado do cliente lendo o Gatilho existente.</span><span class="sxs-lookup"><span data-stu-id="42a80-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="42a80-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42a80-112">EXAMPLES</span></span>

### <span data-ttu-id="42a80-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42a80-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="42a80-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="42a80-114">PARAMETERS</span></span>

### <span data-ttu-id="42a80-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42a80-115">-AccountName</span></span>
<span data-ttu-id="42a80-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="42a80-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="42a80-117">-Body</span><span class="sxs-lookup"><span data-stu-id="42a80-117">-Body</span></span>
<span data-ttu-id="42a80-118">O corpo do Gatilho.</span><span class="sxs-lookup"><span data-stu-id="42a80-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="42a80-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42a80-119">-Confirm</span></span>
<span data-ttu-id="42a80-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42a80-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42a80-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="42a80-121">-ContainerName</span></span>
<span data-ttu-id="42a80-122">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="42a80-122">Container name.</span></span>

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

### <span data-ttu-id="42a80-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42a80-123">-DatabaseName</span></span>
<span data-ttu-id="42a80-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="42a80-124">Database name.</span></span>

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

### <span data-ttu-id="42a80-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a80-125">-DefaultProfile</span></span>
<span data-ttu-id="42a80-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42a80-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42a80-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42a80-127">-InputObject</span></span>
<span data-ttu-id="42a80-128">Objeto trigger sql</span><span class="sxs-lookup"><span data-stu-id="42a80-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42a80-129">-Name</span><span class="sxs-lookup"><span data-stu-id="42a80-129">-Name</span></span>
<span data-ttu-id="42a80-130">Nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="42a80-130">Trigger name.</span></span>

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

### <span data-ttu-id="42a80-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="42a80-131">-ParentObject</span></span>
<span data-ttu-id="42a80-132">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="42a80-132">Sql Container object.</span></span>

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

### <span data-ttu-id="42a80-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a80-133">-ResourceGroupName</span></span>
<span data-ttu-id="42a80-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42a80-134">Name of resource group.</span></span>

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

### <span data-ttu-id="42a80-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="42a80-135">-TriggerOperation</span></span>
<span data-ttu-id="42a80-136">A operação à que o gatilho está associado.</span><span class="sxs-lookup"><span data-stu-id="42a80-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="42a80-137">Os valores possíveis incluem: 'All', 'Create', 'Update', 'Delete', 'Replace'</span><span class="sxs-lookup"><span data-stu-id="42a80-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="42a80-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="42a80-138">-TriggerType</span></span>
<span data-ttu-id="42a80-139">Tipo do Gatilho.</span><span class="sxs-lookup"><span data-stu-id="42a80-139">Type of the Trigger.</span></span>
<span data-ttu-id="42a80-140">Os valores possíveis incluem: 'Pre', 'Post'</span><span class="sxs-lookup"><span data-stu-id="42a80-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="42a80-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42a80-141">-WhatIf</span></span>
<span data-ttu-id="42a80-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42a80-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42a80-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42a80-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42a80-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a80-144">CommonParameters</span></span>
<span data-ttu-id="42a80-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a80-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a80-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42a80-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a80-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42a80-147">INPUTS</span></span>

### <span data-ttu-id="42a80-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="42a80-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="42a80-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="42a80-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="42a80-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="42a80-150">OUTPUTS</span></span>

### <span data-ttu-id="42a80-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="42a80-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="42a80-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="42a80-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="42a80-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="42a80-153">NOTES</span></span>

## <span data-ttu-id="42a80-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42a80-154">RELATED LINKS</span></span>
