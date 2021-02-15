---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112061"
---
# <span data-ttu-id="61867-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="61867-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="61867-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61867-102">SYNOPSIS</span></span>
<span data-ttu-id="61867-103">Obtém a Função Definida pelo Usuário sql do Sql.</span><span class="sxs-lookup"><span data-stu-id="61867-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="61867-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61867-104">SYNTAX</span></span>

### <span data-ttu-id="61867-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61867-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61867-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61867-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61867-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="61867-107">DESCRIPTION</span></span>
<span data-ttu-id="61867-108">O cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** obtém a lista de todos os existentes Do Sql UserDefinedFunctions do Sql Para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e obtém um único UserDefinedFunction sql do Sql Sql Para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="61867-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="61867-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61867-109">EXAMPLES</span></span>

### <span data-ttu-id="61867-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61867-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="61867-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61867-111">PARAMETERS</span></span>

### <span data-ttu-id="61867-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="61867-112">-AccountName</span></span>
<span data-ttu-id="61867-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="61867-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="61867-114">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="61867-114">-ContainerName</span></span>
<span data-ttu-id="61867-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="61867-115">Container name.</span></span>

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

### <span data-ttu-id="61867-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="61867-116">-DatabaseName</span></span>
<span data-ttu-id="61867-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="61867-117">Database name.</span></span>

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

### <span data-ttu-id="61867-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61867-118">-DefaultProfile</span></span>
<span data-ttu-id="61867-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61867-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61867-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="61867-120">-Name</span></span>
<span data-ttu-id="61867-121">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="61867-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="61867-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="61867-122">-ParentObject</span></span>
<span data-ttu-id="61867-123">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="61867-123">Sql Container object.</span></span>

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

### <span data-ttu-id="61867-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61867-124">-ResourceGroupName</span></span>
<span data-ttu-id="61867-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61867-125">Name of resource group.</span></span>

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

### <span data-ttu-id="61867-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61867-126">CommonParameters</span></span>
<span data-ttu-id="61867-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61867-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61867-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61867-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61867-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="61867-129">INPUTS</span></span>

### <span data-ttu-id="61867-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61867-130">None</span></span>

## <span data-ttu-id="61867-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="61867-131">OUTPUTS</span></span>

### <span data-ttu-id="61867-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="61867-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="61867-133">Notas</span><span class="sxs-lookup"><span data-stu-id="61867-133">NOTES</span></span>

## <span data-ttu-id="61867-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61867-134">RELATED LINKS</span></span>
