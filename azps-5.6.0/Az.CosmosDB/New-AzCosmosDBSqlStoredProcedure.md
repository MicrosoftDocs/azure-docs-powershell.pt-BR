---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b088eaf9e09408b8a294965c66acf88ac2715dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886780"
---
# <span data-ttu-id="025c3-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="025c3-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="025c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025c3-102">SYNOPSIS</span></span>
<span data-ttu-id="025c3-103">Cria um novo Sql StoredProcedure do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="025c3-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="025c3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="025c3-104">SYNTAX</span></span>

### <span data-ttu-id="025c3-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="025c3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="025c3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="025c3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025c3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="025c3-107">DESCRIPTION</span></span>
<span data-ttu-id="025c3-108">Cria um novo Sql StoredProcedure do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="025c3-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="025c3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="025c3-109">EXAMPLES</span></span>

### <span data-ttu-id="025c3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="025c3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="025c3-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="025c3-111">PARAMETERS</span></span>

### <span data-ttu-id="025c3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="025c3-112">-AccountName</span></span>
<span data-ttu-id="025c3-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="025c3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="025c3-114">-Body</span><span class="sxs-lookup"><span data-stu-id="025c3-114">-Body</span></span>
<span data-ttu-id="025c3-115">O corpo do Procedimento Armazenado.</span><span class="sxs-lookup"><span data-stu-id="025c3-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="025c3-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="025c3-116">-Confirm</span></span>
<span data-ttu-id="025c3-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025c3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="025c3-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="025c3-118">-ContainerName</span></span>
<span data-ttu-id="025c3-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="025c3-119">Container name.</span></span>

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

### <span data-ttu-id="025c3-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="025c3-120">-DatabaseName</span></span>
<span data-ttu-id="025c3-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="025c3-121">Database name.</span></span>

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

### <span data-ttu-id="025c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025c3-122">-DefaultProfile</span></span>
<span data-ttu-id="025c3-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="025c3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="025c3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="025c3-124">-Name</span></span>
<span data-ttu-id="025c3-125">Nome de Prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="025c3-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="025c3-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="025c3-126">-ParentObject</span></span>
<span data-ttu-id="025c3-127">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="025c3-127">Sql Container object.</span></span>

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

### <span data-ttu-id="025c3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025c3-128">-ResourceGroupName</span></span>
<span data-ttu-id="025c3-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="025c3-129">Name of resource group.</span></span>

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

### <span data-ttu-id="025c3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025c3-130">-WhatIf</span></span>
<span data-ttu-id="025c3-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="025c3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="025c3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="025c3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="025c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025c3-133">CommonParameters</span></span>
<span data-ttu-id="025c3-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025c3-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="025c3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025c3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="025c3-136">INPUTS</span></span>

### <span data-ttu-id="025c3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="025c3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="025c3-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="025c3-138">OUTPUTS</span></span>

### <span data-ttu-id="025c3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="025c3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="025c3-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="025c3-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="025c3-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="025c3-141">NOTES</span></span>

## <span data-ttu-id="025c3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="025c3-142">RELATED LINKS</span></span>
