---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256592"
---
# <span data-ttu-id="a3656-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="a3656-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="a3656-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3656-102">SYNOPSIS</span></span>
<span data-ttu-id="a3656-103">Obtém as propriedades de produtividade CosmosDB do banco de dados do MongoDB.</span><span class="sxs-lookup"><span data-stu-id="a3656-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="a3656-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3656-104">SYNTAX</span></span>

### <span data-ttu-id="a3656-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3656-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3656-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3656-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3656-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3656-107">DESCRIPTION</span></span>
<span data-ttu-id="a3656-108">O cmdlet **Get-AzCosmosDBMongoDBDatabaseThroughput** Obtém as propriedades de produtividade do banco de dados do MongoDB.</span><span class="sxs-lookup"><span data-stu-id="a3656-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="a3656-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3656-109">EXAMPLES</span></span>

### <span data-ttu-id="a3656-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3656-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="a3656-111">OS</span><span class="sxs-lookup"><span data-stu-id="a3656-111">PARAMETERS</span></span>

### <span data-ttu-id="a3656-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3656-112">-AccountName</span></span>
<span data-ttu-id="a3656-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="a3656-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a3656-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3656-114">-DefaultProfile</span></span>
<span data-ttu-id="a3656-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3656-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3656-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3656-116">-InputObject</span></span>
<span data-ttu-id="a3656-117">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a3656-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3656-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3656-118">-Name</span></span>
<span data-ttu-id="a3656-119">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a3656-119">Database name.</span></span>

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

### <span data-ttu-id="a3656-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3656-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3656-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3656-121">Name of resource group.</span></span>

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

### <span data-ttu-id="a3656-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3656-122">CommonParameters</span></span>
<span data-ttu-id="a3656-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3656-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3656-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3656-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3656-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3656-125">INPUTS</span></span>

### <span data-ttu-id="a3656-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a3656-126">None</span></span>

## <span data-ttu-id="a3656-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3656-127">OUTPUTS</span></span>

### <span data-ttu-id="a3656-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a3656-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a3656-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3656-129">NOTES</span></span>

## <span data-ttu-id="a3656-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3656-130">RELATED LINKS</span></span>
