---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: c8cfb1077f418c9d671729cb0ff762141a7b77c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777534"
---
# <span data-ttu-id="73e40-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="73e40-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="73e40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73e40-102">SYNOPSIS</span></span>
<span data-ttu-id="73e40-103">Obtém a função definida pelo usuário SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="73e40-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="73e40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73e40-104">SYNTAX</span></span>

### <span data-ttu-id="73e40-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73e40-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73e40-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73e40-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73e40-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73e40-107">DESCRIPTION</span></span>
<span data-ttu-id="73e40-108">O cmdlet **Get-AzCosmosDBSqlUserDefinedFunction** Obtém a lista de todos os CosmosDB SQL UserDefinedFunctions existentes para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e Obtém um único CosmosDB SQL UserDefinedFunction para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e UserDefinedFunctionName.</span><span class="sxs-lookup"><span data-stu-id="73e40-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="73e40-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73e40-109">EXAMPLES</span></span>

### <span data-ttu-id="73e40-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73e40-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="73e40-111">OS</span><span class="sxs-lookup"><span data-stu-id="73e40-111">PARAMETERS</span></span>

### <span data-ttu-id="73e40-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="73e40-112">-AccountName</span></span>
<span data-ttu-id="73e40-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="73e40-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="73e40-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="73e40-114">-ContainerName</span></span>
<span data-ttu-id="73e40-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="73e40-115">Container name.</span></span>

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

### <span data-ttu-id="73e40-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73e40-116">-DatabaseName</span></span>
<span data-ttu-id="73e40-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="73e40-117">Database name.</span></span>

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

### <span data-ttu-id="73e40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e40-118">-DefaultProfile</span></span>
<span data-ttu-id="73e40-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73e40-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73e40-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73e40-120">-InputObject</span></span>
<span data-ttu-id="73e40-121">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="73e40-121">Sql Container object.</span></span>

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

### <span data-ttu-id="73e40-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="73e40-122">-Name</span></span>
<span data-ttu-id="73e40-123">Nome da função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="73e40-123">User Defined Function Name.</span></span>

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

### <span data-ttu-id="73e40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e40-124">-ResourceGroupName</span></span>
<span data-ttu-id="73e40-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73e40-125">Name of resource group.</span></span>

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

### <span data-ttu-id="73e40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e40-126">CommonParameters</span></span>
<span data-ttu-id="73e40-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73e40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e40-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73e40-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e40-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73e40-129">INPUTS</span></span>

### <span data-ttu-id="73e40-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="73e40-130">None</span></span>

## <span data-ttu-id="73e40-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73e40-131">OUTPUTS</span></span>

### <span data-ttu-id="73e40-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="73e40-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="73e40-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73e40-133">NOTES</span></span>

## <span data-ttu-id="73e40-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73e40-134">RELATED LINKS</span></span>
