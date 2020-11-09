---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1948bc5b5488c951861509c9b3c9ee7815eddec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281224"
---
# <span data-ttu-id="84e40-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="84e40-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="84e40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84e40-102">SYNOPSIS</span></span>
<span data-ttu-id="84e40-103">Atualiza o valor de produtividade de um banco de dados CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="84e40-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="84e40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84e40-104">SYNTAX</span></span>

### <span data-ttu-id="84e40-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="84e40-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e40-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e40-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84e40-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e40-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e40-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84e40-108">DESCRIPTION</span></span>
<span data-ttu-id="84e40-109">Atualiza o valor de produtividade de um banco de dados CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="84e40-109">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="84e40-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84e40-110">EXAMPLES</span></span>

### <span data-ttu-id="84e40-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84e40-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="84e40-112">OS</span><span class="sxs-lookup"><span data-stu-id="84e40-112">PARAMETERS</span></span>

### <span data-ttu-id="84e40-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="84e40-113">-AccountName</span></span>
<span data-ttu-id="84e40-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="84e40-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="84e40-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="84e40-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="84e40-116">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="84e40-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="84e40-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="84e40-117">-Confirm</span></span>
<span data-ttu-id="84e40-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84e40-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84e40-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e40-119">-DefaultProfile</span></span>
<span data-ttu-id="84e40-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84e40-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84e40-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84e40-121">-InputObject</span></span>
<span data-ttu-id="84e40-122">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="84e40-122">CosmosDB Account object</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84e40-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="84e40-123">-Name</span></span>
<span data-ttu-id="84e40-124">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="84e40-124">Database name.</span></span>

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

### <span data-ttu-id="84e40-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="84e40-125">-ParentObject</span></span>
<span data-ttu-id="84e40-126">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="84e40-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="84e40-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e40-127">-ResourceGroupName</span></span>
<span data-ttu-id="84e40-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84e40-128">Name of resource group.</span></span>

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

### <span data-ttu-id="84e40-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="84e40-129">-Throughput</span></span>
<span data-ttu-id="84e40-130">A produtividade do banco de dados do Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="84e40-130">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="84e40-131">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="84e40-131">Default value is 400.</span></span>

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

### <span data-ttu-id="84e40-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e40-132">-WhatIf</span></span>
<span data-ttu-id="84e40-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="84e40-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84e40-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84e40-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84e40-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e40-135">CommonParameters</span></span>
<span data-ttu-id="84e40-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e40-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e40-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84e40-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e40-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84e40-138">INPUTS</span></span>

### <span data-ttu-id="84e40-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="84e40-139">None</span></span>

## <span data-ttu-id="84e40-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84e40-140">OUTPUTS</span></span>

### <span data-ttu-id="84e40-141">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="84e40-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="84e40-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84e40-142">NOTES</span></span>

## <span data-ttu-id="84e40-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84e40-143">RELATED LINKS</span></span>
