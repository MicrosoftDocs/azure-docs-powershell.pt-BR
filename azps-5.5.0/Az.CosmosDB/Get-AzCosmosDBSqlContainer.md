---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117795"
---
# <span data-ttu-id="87f90-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="87f90-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="87f90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87f90-102">SYNOPSIS</span></span>
<span data-ttu-id="87f90-103">Obtém o Contêiner Sql do Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="87f90-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="87f90-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87f90-104">SYNTAX</span></span>

### <span data-ttu-id="87f90-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="87f90-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="87f90-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87f90-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87f90-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="87f90-107">DESCRIPTION</span></span>
<span data-ttu-id="87f90-108">O cmdlet **Get-AzCosmosDBSqlContainer** obtém a lista de todos os Contêineres Sql do Sql Do Sql existentes para um determinado ResourceGroupName, AccountName e DatabaseName e obtém um único Contêiner Sql Do Sql Do Sql DoLMDB para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="87f90-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="87f90-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87f90-109">EXAMPLES</span></span>

### <span data-ttu-id="87f90-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="87f90-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="87f90-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87f90-111">PARAMETERS</span></span>

### <span data-ttu-id="87f90-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="87f90-112">-AccountName</span></span>
<span data-ttu-id="87f90-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="87f90-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="87f90-114">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="87f90-114">-DatabaseName</span></span>
<span data-ttu-id="87f90-115">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87f90-115">Database name.</span></span>

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

### <span data-ttu-id="87f90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f90-116">-DefaultProfile</span></span>
<span data-ttu-id="87f90-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87f90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87f90-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="87f90-118">-Name</span></span>
<span data-ttu-id="87f90-119">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="87f90-119">Container name.</span></span>

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

### <span data-ttu-id="87f90-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="87f90-120">-ParentObject</span></span>
<span data-ttu-id="87f90-121">Objeto banco de dados sql.</span><span class="sxs-lookup"><span data-stu-id="87f90-121">Sql Database object.</span></span>

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

### <span data-ttu-id="87f90-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f90-122">-ResourceGroupName</span></span>
<span data-ttu-id="87f90-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="87f90-123">Name of resource group.</span></span>

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

### <span data-ttu-id="87f90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f90-124">CommonParameters</span></span>
<span data-ttu-id="87f90-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87f90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f90-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87f90-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f90-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="87f90-127">INPUTS</span></span>

### <span data-ttu-id="87f90-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87f90-128">None</span></span>

## <span data-ttu-id="87f90-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="87f90-129">OUTPUTS</span></span>

### <span data-ttu-id="87f90-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="87f90-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="87f90-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="87f90-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="87f90-132">Notas</span><span class="sxs-lookup"><span data-stu-id="87f90-132">NOTES</span></span>

## <span data-ttu-id="87f90-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87f90-133">RELATED LINKS</span></span>
