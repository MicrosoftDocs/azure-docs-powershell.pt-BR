---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116483"
---
# <span data-ttu-id="b6228-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="b6228-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="b6228-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6228-102">SYNOPSIS</span></span>
<span data-ttu-id="b6228-103">Obtém o valor de produtividade do Espaço de Keyspace de Guida.</span><span class="sxs-lookup"><span data-stu-id="b6228-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="b6228-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6228-104">SYNTAX</span></span>

### <span data-ttu-id="b6228-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b6228-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6228-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6228-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6228-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6228-107">DESCRIPTION</span></span>
<span data-ttu-id="b6228-108">O cmdlet **Get-AzCosmosDBCasskeyspaceThroughput** obtém o objeto de produtividade correspondente a um determinado Espaço de Tecla.</span><span class="sxs-lookup"><span data-stu-id="b6228-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="b6228-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6228-109">EXAMPLES</span></span>

### <span data-ttu-id="b6228-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6228-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="b6228-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6228-111">PARAMETERS</span></span>

### <span data-ttu-id="b6228-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="b6228-112">-AccountName</span></span>
<span data-ttu-id="b6228-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="b6228-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b6228-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6228-114">-DefaultProfile</span></span>
<span data-ttu-id="b6228-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6228-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6228-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6228-116">-InputObject</span></span>
<span data-ttu-id="b6228-117">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="b6228-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b6228-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6228-118">-Name</span></span>
<span data-ttu-id="b6228-119">Nome do Espaço de Teclas Descaroçador.</span><span class="sxs-lookup"><span data-stu-id="b6228-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="b6228-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6228-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6228-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6228-121">Name of resource group.</span></span>

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

### <span data-ttu-id="b6228-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6228-122">CommonParameters</span></span>
<span data-ttu-id="b6228-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6228-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6228-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6228-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6228-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="b6228-125">INPUTS</span></span>

### <span data-ttu-id="b6228-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b6228-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b6228-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="b6228-127">OUTPUTS</span></span>

### <span data-ttu-id="b6228-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b6228-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b6228-129">Notas</span><span class="sxs-lookup"><span data-stu-id="b6228-129">NOTES</span></span>

## <span data-ttu-id="b6228-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6228-130">RELATED LINKS</span></span>
