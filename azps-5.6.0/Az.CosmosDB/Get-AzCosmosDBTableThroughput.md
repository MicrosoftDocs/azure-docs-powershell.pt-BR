---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7b48190a9ef01d468e762d93d7bc63a96e831de8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889790"
---
# <span data-ttu-id="d3373-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="d3373-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="d3373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3373-102">SYNOPSIS</span></span>
<span data-ttu-id="d3373-103">Obtém a produtividade de uma Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d3373-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="d3373-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3373-104">SYNTAX</span></span>

### <span data-ttu-id="d3373-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3373-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3373-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3373-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3373-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3373-107">DESCRIPTION</span></span>
<span data-ttu-id="d3373-108">O cmdlet **Get-AzCosmosDBTableThroughput** obtém a produtividade de uma Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d3373-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="d3373-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3373-109">EXAMPLES</span></span>

### <span data-ttu-id="d3373-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3373-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="d3373-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3373-111">PARAMETERS</span></span>

### <span data-ttu-id="d3373-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3373-112">-AccountName</span></span>
<span data-ttu-id="d3373-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="d3373-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d3373-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3373-114">-DefaultProfile</span></span>
<span data-ttu-id="d3373-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3373-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3373-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3373-116">-InputObject</span></span>
<span data-ttu-id="d3373-117">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d3373-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d3373-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d3373-118">-Name</span></span>
<span data-ttu-id="d3373-119">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="d3373-119">Name of the Table.</span></span>

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

### <span data-ttu-id="d3373-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3373-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3373-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3373-121">Name of resource group.</span></span>

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

### <span data-ttu-id="d3373-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3373-122">CommonParameters</span></span>
<span data-ttu-id="d3373-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3373-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3373-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3373-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3373-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3373-125">INPUTS</span></span>

### <span data-ttu-id="d3373-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d3373-126">None</span></span>

## <span data-ttu-id="d3373-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3373-127">OUTPUTS</span></span>

### <span data-ttu-id="d3373-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d3373-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d3373-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3373-129">NOTES</span></span>

## <span data-ttu-id="d3373-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3373-130">RELATED LINKS</span></span>
