---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: b4afffee9f5eced29968b136ec1dc9a07250ab8d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942181"
---
# <span data-ttu-id="b6d05-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="b6d05-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="b6d05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6d05-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d05-103">Atualiza o valor de produtividade de um banco de dados SQL do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b6d05-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="b6d05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6d05-104">SYNTAX</span></span>

### <span data-ttu-id="b6d05-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6d05-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6d05-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6d05-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -Throughput <Int32> -ParentObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6d05-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6d05-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6d05-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6d05-108">EXAMPLES</span></span>

### <span data-ttu-id="b6d05-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6d05-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="b6d05-110">OS</span><span class="sxs-lookup"><span data-stu-id="b6d05-110">PARAMETERS</span></span>

### <span data-ttu-id="b6d05-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6d05-111">-AccountName</span></span>
<span data-ttu-id="b6d05-112">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="b6d05-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b6d05-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6d05-113">-Confirm</span></span>
<span data-ttu-id="b6d05-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6d05-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6d05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d05-115">-DefaultProfile</span></span>
<span data-ttu-id="b6d05-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6d05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6d05-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6d05-117">-InputObject</span></span>
<span data-ttu-id="b6d05-118">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b6d05-118">CosmosDB Account object</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6d05-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6d05-119">-Name</span></span>
<span data-ttu-id="b6d05-120">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b6d05-120">Database name.</span></span>

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

### <span data-ttu-id="b6d05-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b6d05-121">-ParentObject</span></span>
<span data-ttu-id="b6d05-122">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b6d05-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6d05-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d05-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6d05-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6d05-124">Name of resource group.</span></span>

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

### <span data-ttu-id="b6d05-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="b6d05-125">-Throughput</span></span>
<span data-ttu-id="b6d05-126">O throughput do banco de dados SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b6d05-126">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="b6d05-127">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="b6d05-127">Default value is 400.</span></span>

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

### <span data-ttu-id="b6d05-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6d05-128">-WhatIf</span></span>
<span data-ttu-id="b6d05-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6d05-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6d05-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6d05-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6d05-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d05-131">CommonParameters</span></span>
<span data-ttu-id="b6d05-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6d05-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d05-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6d05-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d05-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6d05-134">INPUTS</span></span>

### <span data-ttu-id="b6d05-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b6d05-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b6d05-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6d05-136">OUTPUTS</span></span>

### <span data-ttu-id="b6d05-137">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b6d05-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b6d05-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6d05-138">NOTES</span></span>

## <span data-ttu-id="b6d05-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6d05-139">RELATED LINKS</span></span>
