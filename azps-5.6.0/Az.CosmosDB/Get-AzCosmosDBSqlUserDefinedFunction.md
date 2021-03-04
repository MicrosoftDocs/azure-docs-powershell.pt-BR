---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 0d422014d3cf2ca2ffa18b60c10b50b21bf91144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889794"
---
# <span data-ttu-id="9db18-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="9db18-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="9db18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9db18-102">SYNOPSIS</span></span>
<span data-ttu-id="9db18-103">Obtém a Função Definida do Usuário Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9db18-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="9db18-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9db18-104">SYNTAX</span></span>

### <span data-ttu-id="9db18-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9db18-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9db18-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9db18-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9db18-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9db18-107">DESCRIPTION</span></span>
<span data-ttu-id="9db18-108">O cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** obtém a lista de todos os Usuários Sql Do CosmosDB existentesDefinedFunctions para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e obtém um único Usuário Sql Do CosmosDBDefinedFunction para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="9db18-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="9db18-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9db18-109">EXAMPLES</span></span>

### <span data-ttu-id="9db18-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9db18-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="9db18-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9db18-111">PARAMETERS</span></span>

### <span data-ttu-id="9db18-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9db18-112">-AccountName</span></span>
<span data-ttu-id="9db18-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="9db18-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9db18-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9db18-114">-ContainerName</span></span>
<span data-ttu-id="9db18-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9db18-115">Container name.</span></span>

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

### <span data-ttu-id="9db18-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9db18-116">-DatabaseName</span></span>
<span data-ttu-id="9db18-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9db18-117">Database name.</span></span>

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

### <span data-ttu-id="9db18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db18-118">-DefaultProfile</span></span>
<span data-ttu-id="9db18-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9db18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9db18-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9db18-120">-Name</span></span>
<span data-ttu-id="9db18-121">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9db18-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="9db18-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9db18-122">-ParentObject</span></span>
<span data-ttu-id="9db18-123">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="9db18-123">Sql Container object.</span></span>

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

### <span data-ttu-id="9db18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db18-124">-ResourceGroupName</span></span>
<span data-ttu-id="9db18-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9db18-125">Name of resource group.</span></span>

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

### <span data-ttu-id="9db18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db18-126">CommonParameters</span></span>
<span data-ttu-id="9db18-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db18-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9db18-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db18-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9db18-129">INPUTS</span></span>

### <span data-ttu-id="9db18-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9db18-130">None</span></span>

## <span data-ttu-id="9db18-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9db18-131">OUTPUTS</span></span>

### <span data-ttu-id="9db18-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="9db18-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="9db18-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="9db18-133">NOTES</span></span>

## <span data-ttu-id="9db18-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9db18-134">RELATED LINKS</span></span>
