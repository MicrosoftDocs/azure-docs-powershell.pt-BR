---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111045"
---
# <span data-ttu-id="46ebc-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="46ebc-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="46ebc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="46ebc-103">Obtém o Sql StoredProcedure do Sql.</span><span class="sxs-lookup"><span data-stu-id="46ebc-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="46ebc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46ebc-104">SYNTAX</span></span>

### <span data-ttu-id="46ebc-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="46ebc-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46ebc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46ebc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ebc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="46ebc-107">DESCRIPTION</span></span>
<span data-ttu-id="46ebc-108">O cmdlet **Get-AzCosmosDBSqlStoredProcedure** obtém a lista de todos os existentes do Sql Sql StoredProcedures para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName e obtém um único Sql Sql StoredProcedure para um determinado ResourceGroupName, AccountName, DatabaseName, ContainerName e StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="46ebc-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="46ebc-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46ebc-109">EXAMPLES</span></span>

### <span data-ttu-id="46ebc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46ebc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="46ebc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46ebc-111">PARAMETERS</span></span>

### <span data-ttu-id="46ebc-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="46ebc-112">-AccountName</span></span>
<span data-ttu-id="46ebc-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="46ebc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46ebc-114">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="46ebc-114">-ContainerName</span></span>
<span data-ttu-id="46ebc-115">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="46ebc-115">Container name.</span></span>

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

### <span data-ttu-id="46ebc-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="46ebc-116">-DatabaseName</span></span>
<span data-ttu-id="46ebc-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="46ebc-117">Database name.</span></span>

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

### <span data-ttu-id="46ebc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ebc-118">-DefaultProfile</span></span>
<span data-ttu-id="46ebc-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46ebc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ebc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="46ebc-120">-Name</span></span>
<span data-ttu-id="46ebc-121">Nome prcodecure armazenado.</span><span class="sxs-lookup"><span data-stu-id="46ebc-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="46ebc-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="46ebc-122">-ParentObject</span></span>
<span data-ttu-id="46ebc-123">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="46ebc-123">Sql Container object.</span></span>

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

### <span data-ttu-id="46ebc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ebc-124">-ResourceGroupName</span></span>
<span data-ttu-id="46ebc-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46ebc-125">Name of resource group.</span></span>

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

### <span data-ttu-id="46ebc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ebc-126">CommonParameters</span></span>
<span data-ttu-id="46ebc-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ebc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ebc-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46ebc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ebc-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="46ebc-129">INPUTS</span></span>

### <span data-ttu-id="46ebc-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="46ebc-130">None</span></span>

## <span data-ttu-id="46ebc-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="46ebc-131">OUTPUTS</span></span>

### <span data-ttu-id="46ebc-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedGetResults</span><span class="sxs-lookup"><span data-stu-id="46ebc-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="46ebc-133">Notas</span><span class="sxs-lookup"><span data-stu-id="46ebc-133">NOTES</span></span>

## <span data-ttu-id="46ebc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46ebc-134">RELATED LINKS</span></span>
