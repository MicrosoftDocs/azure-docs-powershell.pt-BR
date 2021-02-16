---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117787"
---
# <span data-ttu-id="46253-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="46253-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="46253-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46253-102">SYNOPSIS</span></span>
<span data-ttu-id="46253-103">Cria um novo Sql UserDefinedFunction do Sql.</span><span class="sxs-lookup"><span data-stu-id="46253-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="46253-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46253-104">SYNTAX</span></span>

### <span data-ttu-id="46253-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46253-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46253-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46253-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46253-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="46253-107">DESCRIPTION</span></span>
<span data-ttu-id="46253-108">Cria um novo Sql UserDefinedFunction do Sql.</span><span class="sxs-lookup"><span data-stu-id="46253-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="46253-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46253-109">EXAMPLES</span></span>

### <span data-ttu-id="46253-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46253-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="46253-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46253-111">PARAMETERS</span></span>

### <span data-ttu-id="46253-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="46253-112">-AccountName</span></span>
<span data-ttu-id="46253-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="46253-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46253-114">-Corpo</span><span class="sxs-lookup"><span data-stu-id="46253-114">-Body</span></span>
<span data-ttu-id="46253-115">O corpo da Função Definida pelo Usuário.</span><span class="sxs-lookup"><span data-stu-id="46253-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="46253-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="46253-116">-Confirm</span></span>
<span data-ttu-id="46253-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46253-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46253-118">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="46253-118">-ContainerName</span></span>
<span data-ttu-id="46253-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="46253-119">Container name.</span></span>

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

### <span data-ttu-id="46253-120">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="46253-120">-DatabaseName</span></span>
<span data-ttu-id="46253-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="46253-121">Database name.</span></span>

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

### <span data-ttu-id="46253-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46253-122">-DefaultProfile</span></span>
<span data-ttu-id="46253-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46253-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46253-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="46253-124">-Name</span></span>
<span data-ttu-id="46253-125">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="46253-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="46253-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="46253-126">-ParentObject</span></span>
<span data-ttu-id="46253-127">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="46253-127">Sql Container object.</span></span>

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

### <span data-ttu-id="46253-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46253-128">-ResourceGroupName</span></span>
<span data-ttu-id="46253-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46253-129">Name of resource group.</span></span>

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

### <span data-ttu-id="46253-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46253-130">-WhatIf</span></span>
<span data-ttu-id="46253-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="46253-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46253-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46253-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46253-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46253-133">CommonParameters</span></span>
<span data-ttu-id="46253-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46253-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46253-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46253-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46253-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="46253-136">INPUTS</span></span>

### <span data-ttu-id="46253-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="46253-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="46253-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="46253-138">OUTPUTS</span></span>

### <span data-ttu-id="46253-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="46253-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="46253-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="46253-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="46253-141">Notas</span><span class="sxs-lookup"><span data-stu-id="46253-141">NOTES</span></span>

## <span data-ttu-id="46253-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46253-142">RELATED LINKS</span></span>
