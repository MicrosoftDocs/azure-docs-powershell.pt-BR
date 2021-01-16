---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260277"
---
# <span data-ttu-id="bf0f5-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="bf0f5-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="bf0f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0f5-103">Atualiza o CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="bf0f5-104">Executa uma operação de patch do lado do cliente lendo o UserDefinedFunction existente.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="bf0f5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf0f5-105">SYNTAX</span></span>

### <span data-ttu-id="bf0f5-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf0f5-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf0f5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf0f5-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf0f5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf0f5-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf0f5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf0f5-109">DESCRIPTION</span></span>
<span data-ttu-id="bf0f5-110">Atualiza o CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="bf0f5-111">Executa uma operação de patch do lado do cliente lendo o UserDefinedFunction existente.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="bf0f5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf0f5-112">EXAMPLES</span></span>

### <span data-ttu-id="bf0f5-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf0f5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="bf0f5-114">OS</span><span class="sxs-lookup"><span data-stu-id="bf0f5-114">PARAMETERS</span></span>

### <span data-ttu-id="bf0f5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf0f5-115">-AccountName</span></span>
<span data-ttu-id="bf0f5-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bf0f5-117">-Corpo</span><span class="sxs-lookup"><span data-stu-id="bf0f5-117">-Body</span></span>
<span data-ttu-id="bf0f5-118">O corpo da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="bf0f5-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf0f5-119">-Confirm</span></span>
<span data-ttu-id="bf0f5-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf0f5-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bf0f5-121">-ContainerName</span></span>
<span data-ttu-id="bf0f5-122">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-122">Container name.</span></span>

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

### <span data-ttu-id="bf0f5-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf0f5-123">-DatabaseName</span></span>
<span data-ttu-id="bf0f5-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-124">Database name.</span></span>

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

### <span data-ttu-id="bf0f5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0f5-125">-DefaultProfile</span></span>
<span data-ttu-id="bf0f5-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0f5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf0f5-127">-InputObject</span></span>
<span data-ttu-id="bf0f5-128">Objeto de função definido pelo usuário SQL</span><span class="sxs-lookup"><span data-stu-id="bf0f5-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="bf0f5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf0f5-129">-Name</span></span>
<span data-ttu-id="bf0f5-130">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="bf0f5-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf0f5-131">-ParentObject</span></span>
<span data-ttu-id="bf0f5-132">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-132">Sql Container object.</span></span>

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

### <span data-ttu-id="bf0f5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0f5-133">-ResourceGroupName</span></span>
<span data-ttu-id="bf0f5-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-134">Name of resource group.</span></span>

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

### <span data-ttu-id="bf0f5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf0f5-135">-WhatIf</span></span>
<span data-ttu-id="bf0f5-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf0f5-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf0f5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0f5-138">CommonParameters</span></span>
<span data-ttu-id="bf0f5-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf0f5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0f5-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf0f5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0f5-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf0f5-141">INPUTS</span></span>

### <span data-ttu-id="bf0f5-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="bf0f5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="bf0f5-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="bf0f5-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="bf0f5-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf0f5-144">OUTPUTS</span></span>

### <span data-ttu-id="bf0f5-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="bf0f5-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="bf0f5-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="bf0f5-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="bf0f5-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf0f5-147">NOTES</span></span>

## <span data-ttu-id="bf0f5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf0f5-148">RELATED LINKS</span></span>
