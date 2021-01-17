---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430081"
---
# <span data-ttu-id="c298e-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="c298e-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="c298e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c298e-102">SYNOPSIS</span></span>
<span data-ttu-id="c298e-103">Obtém as configurações de taxa de transferência correspondentes a um contêiner SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c298e-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c298e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c298e-104">SYNTAX</span></span>

### <span data-ttu-id="c298e-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c298e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c298e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c298e-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c298e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c298e-107">DESCRIPTION</span></span>
<span data-ttu-id="c298e-108">O cmdlet **Get-AzCosmosDBSqlContainerThroughput** Obtém as configurações de produtividade correspondentes a um contêiner SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c298e-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="c298e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c298e-109">EXAMPLES</span></span>

### <span data-ttu-id="c298e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c298e-110">Example 1</span></span>
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

## <span data-ttu-id="c298e-111">OS</span><span class="sxs-lookup"><span data-stu-id="c298e-111">PARAMETERS</span></span>

### <span data-ttu-id="c298e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c298e-112">-AccountName</span></span>
<span data-ttu-id="c298e-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="c298e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c298e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c298e-114">-DatabaseName</span></span>
<span data-ttu-id="c298e-115">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c298e-115">Database name.</span></span>

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

### <span data-ttu-id="c298e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c298e-116">-DefaultProfile</span></span>
<span data-ttu-id="c298e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c298e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c298e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c298e-118">-InputObject</span></span>
<span data-ttu-id="c298e-119">Objeto contêiner SQL.</span><span class="sxs-lookup"><span data-stu-id="c298e-119">Sql Container object.</span></span>

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

### <span data-ttu-id="c298e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c298e-120">-Name</span></span>
<span data-ttu-id="c298e-121">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c298e-121">Container name.</span></span>

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

### <span data-ttu-id="c298e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c298e-122">-ResourceGroupName</span></span>
<span data-ttu-id="c298e-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c298e-123">Name of resource group.</span></span>

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

### <span data-ttu-id="c298e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c298e-124">CommonParameters</span></span>
<span data-ttu-id="c298e-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c298e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c298e-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c298e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c298e-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c298e-127">INPUTS</span></span>

### <span data-ttu-id="c298e-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c298e-128">None</span></span>

## <span data-ttu-id="c298e-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c298e-129">OUTPUTS</span></span>

### <span data-ttu-id="c298e-130">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c298e-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c298e-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c298e-131">NOTES</span></span>

## <span data-ttu-id="c298e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c298e-132">RELATED LINKS</span></span>
