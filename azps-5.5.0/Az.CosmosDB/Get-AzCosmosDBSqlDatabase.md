---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116470"
---
# <span data-ttu-id="d271a-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d271a-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d271a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d271a-102">SYNOPSIS</span></span>
<span data-ttu-id="d271a-103">Obtém o Banco de Dados Sql do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="d271a-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d271a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d271a-104">SYNTAX</span></span>

### <span data-ttu-id="d271a-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d271a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d271a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d271a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d271a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d271a-107">DESCRIPTION</span></span>
<span data-ttu-id="d271a-108">O cmdlet **Get-AzCosmosDBSqlDatabase** obtém a lista de todos os Bancos de Dados Sql do Sql Do Sql Do Sql existentes para um determinado ResourceGroupName, AccountName e obtém um único Banco de Dados Sql do Sql Do Sql de Um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="d271a-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="d271a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d271a-109">EXAMPLES</span></span>

### <span data-ttu-id="d271a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d271a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="d271a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d271a-111">PARAMETERS</span></span>

### <span data-ttu-id="d271a-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="d271a-112">-AccountName</span></span>
<span data-ttu-id="d271a-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="d271a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d271a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d271a-114">-DefaultProfile</span></span>
<span data-ttu-id="d271a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d271a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d271a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d271a-116">-Name</span></span>
<span data-ttu-id="d271a-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d271a-117">Database name.</span></span>

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

### <span data-ttu-id="d271a-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d271a-118">-ParentObject</span></span>
<span data-ttu-id="d271a-119">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="d271a-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d271a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d271a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d271a-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d271a-121">Name of resource group.</span></span>

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

### <span data-ttu-id="d271a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d271a-122">CommonParameters</span></span>
<span data-ttu-id="d271a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d271a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d271a-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d271a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d271a-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="d271a-125">INPUTS</span></span>

### <span data-ttu-id="d271a-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d271a-126">None</span></span>

## <span data-ttu-id="d271a-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="d271a-127">OUTPUTS</span></span>

### <span data-ttu-id="d271a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d271a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="d271a-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d271a-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d271a-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d271a-130">NOTES</span></span>

## <span data-ttu-id="d271a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d271a-131">RELATED LINKS</span></span>
