---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940550"
---
# <span data-ttu-id="af940-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="af940-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="af940-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af940-102">SYNOPSIS</span></span>
<span data-ttu-id="af940-103">Cria um novo ou atualiza um gatilho SQL do CosmosDB existente.</span><span class="sxs-lookup"><span data-stu-id="af940-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="af940-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af940-104">SYNTAX</span></span>

### <span data-ttu-id="af940-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="af940-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af940-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af940-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af940-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af940-107">DESCRIPTION</span></span>
<span data-ttu-id="af940-108">O cmdlet **set-AzCosmosDBSqlTrigger** cria um novo ou atualiza um gatilho SQL existente do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="af940-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="af940-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af940-109">EXAMPLES</span></span>

### <span data-ttu-id="af940-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af940-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="af940-111">OS</span><span class="sxs-lookup"><span data-stu-id="af940-111">PARAMETERS</span></span>

### <span data-ttu-id="af940-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af940-112">-AccountName</span></span>
<span data-ttu-id="af940-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="af940-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="af940-114">-Corpo</span><span class="sxs-lookup"><span data-stu-id="af940-114">-Body</span></span>
<span data-ttu-id="af940-115">O corpo do disparador.</span><span class="sxs-lookup"><span data-stu-id="af940-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="af940-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af940-116">-Confirm</span></span>
<span data-ttu-id="af940-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af940-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af940-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="af940-118">-ContainerName</span></span>
<span data-ttu-id="af940-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="af940-119">Container name.</span></span>

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

### <span data-ttu-id="af940-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af940-120">-DatabaseName</span></span>
<span data-ttu-id="af940-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="af940-121">Database name.</span></span>

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

### <span data-ttu-id="af940-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af940-122">-DefaultProfile</span></span>
<span data-ttu-id="af940-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af940-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af940-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af940-124">-InputObject</span></span>
<span data-ttu-id="af940-125">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="af940-125">Sql Container object.</span></span>

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

### <span data-ttu-id="af940-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="af940-126">-Name</span></span>
<span data-ttu-id="af940-127">Nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="af940-127">Trigger name.</span></span>

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

### <span data-ttu-id="af940-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af940-128">-ResourceGroupName</span></span>
<span data-ttu-id="af940-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af940-129">Name of resource group.</span></span>

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

### <span data-ttu-id="af940-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="af940-130">-TriggerOperation</span></span>
<span data-ttu-id="af940-131">A operação à qual o gatilho está associado.</span><span class="sxs-lookup"><span data-stu-id="af940-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="af940-132">Os valores possíveis incluem: ' all', ' Create ', ' Update ', ' Delete ', ' replace '</span><span class="sxs-lookup"><span data-stu-id="af940-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="af940-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="af940-133">-TriggerType</span></span>
<span data-ttu-id="af940-134">Tipo de gatilho.</span><span class="sxs-lookup"><span data-stu-id="af940-134">Type of the Trigger.</span></span>
<span data-ttu-id="af940-135">Os valores possíveis incluem: ' pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="af940-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="af940-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af940-136">-WhatIf</span></span>
<span data-ttu-id="af940-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af940-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af940-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af940-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af940-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af940-139">CommonParameters</span></span>
<span data-ttu-id="af940-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af940-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af940-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af940-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af940-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af940-142">INPUTS</span></span>

### <span data-ttu-id="af940-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="af940-143">None</span></span>

## <span data-ttu-id="af940-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af940-144">OUTPUTS</span></span>

### <span data-ttu-id="af940-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="af940-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="af940-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af940-146">NOTES</span></span>

## <span data-ttu-id="af940-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af940-147">RELATED LINKS</span></span>
