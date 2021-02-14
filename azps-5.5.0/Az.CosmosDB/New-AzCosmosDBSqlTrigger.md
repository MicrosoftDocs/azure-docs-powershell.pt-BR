---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111027"
---
# <span data-ttu-id="127eb-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="127eb-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="127eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="127eb-102">SYNOPSIS</span></span>
<span data-ttu-id="127eb-103">Cria um novo Gatilho Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="127eb-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="127eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="127eb-104">SYNTAX</span></span>

### <span data-ttu-id="127eb-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="127eb-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127eb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="127eb-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="127eb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="127eb-107">DESCRIPTION</span></span>
<span data-ttu-id="127eb-108">Cria um novo Gatilho Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="127eb-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="127eb-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="127eb-109">EXAMPLES</span></span>

### <span data-ttu-id="127eb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="127eb-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="127eb-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="127eb-111">PARAMETERS</span></span>

### <span data-ttu-id="127eb-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="127eb-112">-AccountName</span></span>
<span data-ttu-id="127eb-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="127eb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="127eb-114">-Corpo</span><span class="sxs-lookup"><span data-stu-id="127eb-114">-Body</span></span>
<span data-ttu-id="127eb-115">O corpo do Gatilho.</span><span class="sxs-lookup"><span data-stu-id="127eb-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="127eb-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="127eb-116">-Confirm</span></span>
<span data-ttu-id="127eb-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="127eb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="127eb-118">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="127eb-118">-ContainerName</span></span>
<span data-ttu-id="127eb-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="127eb-119">Container name.</span></span>

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

### <span data-ttu-id="127eb-120">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="127eb-120">-DatabaseName</span></span>
<span data-ttu-id="127eb-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="127eb-121">Database name.</span></span>

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

### <span data-ttu-id="127eb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127eb-122">-DefaultProfile</span></span>
<span data-ttu-id="127eb-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="127eb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="127eb-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="127eb-124">-Name</span></span>
<span data-ttu-id="127eb-125">Nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="127eb-125">Trigger name.</span></span>

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

### <span data-ttu-id="127eb-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="127eb-126">-ParentObject</span></span>
<span data-ttu-id="127eb-127">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="127eb-127">Sql Container object.</span></span>

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

### <span data-ttu-id="127eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="127eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="127eb-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="127eb-129">Name of resource group.</span></span>

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

### <span data-ttu-id="127eb-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="127eb-130">-TriggerOperation</span></span>
<span data-ttu-id="127eb-131">A operação à que o gatilho está associado.</span><span class="sxs-lookup"><span data-stu-id="127eb-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="127eb-132">Os valores possíveis incluem: 'Tudo', 'Criar', 'Atualizar', 'Excluir', 'Substituir'</span><span class="sxs-lookup"><span data-stu-id="127eb-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="127eb-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="127eb-133">-TriggerType</span></span>
<span data-ttu-id="127eb-134">Tipo do Gatilho.</span><span class="sxs-lookup"><span data-stu-id="127eb-134">Type of the Trigger.</span></span>
<span data-ttu-id="127eb-135">Os valores possíveis incluem: 'Pre', 'Post'</span><span class="sxs-lookup"><span data-stu-id="127eb-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="127eb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="127eb-136">-WhatIf</span></span>
<span data-ttu-id="127eb-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="127eb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="127eb-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="127eb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="127eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127eb-139">CommonParameters</span></span>
<span data-ttu-id="127eb-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127eb-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="127eb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127eb-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="127eb-142">INPUTS</span></span>

### <span data-ttu-id="127eb-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="127eb-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="127eb-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="127eb-144">OUTPUTS</span></span>

### <span data-ttu-id="127eb-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTrigetResults</span><span class="sxs-lookup"><span data-stu-id="127eb-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="127eb-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="127eb-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="127eb-147">Notas</span><span class="sxs-lookup"><span data-stu-id="127eb-147">NOTES</span></span>

## <span data-ttu-id="127eb-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="127eb-148">RELATED LINKS</span></span>
