---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434088"
---
# <span data-ttu-id="1bf57-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="1bf57-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="1bf57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bf57-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf57-103">Obtém a taxa de transferência de uma tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1bf57-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="1bf57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bf57-104">SYNTAX</span></span>

### <span data-ttu-id="1bf57-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1bf57-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bf57-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bf57-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf57-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bf57-107">DESCRIPTION</span></span>
<span data-ttu-id="1bf57-108">O cmdlet **Get-AzCosmosDBTableThroughput** Obtém a taxa de transferência de uma tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1bf57-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="1bf57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bf57-109">EXAMPLES</span></span>

### <span data-ttu-id="1bf57-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1bf57-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="1bf57-111">OS</span><span class="sxs-lookup"><span data-stu-id="1bf57-111">PARAMETERS</span></span>

### <span data-ttu-id="1bf57-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1bf57-112">-AccountName</span></span>
<span data-ttu-id="1bf57-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="1bf57-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1bf57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf57-114">-DefaultProfile</span></span>
<span data-ttu-id="1bf57-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf57-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf57-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bf57-116">-InputObject</span></span>
<span data-ttu-id="1bf57-117">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1bf57-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1bf57-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bf57-118">-Name</span></span>
<span data-ttu-id="1bf57-119">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="1bf57-119">Name of the Table.</span></span>

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

### <span data-ttu-id="1bf57-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf57-120">-ResourceGroupName</span></span>
<span data-ttu-id="1bf57-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1bf57-121">Name of resource group.</span></span>

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

### <span data-ttu-id="1bf57-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf57-122">CommonParameters</span></span>
<span data-ttu-id="1bf57-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf57-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf57-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bf57-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf57-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bf57-125">INPUTS</span></span>

### <span data-ttu-id="1bf57-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1bf57-126">None</span></span>

## <span data-ttu-id="1bf57-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bf57-127">OUTPUTS</span></span>

### <span data-ttu-id="1bf57-128">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1bf57-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1bf57-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bf57-129">NOTES</span></span>

## <span data-ttu-id="1bf57-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bf57-130">RELATED LINKS</span></span>
