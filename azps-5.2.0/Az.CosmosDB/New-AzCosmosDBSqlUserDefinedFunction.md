---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259322"
---
# <span data-ttu-id="4b6a3-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="4b6a3-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="4b6a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6a3-103">Cria um novo CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="4b6a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b6a3-104">SYNTAX</span></span>

### <span data-ttu-id="4b6a3-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b6a3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b6a3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b6a3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b6a3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b6a3-107">DESCRIPTION</span></span>
<span data-ttu-id="4b6a3-108">Cria um novo CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="4b6a3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b6a3-109">EXAMPLES</span></span>

### <span data-ttu-id="4b6a3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b6a3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="4b6a3-111">OS</span><span class="sxs-lookup"><span data-stu-id="4b6a3-111">PARAMETERS</span></span>

### <span data-ttu-id="4b6a3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4b6a3-112">-AccountName</span></span>
<span data-ttu-id="4b6a3-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4b6a3-114">-Corpo</span><span class="sxs-lookup"><span data-stu-id="4b6a3-114">-Body</span></span>
<span data-ttu-id="4b6a3-115">O corpo da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="4b6a3-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b6a3-116">-Confirm</span></span>
<span data-ttu-id="4b6a3-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b6a3-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4b6a3-118">-ContainerName</span></span>
<span data-ttu-id="4b6a3-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-119">Container name.</span></span>

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

### <span data-ttu-id="4b6a3-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b6a3-120">-DatabaseName</span></span>
<span data-ttu-id="4b6a3-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-121">Database name.</span></span>

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

### <span data-ttu-id="4b6a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6a3-122">-DefaultProfile</span></span>
<span data-ttu-id="4b6a3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b6a3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b6a3-124">-Name</span></span>
<span data-ttu-id="4b6a3-125">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="4b6a3-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4b6a3-126">-ParentObject</span></span>
<span data-ttu-id="4b6a3-127">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-127">Sql Container object.</span></span>

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

### <span data-ttu-id="4b6a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b6a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="4b6a3-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-129">Name of resource group.</span></span>

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

### <span data-ttu-id="4b6a3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b6a3-130">-WhatIf</span></span>
<span data-ttu-id="4b6a3-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b6a3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b6a3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6a3-133">CommonParameters</span></span>
<span data-ttu-id="4b6a3-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6a3-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b6a3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6a3-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b6a3-136">INPUTS</span></span>

### <span data-ttu-id="4b6a3-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="4b6a3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="4b6a3-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b6a3-138">OUTPUTS</span></span>

### <span data-ttu-id="4b6a3-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="4b6a3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="4b6a3-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="4b6a3-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="4b6a3-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b6a3-141">NOTES</span></span>

## <span data-ttu-id="4b6a3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b6a3-142">RELATED LINKS</span></span>
