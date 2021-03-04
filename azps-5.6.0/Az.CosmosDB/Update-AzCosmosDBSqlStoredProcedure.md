---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 8a717b15268090a7e5ea356c49b11d9aba1ab009
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888530"
---
# <span data-ttu-id="99ee5-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="99ee5-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="99ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="99ee5-103">Atualiza o Sql StoredProcedure do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="99ee5-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="99ee5-104">Executa uma operação de patch do lado do cliente lendo o StoredProcedure existente.</span><span class="sxs-lookup"><span data-stu-id="99ee5-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="99ee5-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="99ee5-105">SYNTAX</span></span>

### <span data-ttu-id="99ee5-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="99ee5-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ee5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99ee5-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ee5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99ee5-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99ee5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="99ee5-109">DESCRIPTION</span></span>
<span data-ttu-id="99ee5-110">Atualiza o Sql StoredProcedure do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="99ee5-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="99ee5-111">Executa uma operação de patch do lado do cliente lendo o StoredProcedure existente.</span><span class="sxs-lookup"><span data-stu-id="99ee5-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="99ee5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99ee5-112">EXAMPLES</span></span>

### <span data-ttu-id="99ee5-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99ee5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="99ee5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="99ee5-114">PARAMETERS</span></span>

### <span data-ttu-id="99ee5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="99ee5-115">-AccountName</span></span>
<span data-ttu-id="99ee5-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="99ee5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="99ee5-117">-Body</span><span class="sxs-lookup"><span data-stu-id="99ee5-117">-Body</span></span>
<span data-ttu-id="99ee5-118">O corpo do Procedimento Armazenado.</span><span class="sxs-lookup"><span data-stu-id="99ee5-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="99ee5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99ee5-119">-Confirm</span></span>
<span data-ttu-id="99ee5-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99ee5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ee5-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="99ee5-121">-ContainerName</span></span>
<span data-ttu-id="99ee5-122">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="99ee5-122">Container name.</span></span>

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

### <span data-ttu-id="99ee5-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="99ee5-123">-DatabaseName</span></span>
<span data-ttu-id="99ee5-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="99ee5-124">Database name.</span></span>

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

### <span data-ttu-id="99ee5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ee5-125">-DefaultProfile</span></span>
<span data-ttu-id="99ee5-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99ee5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99ee5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99ee5-127">-InputObject</span></span>
<span data-ttu-id="99ee5-128">Objeto Sql Stored Procedure</span><span class="sxs-lookup"><span data-stu-id="99ee5-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99ee5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="99ee5-129">-Name</span></span>
<span data-ttu-id="99ee5-130">Nome de Prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="99ee5-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="99ee5-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="99ee5-131">-ParentObject</span></span>
<span data-ttu-id="99ee5-132">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="99ee5-132">Sql Container object.</span></span>

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

### <span data-ttu-id="99ee5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ee5-133">-ResourceGroupName</span></span>
<span data-ttu-id="99ee5-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99ee5-134">Name of resource group.</span></span>

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

### <span data-ttu-id="99ee5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ee5-135">-WhatIf</span></span>
<span data-ttu-id="99ee5-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99ee5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ee5-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99ee5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ee5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ee5-138">CommonParameters</span></span>
<span data-ttu-id="99ee5-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ee5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ee5-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99ee5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ee5-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99ee5-141">INPUTS</span></span>

### <span data-ttu-id="99ee5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="99ee5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="99ee5-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="99ee5-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="99ee5-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="99ee5-144">OUTPUTS</span></span>

### <span data-ttu-id="99ee5-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="99ee5-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="99ee5-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="99ee5-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="99ee5-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="99ee5-147">NOTES</span></span>

## <span data-ttu-id="99ee5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99ee5-148">RELATED LINKS</span></span>
