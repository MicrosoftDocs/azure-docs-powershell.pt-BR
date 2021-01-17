---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434093"
---
# <span data-ttu-id="c1df9-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="c1df9-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="c1df9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1df9-102">SYNOPSIS</span></span>
<span data-ttu-id="c1df9-103">Obtém o contêiner SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c1df9-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c1df9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1df9-104">SYNTAX</span></span>

### <span data-ttu-id="c1df9-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1df9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="c1df9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1df9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1df9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1df9-107">DESCRIPTION</span></span>
<span data-ttu-id="c1df9-108">O cmdlet **Get-AzCosmosDBSqlContainer** Obtém a lista de todos os contêineres SQL existentes do CosmosDB para um determinado ResourceGroupName, AccountName e DatabaseName e Obtém um contêiner SQL único CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="c1df9-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="c1df9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1df9-109">EXAMPLES</span></span>

### <span data-ttu-id="c1df9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1df9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="c1df9-111">OS</span><span class="sxs-lookup"><span data-stu-id="c1df9-111">PARAMETERS</span></span>

### <span data-ttu-id="c1df9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1df9-112">-AccountName</span></span>
<span data-ttu-id="c1df9-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c1df9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c1df9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c1df9-114">-DatabaseName</span></span>
<span data-ttu-id="c1df9-115">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c1df9-115">Database name.</span></span>

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

### <span data-ttu-id="c1df9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1df9-116">-DefaultProfile</span></span>
<span data-ttu-id="c1df9-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1df9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1df9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1df9-118">-Name</span></span>
<span data-ttu-id="c1df9-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c1df9-119">Container name.</span></span>

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

### <span data-ttu-id="c1df9-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c1df9-120">-ParentObject</span></span>
<span data-ttu-id="c1df9-121">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="c1df9-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1df9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1df9-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1df9-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c1df9-123">Name of resource group.</span></span>

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

### <span data-ttu-id="c1df9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1df9-124">CommonParameters</span></span>
<span data-ttu-id="c1df9-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1df9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1df9-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1df9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1df9-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1df9-127">INPUTS</span></span>

### <span data-ttu-id="c1df9-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c1df9-128">None</span></span>

## <span data-ttu-id="c1df9-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1df9-129">OUTPUTS</span></span>

### <span data-ttu-id="c1df9-130">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="c1df9-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="c1df9-131">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c1df9-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c1df9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1df9-132">NOTES</span></span>

## <span data-ttu-id="c1df9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1df9-133">RELATED LINKS</span></span>
