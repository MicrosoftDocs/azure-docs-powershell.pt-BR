---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: dbffec52b5c1b30f6b00febbc2e6c952beda669e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888547"
---
# <span data-ttu-id="5107f-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="5107f-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="5107f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5107f-102">SYNOPSIS</span></span>
<span data-ttu-id="5107f-103">Atualiza o banco de dados MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5107f-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="5107f-104">Executa uma operação de patch do lado do cliente lendo o Banco de Dados existente.</span><span class="sxs-lookup"><span data-stu-id="5107f-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="5107f-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5107f-105">SYNTAX</span></span>

### <span data-ttu-id="5107f-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5107f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5107f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5107f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5107f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5107f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5107f-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5107f-109">DESCRIPTION</span></span>
<span data-ttu-id="5107f-110">Atualiza o banco de dados MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5107f-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="5107f-111">Executa uma operação de patch do lado do cliente lendo o Banco de Dados existente.</span><span class="sxs-lookup"><span data-stu-id="5107f-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="5107f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5107f-112">EXAMPLES</span></span>

### <span data-ttu-id="5107f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5107f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="5107f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5107f-114">PARAMETERS</span></span>

### <span data-ttu-id="5107f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5107f-115">-AccountName</span></span>
<span data-ttu-id="5107f-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="5107f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5107f-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5107f-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5107f-118">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="5107f-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5107f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5107f-119">-Confirm</span></span>
<span data-ttu-id="5107f-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5107f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5107f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5107f-121">-DefaultProfile</span></span>
<span data-ttu-id="5107f-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5107f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5107f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5107f-123">-InputObject</span></span>
<span data-ttu-id="5107f-124">Objeto Mongo Database.</span><span class="sxs-lookup"><span data-stu-id="5107f-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5107f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5107f-125">-Name</span></span>
<span data-ttu-id="5107f-126">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5107f-126">Database name.</span></span>

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

### <span data-ttu-id="5107f-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5107f-127">-ParentObject</span></span>
<span data-ttu-id="5107f-128">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5107f-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5107f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5107f-129">-ResourceGroupName</span></span>
<span data-ttu-id="5107f-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5107f-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5107f-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="5107f-131">-Throughput</span></span>
<span data-ttu-id="5107f-132">A produtividade do banco de dados Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5107f-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="5107f-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="5107f-133">Default value is 400.</span></span>

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

### <span data-ttu-id="5107f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5107f-134">-WhatIf</span></span>
<span data-ttu-id="5107f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5107f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5107f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5107f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5107f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5107f-137">CommonParameters</span></span>
<span data-ttu-id="5107f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5107f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5107f-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5107f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5107f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5107f-140">INPUTS</span></span>

### <span data-ttu-id="5107f-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5107f-141">None</span></span>

## <span data-ttu-id="5107f-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5107f-142">OUTPUTS</span></span>

### <span data-ttu-id="5107f-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5107f-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="5107f-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="5107f-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="5107f-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="5107f-145">NOTES</span></span>

## <span data-ttu-id="5107f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5107f-146">RELATED LINKS</span></span>
