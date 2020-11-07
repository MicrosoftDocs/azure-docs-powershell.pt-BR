---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: a9a81336ab921ebd63b8a969be5fbf65f4b7fa14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940561"
---
# <span data-ttu-id="97662-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="97662-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="97662-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97662-102">SYNOPSIS</span></span>
<span data-ttu-id="97662-103">Obtém o StoredProcedure do SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="97662-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="97662-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97662-104">SYNTAX</span></span>

### <span data-ttu-id="97662-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97662-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97662-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97662-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97662-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97662-107">DESCRIPTION</span></span>
<span data-ttu-id="97662-108">O cmdlet **Get-AzCosmosDBSqlStoredProcedure** Obtém a lista de todos os StoredProcedures SQL existentes do SQL para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e Obtém um único StoredProcedure do SQL de CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e storedprocedurename.</span><span class="sxs-lookup"><span data-stu-id="97662-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="97662-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97662-109">EXAMPLES</span></span>

### <span data-ttu-id="97662-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97662-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="97662-111">OS</span><span class="sxs-lookup"><span data-stu-id="97662-111">PARAMETERS</span></span>

### <span data-ttu-id="97662-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97662-112">-AccountName</span></span>
<span data-ttu-id="97662-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="97662-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="97662-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="97662-114">-ContainerName</span></span>
<span data-ttu-id="97662-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="97662-115">Container name.</span></span>

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

### <span data-ttu-id="97662-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97662-116">-DatabaseName</span></span>
<span data-ttu-id="97662-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="97662-117">Database name.</span></span>

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

### <span data-ttu-id="97662-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97662-118">-DefaultProfile</span></span>
<span data-ttu-id="97662-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97662-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97662-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97662-120">-InputObject</span></span>
<span data-ttu-id="97662-121">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="97662-121">Sql Container object.</span></span>

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

### <span data-ttu-id="97662-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="97662-122">-Name</span></span>
<span data-ttu-id="97662-123">Nome Prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="97662-123">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="97662-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97662-124">-ResourceGroupName</span></span>
<span data-ttu-id="97662-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97662-125">Name of resource group.</span></span>

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

### <span data-ttu-id="97662-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97662-126">CommonParameters</span></span>
<span data-ttu-id="97662-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97662-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97662-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97662-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97662-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97662-129">INPUTS</span></span>

### <span data-ttu-id="97662-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="97662-130">None</span></span>

## <span data-ttu-id="97662-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97662-131">OUTPUTS</span></span>

### <span data-ttu-id="97662-132">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="97662-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="97662-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97662-133">NOTES</span></span>

## <span data-ttu-id="97662-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97662-134">RELATED LINKS</span></span>
