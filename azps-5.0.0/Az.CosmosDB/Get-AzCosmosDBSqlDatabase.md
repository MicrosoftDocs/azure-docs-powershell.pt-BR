---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281379"
---
# <span data-ttu-id="110a6-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="110a6-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="110a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="110a6-102">SYNOPSIS</span></span>
<span data-ttu-id="110a6-103">Obtém o banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="110a6-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="110a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="110a6-104">SYNTAX</span></span>

### <span data-ttu-id="110a6-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="110a6-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="110a6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="110a6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="110a6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="110a6-107">DESCRIPTION</span></span>
<span data-ttu-id="110a6-108">O cmdlet **Get-AzCosmosDBSqlDatabase** Obtém a lista de todos os bancos de dados SQL existentes do CosmosDB para um determinado ResourceGroupName, AccountName e Obtém um único banco de dados SQL CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="110a6-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="110a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="110a6-109">EXAMPLES</span></span>

### <span data-ttu-id="110a6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="110a6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="110a6-111">OS</span><span class="sxs-lookup"><span data-stu-id="110a6-111">PARAMETERS</span></span>

### <span data-ttu-id="110a6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="110a6-112">-AccountName</span></span>
<span data-ttu-id="110a6-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="110a6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="110a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110a6-114">-DefaultProfile</span></span>
<span data-ttu-id="110a6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="110a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="110a6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="110a6-116">-Name</span></span>
<span data-ttu-id="110a6-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="110a6-117">Database name.</span></span>

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

### <span data-ttu-id="110a6-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="110a6-118">-ParentObject</span></span>
<span data-ttu-id="110a6-119">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="110a6-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="110a6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="110a6-120">-ResourceGroupName</span></span>
<span data-ttu-id="110a6-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="110a6-121">Name of resource group.</span></span>

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

### <span data-ttu-id="110a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110a6-122">CommonParameters</span></span>
<span data-ttu-id="110a6-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="110a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110a6-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="110a6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110a6-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="110a6-125">INPUTS</span></span>

### <span data-ttu-id="110a6-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="110a6-126">None</span></span>

## <span data-ttu-id="110a6-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="110a6-127">OUTPUTS</span></span>

### <span data-ttu-id="110a6-128">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="110a6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="110a6-129">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="110a6-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="110a6-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="110a6-130">NOTES</span></span>

## <span data-ttu-id="110a6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="110a6-131">RELATED LINKS</span></span>
