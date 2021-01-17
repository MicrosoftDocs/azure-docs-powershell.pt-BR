---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434091"
---
# <span data-ttu-id="8f2d5-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="8f2d5-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="8f2d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2d5-103">Obtém o StoredProcedure do SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="8f2d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f2d5-104">SYNTAX</span></span>

### <span data-ttu-id="8f2d5-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f2d5-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f2d5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f2d5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f2d5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f2d5-107">DESCRIPTION</span></span>
<span data-ttu-id="8f2d5-108">O cmdlet **Get-AzCosmosDBSqlStoredProcedure** Obtém a lista de todos os StoredProcedures SQL existentes do SQL para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e Obtém um único StoredProcedure do SQL de CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e storedprocedurename.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="8f2d5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f2d5-109">EXAMPLES</span></span>

### <span data-ttu-id="8f2d5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f2d5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="8f2d5-111">OS</span><span class="sxs-lookup"><span data-stu-id="8f2d5-111">PARAMETERS</span></span>

### <span data-ttu-id="8f2d5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8f2d5-112">-AccountName</span></span>
<span data-ttu-id="8f2d5-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8f2d5-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8f2d5-114">-ContainerName</span></span>
<span data-ttu-id="8f2d5-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-115">Container name.</span></span>

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

### <span data-ttu-id="8f2d5-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f2d5-116">-DatabaseName</span></span>
<span data-ttu-id="8f2d5-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-117">Database name.</span></span>

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

### <span data-ttu-id="8f2d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2d5-118">-DefaultProfile</span></span>
<span data-ttu-id="8f2d5-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f2d5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f2d5-120">-Name</span></span>
<span data-ttu-id="8f2d5-121">Nome Prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="8f2d5-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8f2d5-122">-ParentObject</span></span>
<span data-ttu-id="8f2d5-123">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-123">Sql Container object.</span></span>

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

### <span data-ttu-id="8f2d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f2d5-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-125">Name of resource group.</span></span>

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

### <span data-ttu-id="8f2d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2d5-126">CommonParameters</span></span>
<span data-ttu-id="8f2d5-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2d5-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f2d5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2d5-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f2d5-129">INPUTS</span></span>

### <span data-ttu-id="8f2d5-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8f2d5-130">None</span></span>

## <span data-ttu-id="8f2d5-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f2d5-131">OUTPUTS</span></span>

### <span data-ttu-id="8f2d5-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="8f2d5-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="8f2d5-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f2d5-133">NOTES</span></span>

## <span data-ttu-id="8f2d5-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f2d5-134">RELATED LINKS</span></span>
