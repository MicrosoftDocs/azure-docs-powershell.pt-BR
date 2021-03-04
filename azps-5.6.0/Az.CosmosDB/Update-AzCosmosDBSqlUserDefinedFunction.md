---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: d1f4e4c5c48e33a1b3c2ac882b0c561bb50f9bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892864"
---
# <span data-ttu-id="1b1f2-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="1b1f2-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="1b1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1f2-103">Atualiza o UserDefinedFunction do Sql Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="1b1f2-104">Executa uma operação de patch do lado do cliente lendo o UserDefinedFunction existente.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="1b1f2-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1b1f2-105">SYNTAX</span></span>

### <span data-ttu-id="1b1f2-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1b1f2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b1f2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b1f2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b1f2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b1f2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b1f2-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1b1f2-109">DESCRIPTION</span></span>
<span data-ttu-id="1b1f2-110">Atualiza o UserDefinedFunction do Sql Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="1b1f2-111">Executa uma operação de patch do lado do cliente lendo o UserDefinedFunction existente.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="1b1f2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b1f2-112">EXAMPLES</span></span>

### <span data-ttu-id="1b1f2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b1f2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="1b1f2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1b1f2-114">PARAMETERS</span></span>

### <span data-ttu-id="1b1f2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b1f2-115">-AccountName</span></span>
<span data-ttu-id="1b1f2-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1b1f2-117">-Body</span><span class="sxs-lookup"><span data-stu-id="1b1f2-117">-Body</span></span>
<span data-ttu-id="1b1f2-118">O corpo da Função Definida pelo Usuário.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="1b1f2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b1f2-119">-Confirm</span></span>
<span data-ttu-id="1b1f2-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b1f2-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1b1f2-121">-ContainerName</span></span>
<span data-ttu-id="1b1f2-122">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-122">Container name.</span></span>

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

### <span data-ttu-id="1b1f2-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b1f2-123">-DatabaseName</span></span>
<span data-ttu-id="1b1f2-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-124">Database name.</span></span>

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

### <span data-ttu-id="1b1f2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1f2-125">-DefaultProfile</span></span>
<span data-ttu-id="1b1f2-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b1f2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b1f2-127">-InputObject</span></span>
<span data-ttu-id="1b1f2-128">Objeto de função definida pelo usuário sql</span><span class="sxs-lookup"><span data-stu-id="1b1f2-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1f2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1b1f2-129">-Name</span></span>
<span data-ttu-id="1b1f2-130">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="1b1f2-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1b1f2-131">-ParentObject</span></span>
<span data-ttu-id="1b1f2-132">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-132">Sql Container object.</span></span>

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

### <span data-ttu-id="1b1f2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1f2-133">-ResourceGroupName</span></span>
<span data-ttu-id="1b1f2-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-134">Name of resource group.</span></span>

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

### <span data-ttu-id="1b1f2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b1f2-135">-WhatIf</span></span>
<span data-ttu-id="1b1f2-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b1f2-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b1f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1f2-138">CommonParameters</span></span>
<span data-ttu-id="1b1f2-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1f2-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b1f2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1f2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b1f2-141">INPUTS</span></span>

### <span data-ttu-id="1b1f2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="1b1f2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="1b1f2-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="1b1f2-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="1b1f2-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1b1f2-144">OUTPUTS</span></span>

### <span data-ttu-id="1b1f2-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="1b1f2-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="1b1f2-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1b1f2-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1b1f2-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="1b1f2-147">NOTES</span></span>

## <span data-ttu-id="1b1f2-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b1f2-148">RELATED LINKS</span></span>
