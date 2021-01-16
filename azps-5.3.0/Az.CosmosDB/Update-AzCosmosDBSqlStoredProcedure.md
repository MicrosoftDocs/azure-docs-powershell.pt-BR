---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434007"
---
# <span data-ttu-id="5e58e-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="5e58e-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="5e58e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e58e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e58e-103">Atualiza o StoredProcedure do SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5e58e-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="5e58e-104">Executa uma operação de patch do lado do cliente lendo o StoredProcedure existente.</span><span class="sxs-lookup"><span data-stu-id="5e58e-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="5e58e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e58e-105">SYNTAX</span></span>

### <span data-ttu-id="5e58e-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e58e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e58e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e58e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e58e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e58e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e58e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e58e-109">DESCRIPTION</span></span>
<span data-ttu-id="5e58e-110">Atualiza o StoredProcedure do SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5e58e-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="5e58e-111">Executa uma operação de patch do lado do cliente lendo o StoredProcedure existente.</span><span class="sxs-lookup"><span data-stu-id="5e58e-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="5e58e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e58e-112">EXAMPLES</span></span>

### <span data-ttu-id="5e58e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e58e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="5e58e-114">OS</span><span class="sxs-lookup"><span data-stu-id="5e58e-114">PARAMETERS</span></span>

### <span data-ttu-id="5e58e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e58e-115">-AccountName</span></span>
<span data-ttu-id="5e58e-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="5e58e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e58e-117">-Corpo</span><span class="sxs-lookup"><span data-stu-id="5e58e-117">-Body</span></span>
<span data-ttu-id="5e58e-118">O corpo do procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="5e58e-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="5e58e-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e58e-119">-Confirm</span></span>
<span data-ttu-id="5e58e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e58e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e58e-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5e58e-121">-ContainerName</span></span>
<span data-ttu-id="5e58e-122">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="5e58e-122">Container name.</span></span>

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

### <span data-ttu-id="5e58e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e58e-123">-DatabaseName</span></span>
<span data-ttu-id="5e58e-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5e58e-124">Database name.</span></span>

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

### <span data-ttu-id="5e58e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e58e-125">-DefaultProfile</span></span>
<span data-ttu-id="5e58e-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e58e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e58e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e58e-127">-InputObject</span></span>
<span data-ttu-id="5e58e-128">Objeto de procedimento armazenado SQL</span><span class="sxs-lookup"><span data-stu-id="5e58e-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="5e58e-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e58e-129">-Name</span></span>
<span data-ttu-id="5e58e-130">Nome Prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="5e58e-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="5e58e-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e58e-131">-ParentObject</span></span>
<span data-ttu-id="5e58e-132">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="5e58e-132">Sql Container object.</span></span>

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

### <span data-ttu-id="5e58e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e58e-133">-ResourceGroupName</span></span>
<span data-ttu-id="5e58e-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e58e-134">Name of resource group.</span></span>

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

### <span data-ttu-id="5e58e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e58e-135">-WhatIf</span></span>
<span data-ttu-id="5e58e-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e58e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e58e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e58e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e58e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e58e-138">CommonParameters</span></span>
<span data-ttu-id="5e58e-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e58e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e58e-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e58e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e58e-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e58e-141">INPUTS</span></span>

### <span data-ttu-id="5e58e-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="5e58e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="5e58e-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="5e58e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="5e58e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e58e-144">OUTPUTS</span></span>

### <span data-ttu-id="5e58e-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="5e58e-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="5e58e-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="5e58e-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="5e58e-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e58e-147">NOTES</span></span>

## <span data-ttu-id="5e58e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e58e-148">RELATED LINKS</span></span>
