---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429995"
---
# <span data-ttu-id="7df4a-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="7df4a-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="7df4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7df4a-102">SYNOPSIS</span></span>
<span data-ttu-id="7df4a-103">Atualiza o gatilho SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7df4a-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="7df4a-104">Executa uma operação de patch do lado do cliente lendo o gatilho existente.</span><span class="sxs-lookup"><span data-stu-id="7df4a-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="7df4a-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7df4a-105">SYNTAX</span></span>

### <span data-ttu-id="7df4a-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7df4a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7df4a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7df4a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7df4a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7df4a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df4a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7df4a-109">DESCRIPTION</span></span>
<span data-ttu-id="7df4a-110">Atualiza o gatilho SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7df4a-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="7df4a-111">Executa uma operação de patch do lado do cliente lendo o gatilho existente.</span><span class="sxs-lookup"><span data-stu-id="7df4a-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="7df4a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7df4a-112">EXAMPLES</span></span>

### <span data-ttu-id="7df4a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7df4a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="7df4a-114">OS</span><span class="sxs-lookup"><span data-stu-id="7df4a-114">PARAMETERS</span></span>

### <span data-ttu-id="7df4a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7df4a-115">-AccountName</span></span>
<span data-ttu-id="7df4a-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="7df4a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7df4a-117">-Corpo</span><span class="sxs-lookup"><span data-stu-id="7df4a-117">-Body</span></span>
<span data-ttu-id="7df4a-118">O corpo do disparador.</span><span class="sxs-lookup"><span data-stu-id="7df4a-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="7df4a-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7df4a-119">-Confirm</span></span>
<span data-ttu-id="7df4a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7df4a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df4a-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7df4a-121">-ContainerName</span></span>
<span data-ttu-id="7df4a-122">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7df4a-122">Container name.</span></span>

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

### <span data-ttu-id="7df4a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7df4a-123">-DatabaseName</span></span>
<span data-ttu-id="7df4a-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7df4a-124">Database name.</span></span>

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

### <span data-ttu-id="7df4a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df4a-125">-DefaultProfile</span></span>
<span data-ttu-id="7df4a-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7df4a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7df4a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7df4a-127">-InputObject</span></span>
<span data-ttu-id="7df4a-128">Objeto de gatilho SQL</span><span class="sxs-lookup"><span data-stu-id="7df4a-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="7df4a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7df4a-129">-Name</span></span>
<span data-ttu-id="7df4a-130">Nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="7df4a-130">Trigger name.</span></span>

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

### <span data-ttu-id="7df4a-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7df4a-131">-ParentObject</span></span>
<span data-ttu-id="7df4a-132">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="7df4a-132">Sql Container object.</span></span>

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

### <span data-ttu-id="7df4a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df4a-133">-ResourceGroupName</span></span>
<span data-ttu-id="7df4a-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7df4a-134">Name of resource group.</span></span>

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

### <span data-ttu-id="7df4a-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="7df4a-135">-TriggerOperation</span></span>
<span data-ttu-id="7df4a-136">A operação à qual o gatilho está associado.</span><span class="sxs-lookup"><span data-stu-id="7df4a-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="7df4a-137">Os valores possíveis incluem: ' all', ' Create ', ' Update ', ' Delete ', ' replace '</span><span class="sxs-lookup"><span data-stu-id="7df4a-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="7df4a-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="7df4a-138">-TriggerType</span></span>
<span data-ttu-id="7df4a-139">Tipo de gatilho.</span><span class="sxs-lookup"><span data-stu-id="7df4a-139">Type of the Trigger.</span></span>
<span data-ttu-id="7df4a-140">Os valores possíveis incluem: ' pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="7df4a-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="7df4a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df4a-141">-WhatIf</span></span>
<span data-ttu-id="7df4a-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7df4a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df4a-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7df4a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df4a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df4a-144">CommonParameters</span></span>
<span data-ttu-id="7df4a-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df4a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df4a-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7df4a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df4a-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7df4a-147">INPUTS</span></span>

### <span data-ttu-id="7df4a-148">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="7df4a-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="7df4a-149">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="7df4a-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="7df4a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7df4a-150">OUTPUTS</span></span>

### <span data-ttu-id="7df4a-151">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="7df4a-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="7df4a-152">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7df4a-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7df4a-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7df4a-153">NOTES</span></span>

## <span data-ttu-id="7df4a-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7df4a-154">RELATED LINKS</span></span>
