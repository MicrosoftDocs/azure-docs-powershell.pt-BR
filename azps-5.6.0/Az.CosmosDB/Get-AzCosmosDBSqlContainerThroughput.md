---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 3ceb7ccbb789c21fc0fdb51244260e6a54b3e900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891503"
---
# <span data-ttu-id="ed447-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="ed447-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="ed447-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed447-102">SYNOPSIS</span></span>
<span data-ttu-id="ed447-103">Obtém as configurações de transferência correspondentes a um Contêiner Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ed447-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="ed447-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed447-104">SYNTAX</span></span>

### <span data-ttu-id="ed447-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed447-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed447-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed447-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed447-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed447-107">DESCRIPTION</span></span>
<span data-ttu-id="ed447-108">O cmdlet **Get-AzCosmosDBSqlContainerThroughput** obtém as configurações de transferência correspondentes a um Contêiner Sql do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ed447-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="ed447-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed447-109">EXAMPLES</span></span>

### <span data-ttu-id="ed447-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed447-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="ed447-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed447-111">PARAMETERS</span></span>

### <span data-ttu-id="ed447-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed447-112">-AccountName</span></span>
<span data-ttu-id="ed447-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="ed447-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ed447-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed447-114">-DatabaseName</span></span>
<span data-ttu-id="ed447-115">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ed447-115">Database name.</span></span>

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

### <span data-ttu-id="ed447-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed447-116">-DefaultProfile</span></span>
<span data-ttu-id="ed447-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed447-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed447-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed447-118">-InputObject</span></span>
<span data-ttu-id="ed447-119">Objeto Sql Container.</span><span class="sxs-lookup"><span data-stu-id="ed447-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed447-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ed447-120">-Name</span></span>
<span data-ttu-id="ed447-121">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="ed447-121">Container name.</span></span>

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

### <span data-ttu-id="ed447-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed447-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed447-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed447-123">Name of resource group.</span></span>

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

### <span data-ttu-id="ed447-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed447-124">CommonParameters</span></span>
<span data-ttu-id="ed447-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed447-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed447-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed447-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed447-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed447-127">INPUTS</span></span>

### <span data-ttu-id="ed447-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ed447-128">None</span></span>

## <span data-ttu-id="ed447-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed447-129">OUTPUTS</span></span>

### <span data-ttu-id="ed447-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ed447-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ed447-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed447-131">NOTES</span></span>

## <span data-ttu-id="ed447-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed447-132">RELATED LINKS</span></span>
