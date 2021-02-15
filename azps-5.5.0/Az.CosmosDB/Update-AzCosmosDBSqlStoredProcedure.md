---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112022"
---
# <span data-ttu-id="e60b2-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="e60b2-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="e60b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e60b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e60b2-103">Atualiza o Sql StoredProcedure do SqlDb.</span><span class="sxs-lookup"><span data-stu-id="e60b2-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="e60b2-104">Executa uma operação de patch do lado do cliente lendo o StoredProcedure existente.</span><span class="sxs-lookup"><span data-stu-id="e60b2-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="e60b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e60b2-105">SYNTAX</span></span>

### <span data-ttu-id="e60b2-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e60b2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e60b2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e60b2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e60b2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e60b2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e60b2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e60b2-109">DESCRIPTION</span></span>
<span data-ttu-id="e60b2-110">Atualiza o Sql StoredProcedure do SqlDb.</span><span class="sxs-lookup"><span data-stu-id="e60b2-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="e60b2-111">Executa uma operação de patch do lado do cliente lendo o StoredProcedure existente.</span><span class="sxs-lookup"><span data-stu-id="e60b2-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="e60b2-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e60b2-112">EXAMPLES</span></span>

### <span data-ttu-id="e60b2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e60b2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="e60b2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e60b2-114">PARAMETERS</span></span>

### <span data-ttu-id="e60b2-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="e60b2-115">-AccountName</span></span>
<span data-ttu-id="e60b2-116">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="e60b2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e60b2-117">-Corpo</span><span class="sxs-lookup"><span data-stu-id="e60b2-117">-Body</span></span>
<span data-ttu-id="e60b2-118">O corpo do Procedimento Armazenado.</span><span class="sxs-lookup"><span data-stu-id="e60b2-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="e60b2-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e60b2-119">-Confirm</span></span>
<span data-ttu-id="e60b2-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e60b2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e60b2-121">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="e60b2-121">-ContainerName</span></span>
<span data-ttu-id="e60b2-122">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e60b2-122">Container name.</span></span>

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

### <span data-ttu-id="e60b2-123">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="e60b2-123">-DatabaseName</span></span>
<span data-ttu-id="e60b2-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e60b2-124">Database name.</span></span>

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

### <span data-ttu-id="e60b2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60b2-125">-DefaultProfile</span></span>
<span data-ttu-id="e60b2-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e60b2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e60b2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e60b2-127">-InputObject</span></span>
<span data-ttu-id="e60b2-128">Objeto procedimento armazenado do Sql</span><span class="sxs-lookup"><span data-stu-id="e60b2-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="e60b2-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e60b2-129">-Name</span></span>
<span data-ttu-id="e60b2-130">Nome prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="e60b2-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="e60b2-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e60b2-131">-ParentObject</span></span>
<span data-ttu-id="e60b2-132">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="e60b2-132">Sql Container object.</span></span>

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

### <span data-ttu-id="e60b2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e60b2-133">-ResourceGroupName</span></span>
<span data-ttu-id="e60b2-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e60b2-134">Name of resource group.</span></span>

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

### <span data-ttu-id="e60b2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e60b2-135">-WhatIf</span></span>
<span data-ttu-id="e60b2-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e60b2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e60b2-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e60b2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e60b2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60b2-138">CommonParameters</span></span>
<span data-ttu-id="e60b2-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e60b2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60b2-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e60b2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60b2-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="e60b2-141">INPUTS</span></span>

### <span data-ttu-id="e60b2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e60b2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="e60b2-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedGetResults</span><span class="sxs-lookup"><span data-stu-id="e60b2-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="e60b2-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="e60b2-144">OUTPUTS</span></span>

### <span data-ttu-id="e60b2-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedGetResults</span><span class="sxs-lookup"><span data-stu-id="e60b2-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="e60b2-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e60b2-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e60b2-147">Notas</span><span class="sxs-lookup"><span data-stu-id="e60b2-147">NOTES</span></span>

## <span data-ttu-id="e60b2-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e60b2-148">RELATED LINKS</span></span>
