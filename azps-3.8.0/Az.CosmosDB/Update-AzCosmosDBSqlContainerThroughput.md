---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: e38e10765bc9a9768efaf1598a1865ec985b376c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942185"
---
# <span data-ttu-id="513db-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="513db-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="513db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="513db-102">SYNOPSIS</span></span>
<span data-ttu-id="513db-103">Atualiza o valor de produtividade de um contêiner SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="513db-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="513db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="513db-104">SYNTAX</span></span>

### <span data-ttu-id="513db-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="513db-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="513db-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="513db-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="513db-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="513db-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="513db-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="513db-108">EXAMPLES</span></span>

### <span data-ttu-id="513db-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="513db-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="513db-110">OS</span><span class="sxs-lookup"><span data-stu-id="513db-110">PARAMETERS</span></span>

### <span data-ttu-id="513db-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="513db-111">-AccountName</span></span>
<span data-ttu-id="513db-112">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="513db-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="513db-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="513db-113">-Confirm</span></span>
<span data-ttu-id="513db-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="513db-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513db-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="513db-115">-DatabaseName</span></span>
<span data-ttu-id="513db-116">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="513db-116">Database name.</span></span>

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

### <span data-ttu-id="513db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513db-117">-DefaultProfile</span></span>
<span data-ttu-id="513db-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="513db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="513db-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="513db-119">-InputObject</span></span>
<span data-ttu-id="513db-120">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="513db-120">Sql Database object.</span></span>

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

### <span data-ttu-id="513db-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="513db-121">-Name</span></span>
<span data-ttu-id="513db-122">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="513db-122">Container name.</span></span>

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

### <span data-ttu-id="513db-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="513db-123">-ParentObject</span></span>
<span data-ttu-id="513db-124">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="513db-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="513db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="513db-125">-ResourceGroupName</span></span>
<span data-ttu-id="513db-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="513db-126">Name of resource group.</span></span>

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

### <span data-ttu-id="513db-127">-Throughput</span><span class="sxs-lookup"><span data-stu-id="513db-127">-Throughput</span></span>
<span data-ttu-id="513db-128">O throughput do contêiner SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="513db-128">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="513db-129">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="513db-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513db-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="513db-130">-WhatIf</span></span>
<span data-ttu-id="513db-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="513db-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513db-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="513db-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513db-133">CommonParameters</span></span>
<span data-ttu-id="513db-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513db-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="513db-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513db-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="513db-136">INPUTS</span></span>

### <span data-ttu-id="513db-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="513db-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="513db-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="513db-138">OUTPUTS</span></span>

### <span data-ttu-id="513db-139">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="513db-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="513db-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="513db-140">NOTES</span></span>

## <span data-ttu-id="513db-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="513db-141">RELATED LINKS</span></span>
