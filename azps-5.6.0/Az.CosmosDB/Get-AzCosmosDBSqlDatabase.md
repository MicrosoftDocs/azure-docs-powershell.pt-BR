---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 6d0fe9565a969de19234d65378fd91a1af7a327f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901497"
---
# <span data-ttu-id="0f703-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0f703-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="0f703-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f703-102">SYNOPSIS</span></span>
<span data-ttu-id="0f703-103">Obtém o Banco de Dados Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0f703-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="0f703-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0f703-104">SYNTAX</span></span>

### <span data-ttu-id="0f703-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0f703-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f703-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f703-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f703-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0f703-107">DESCRIPTION</span></span>
<span data-ttu-id="0f703-108">O cmdlet **Get-AzCosmosDBSqlDatabase** obtém a lista de todos os bancos de dados sql do CosmosDB existentes para um determinado ResourceGroupName, AccountName e obtém um único Banco de Dados Sql do CosmosDB para um determinado ResourceGroupName, AccountName, DatabaseName e ContainerName.</span><span class="sxs-lookup"><span data-stu-id="0f703-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="0f703-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f703-109">EXAMPLES</span></span>

### <span data-ttu-id="0f703-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f703-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="0f703-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0f703-111">PARAMETERS</span></span>

### <span data-ttu-id="0f703-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0f703-112">-AccountName</span></span>
<span data-ttu-id="0f703-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="0f703-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0f703-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f703-114">-DefaultProfile</span></span>
<span data-ttu-id="0f703-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f703-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f703-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0f703-116">-Name</span></span>
<span data-ttu-id="0f703-117">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f703-117">Database name.</span></span>

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

### <span data-ttu-id="0f703-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0f703-118">-ParentObject</span></span>
<span data-ttu-id="0f703-119">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0f703-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0f703-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f703-120">-ResourceGroupName</span></span>
<span data-ttu-id="0f703-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f703-121">Name of resource group.</span></span>

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

### <span data-ttu-id="0f703-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f703-122">CommonParameters</span></span>
<span data-ttu-id="0f703-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f703-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f703-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f703-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f703-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f703-125">INPUTS</span></span>

### <span data-ttu-id="0f703-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0f703-126">None</span></span>

## <span data-ttu-id="0f703-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0f703-127">OUTPUTS</span></span>

### <span data-ttu-id="0f703-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0f703-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="0f703-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0f703-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0f703-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="0f703-130">NOTES</span></span>

## <span data-ttu-id="0f703-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f703-131">RELATED LINKS</span></span>
