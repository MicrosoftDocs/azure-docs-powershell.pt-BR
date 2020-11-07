---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944108"
---
# <span data-ttu-id="e0b09-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e0b09-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e0b09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0b09-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b09-103">Obtém o contêiner SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e0b09-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e0b09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0b09-104">SYNTAX</span></span>

### <span data-ttu-id="e0b09-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0b09-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="e0b09-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0b09-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0b09-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0b09-107">DESCRIPTION</span></span>
<span data-ttu-id="e0b09-108">O cmdlet **Get-AzCosmosDBSqlContainer** Obtém a lista de todos os contêineres SQL existentes do CosmosDB para um determinado ResourceGroupName, AccountName e DatabaseName e Obtém um contêiner SQL único CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="e0b09-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="e0b09-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0b09-109">EXAMPLES</span></span>

### <span data-ttu-id="e0b09-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0b09-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="e0b09-111">OS</span><span class="sxs-lookup"><span data-stu-id="e0b09-111">PARAMETERS</span></span>

### <span data-ttu-id="e0b09-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e0b09-112">-AccountName</span></span>
<span data-ttu-id="e0b09-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="e0b09-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e0b09-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e0b09-114">-DatabaseName</span></span>
<span data-ttu-id="e0b09-115">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e0b09-115">Database name.</span></span>

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

### <span data-ttu-id="e0b09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b09-116">-DefaultProfile</span></span>
<span data-ttu-id="e0b09-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b09-118">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="e0b09-118">-Detailed</span></span>
<span data-ttu-id="e0b09-119">Se fornecido, o cmdlet retornará o contêiner com o valor de produtividade.</span><span class="sxs-lookup"><span data-stu-id="e0b09-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b09-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0b09-120">-InputObject</span></span>
<span data-ttu-id="e0b09-121">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e0b09-121">Sql Database object.</span></span>

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

### <span data-ttu-id="e0b09-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0b09-122">-Name</span></span>
<span data-ttu-id="e0b09-123">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e0b09-123">Container name.</span></span>

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

### <span data-ttu-id="e0b09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b09-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0b09-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0b09-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e0b09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b09-126">CommonParameters</span></span>
<span data-ttu-id="e0b09-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b09-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0b09-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b09-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0b09-129">INPUTS</span></span>

### <span data-ttu-id="e0b09-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e0b09-130">None</span></span>

## <span data-ttu-id="e0b09-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0b09-131">OUTPUTS</span></span>

### <span data-ttu-id="e0b09-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e0b09-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="e0b09-133">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e0b09-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e0b09-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0b09-134">NOTES</span></span>

## <span data-ttu-id="e0b09-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0b09-135">RELATED LINKS</span></span>
