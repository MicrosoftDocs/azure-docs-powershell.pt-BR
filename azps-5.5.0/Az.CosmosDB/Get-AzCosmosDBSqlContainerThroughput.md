---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116471"
---
# <span data-ttu-id="75eb8-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="75eb8-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="75eb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="75eb8-103">Obtém as configurações de produtividade correspondentes a um Contêiner Sql do Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="75eb8-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="75eb8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75eb8-104">SYNTAX</span></span>

### <span data-ttu-id="75eb8-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75eb8-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75eb8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75eb8-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75eb8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="75eb8-107">DESCRIPTION</span></span>
<span data-ttu-id="75eb8-108">O cmdlet **Get-AzCosmosDBSqlContainerThroughput** obtém as configurações de produtividade correspondentes a um Contêiner Sql Do Sql Do Sql.</span><span class="sxs-lookup"><span data-stu-id="75eb8-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="75eb8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75eb8-109">EXAMPLES</span></span>

### <span data-ttu-id="75eb8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75eb8-110">Example 1</span></span>
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

## <span data-ttu-id="75eb8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75eb8-111">PARAMETERS</span></span>

### <span data-ttu-id="75eb8-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="75eb8-112">-AccountName</span></span>
<span data-ttu-id="75eb8-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="75eb8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="75eb8-114">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="75eb8-114">-DatabaseName</span></span>
<span data-ttu-id="75eb8-115">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="75eb8-115">Database name.</span></span>

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

### <span data-ttu-id="75eb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75eb8-116">-DefaultProfile</span></span>
<span data-ttu-id="75eb8-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75eb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75eb8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75eb8-118">-InputObject</span></span>
<span data-ttu-id="75eb8-119">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="75eb8-119">Sql Container object.</span></span>

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

### <span data-ttu-id="75eb8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="75eb8-120">-Name</span></span>
<span data-ttu-id="75eb8-121">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="75eb8-121">Container name.</span></span>

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

### <span data-ttu-id="75eb8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75eb8-122">-ResourceGroupName</span></span>
<span data-ttu-id="75eb8-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75eb8-123">Name of resource group.</span></span>

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

### <span data-ttu-id="75eb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75eb8-124">CommonParameters</span></span>
<span data-ttu-id="75eb8-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75eb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75eb8-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75eb8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75eb8-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="75eb8-127">INPUTS</span></span>

### <span data-ttu-id="75eb8-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75eb8-128">None</span></span>

## <span data-ttu-id="75eb8-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="75eb8-129">OUTPUTS</span></span>

### <span data-ttu-id="75eb8-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="75eb8-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="75eb8-131">Notas</span><span class="sxs-lookup"><span data-stu-id="75eb8-131">NOTES</span></span>

## <span data-ttu-id="75eb8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75eb8-132">RELATED LINKS</span></span>
