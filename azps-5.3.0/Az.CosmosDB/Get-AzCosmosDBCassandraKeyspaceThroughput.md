---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430094"
---
# <span data-ttu-id="acf4d-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="acf4d-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="acf4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acf4d-102">SYNOPSIS</span></span>
<span data-ttu-id="acf4d-103">Obtém o valor de produtividade do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="acf4d-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="acf4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acf4d-104">SYNTAX</span></span>

### <span data-ttu-id="acf4d-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="acf4d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acf4d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf4d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf4d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acf4d-107">DESCRIPTION</span></span>
<span data-ttu-id="acf4d-108">O cmdlet **Get-AzCosmosDBCassandraKeyspaceThroughput** Obtém o objeto de taxa de transferência correspondente a um espaço de espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="acf4d-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="acf4d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acf4d-109">EXAMPLES</span></span>

### <span data-ttu-id="acf4d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="acf4d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="acf4d-111">OS</span><span class="sxs-lookup"><span data-stu-id="acf4d-111">PARAMETERS</span></span>

### <span data-ttu-id="acf4d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="acf4d-112">-AccountName</span></span>
<span data-ttu-id="acf4d-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="acf4d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="acf4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf4d-114">-DefaultProfile</span></span>
<span data-ttu-id="acf4d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acf4d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf4d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acf4d-116">-InputObject</span></span>
<span data-ttu-id="acf4d-117">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="acf4d-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="acf4d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="acf4d-118">-Name</span></span>
<span data-ttu-id="acf4d-119">Nome do espaço de Cassandra.</span><span class="sxs-lookup"><span data-stu-id="acf4d-119">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf4d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf4d-120">-ResourceGroupName</span></span>
<span data-ttu-id="acf4d-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="acf4d-121">Name of resource group.</span></span>

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

### <span data-ttu-id="acf4d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf4d-122">CommonParameters</span></span>
<span data-ttu-id="acf4d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf4d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf4d-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acf4d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf4d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acf4d-125">INPUTS</span></span>

### <span data-ttu-id="acf4d-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="acf4d-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="acf4d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acf4d-127">OUTPUTS</span></span>

### <span data-ttu-id="acf4d-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="acf4d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="acf4d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acf4d-129">NOTES</span></span>

## <span data-ttu-id="acf4d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acf4d-130">RELATED LINKS</span></span>
