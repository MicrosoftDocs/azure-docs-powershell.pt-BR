---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264466"
---
# <span data-ttu-id="118d3-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="118d3-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="118d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="118d3-102">SYNOPSIS</span></span>
<span data-ttu-id="118d3-103">Atualiza o valor de produtividade de uma tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="118d3-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="118d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="118d3-104">SYNTAX</span></span>

### <span data-ttu-id="118d3-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="118d3-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="118d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="118d3-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="118d3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="118d3-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="118d3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="118d3-108">DESCRIPTION</span></span>
<span data-ttu-id="118d3-109">Atualiza o valor de produtividade de uma tabela CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="118d3-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="118d3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="118d3-110">EXAMPLES</span></span>

### <span data-ttu-id="118d3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="118d3-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="118d3-112">OS</span><span class="sxs-lookup"><span data-stu-id="118d3-112">PARAMETERS</span></span>

### <span data-ttu-id="118d3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="118d3-113">-AccountName</span></span>
<span data-ttu-id="118d3-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="118d3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="118d3-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="118d3-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="118d3-116">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="118d3-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118d3-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="118d3-117">-Confirm</span></span>
<span data-ttu-id="118d3-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="118d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="118d3-119">-DefaultProfile</span></span>
<span data-ttu-id="118d3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="118d3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="118d3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="118d3-121">-InputObject</span></span>
<span data-ttu-id="118d3-122">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="118d3-122">CosmosDB Account object</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="118d3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="118d3-123">-Name</span></span>
<span data-ttu-id="118d3-124">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="118d3-124">Name of the Table.</span></span>

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

### <span data-ttu-id="118d3-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="118d3-125">-ParentObject</span></span>
<span data-ttu-id="118d3-126">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="118d3-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="118d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="118d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="118d3-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="118d3-128">Name of resource group.</span></span>

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

### <span data-ttu-id="118d3-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="118d3-129">-Throughput</span></span>
<span data-ttu-id="118d3-130">A taxa de transferência da tabela (RU/s).</span><span class="sxs-lookup"><span data-stu-id="118d3-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="118d3-131">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="118d3-131">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118d3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="118d3-132">-WhatIf</span></span>
<span data-ttu-id="118d3-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="118d3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="118d3-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="118d3-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="118d3-135">CommonParameters</span></span>
<span data-ttu-id="118d3-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="118d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="118d3-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="118d3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="118d3-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="118d3-138">INPUTS</span></span>

### <span data-ttu-id="118d3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="118d3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="118d3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="118d3-140">OUTPUTS</span></span>

### <span data-ttu-id="118d3-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="118d3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="118d3-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="118d3-142">NOTES</span></span>

## <span data-ttu-id="118d3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="118d3-143">RELATED LINKS</span></span>
