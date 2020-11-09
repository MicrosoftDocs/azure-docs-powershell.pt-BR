---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281284"
---
# <span data-ttu-id="29c29-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="29c29-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="29c29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29c29-102">SYNOPSIS</span></span>
<span data-ttu-id="29c29-103">Cria um novo CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="29c29-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="29c29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29c29-104">SYNTAX</span></span>

### <span data-ttu-id="29c29-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="29c29-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c29-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29c29-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c29-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29c29-107">DESCRIPTION</span></span>
<span data-ttu-id="29c29-108">Cria um novo CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="29c29-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="29c29-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29c29-109">EXAMPLES</span></span>

### <span data-ttu-id="29c29-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29c29-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="29c29-111">OS</span><span class="sxs-lookup"><span data-stu-id="29c29-111">PARAMETERS</span></span>

### <span data-ttu-id="29c29-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="29c29-112">-AccountName</span></span>
<span data-ttu-id="29c29-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="29c29-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="29c29-114">-Corpo</span><span class="sxs-lookup"><span data-stu-id="29c29-114">-Body</span></span>
<span data-ttu-id="29c29-115">O corpo da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="29c29-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="29c29-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29c29-116">-Confirm</span></span>
<span data-ttu-id="29c29-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29c29-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c29-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="29c29-118">-ContainerName</span></span>
<span data-ttu-id="29c29-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="29c29-119">Container name.</span></span>

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

### <span data-ttu-id="29c29-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29c29-120">-DatabaseName</span></span>
<span data-ttu-id="29c29-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="29c29-121">Database name.</span></span>

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

### <span data-ttu-id="29c29-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c29-122">-DefaultProfile</span></span>
<span data-ttu-id="29c29-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29c29-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29c29-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="29c29-124">-Name</span></span>
<span data-ttu-id="29c29-125">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="29c29-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="29c29-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="29c29-126">-ParentObject</span></span>
<span data-ttu-id="29c29-127">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="29c29-127">Sql Container object.</span></span>

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

### <span data-ttu-id="29c29-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c29-128">-ResourceGroupName</span></span>
<span data-ttu-id="29c29-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29c29-129">Name of resource group.</span></span>

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

### <span data-ttu-id="29c29-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c29-130">-WhatIf</span></span>
<span data-ttu-id="29c29-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29c29-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c29-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29c29-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c29-133">CommonParameters</span></span>
<span data-ttu-id="29c29-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c29-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29c29-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c29-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29c29-136">INPUTS</span></span>

### <span data-ttu-id="29c29-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="29c29-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="29c29-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29c29-138">OUTPUTS</span></span>

### <span data-ttu-id="29c29-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="29c29-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="29c29-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="29c29-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="29c29-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29c29-141">NOTES</span></span>

## <span data-ttu-id="29c29-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29c29-142">RELATED LINKS</span></span>
