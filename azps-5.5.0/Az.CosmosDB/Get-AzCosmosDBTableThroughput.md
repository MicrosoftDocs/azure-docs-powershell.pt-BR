---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112053"
---
# <span data-ttu-id="5bed4-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="5bed4-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="5bed4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bed4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bed4-103">Obtém a produtividade de uma Tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5bed4-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="5bed4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bed4-104">SYNTAX</span></span>

### <span data-ttu-id="5bed4-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5bed4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bed4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bed4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bed4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bed4-107">DESCRIPTION</span></span>
<span data-ttu-id="5bed4-108">O **cmdlet Get-AzCosmosDBTableThroughput** obtém a produtividade de uma Tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5bed4-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="5bed4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bed4-109">EXAMPLES</span></span>

### <span data-ttu-id="5bed4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5bed4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="5bed4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bed4-111">PARAMETERS</span></span>

### <span data-ttu-id="5bed4-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="5bed4-112">-AccountName</span></span>
<span data-ttu-id="5bed4-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="5bed4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5bed4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bed4-114">-DefaultProfile</span></span>
<span data-ttu-id="5bed4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bed4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bed4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bed4-116">-InputObject</span></span>
<span data-ttu-id="5bed4-117">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="5bed4-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5bed4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bed4-118">-Name</span></span>
<span data-ttu-id="5bed4-119">Nome da Tabela.</span><span class="sxs-lookup"><span data-stu-id="5bed4-119">Name of the Table.</span></span>

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

### <span data-ttu-id="5bed4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bed4-120">-ResourceGroupName</span></span>
<span data-ttu-id="5bed4-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5bed4-121">Name of resource group.</span></span>

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

### <span data-ttu-id="5bed4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bed4-122">CommonParameters</span></span>
<span data-ttu-id="5bed4-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bed4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bed4-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bed4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bed4-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="5bed4-125">INPUTS</span></span>

### <span data-ttu-id="5bed4-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5bed4-126">None</span></span>

## <span data-ttu-id="5bed4-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="5bed4-127">OUTPUTS</span></span>

### <span data-ttu-id="5bed4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5bed4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5bed4-129">Notas</span><span class="sxs-lookup"><span data-stu-id="5bed4-129">NOTES</span></span>

## <span data-ttu-id="5bed4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bed4-130">RELATED LINKS</span></span>
