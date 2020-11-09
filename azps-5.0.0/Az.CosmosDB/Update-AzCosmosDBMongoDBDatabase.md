---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281225"
---
# <span data-ttu-id="8248a-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="8248a-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="8248a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8248a-102">SYNOPSIS</span></span>
<span data-ttu-id="8248a-103">Atualiza o banco de dados do CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="8248a-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="8248a-104">Executa uma operação de patch do lado do cliente lendo o banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="8248a-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="8248a-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8248a-105">SYNTAX</span></span>

### <span data-ttu-id="8248a-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8248a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8248a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8248a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8248a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8248a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8248a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8248a-109">DESCRIPTION</span></span>
<span data-ttu-id="8248a-110">Atualiza o banco de dados do CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="8248a-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="8248a-111">Executa uma operação de patch do lado do cliente lendo o banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="8248a-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="8248a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8248a-112">EXAMPLES</span></span>

### <span data-ttu-id="8248a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8248a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="8248a-114">OS</span><span class="sxs-lookup"><span data-stu-id="8248a-114">PARAMETERS</span></span>

### <span data-ttu-id="8248a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8248a-115">-AccountName</span></span>
<span data-ttu-id="8248a-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="8248a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8248a-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8248a-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8248a-118">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="8248a-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8248a-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8248a-119">-Confirm</span></span>
<span data-ttu-id="8248a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8248a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8248a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8248a-121">-DefaultProfile</span></span>
<span data-ttu-id="8248a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8248a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8248a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8248a-123">-InputObject</span></span>
<span data-ttu-id="8248a-124">Objeto de banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="8248a-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="8248a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8248a-125">-Name</span></span>
<span data-ttu-id="8248a-126">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8248a-126">Database name.</span></span>

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

### <span data-ttu-id="8248a-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8248a-127">-ParentObject</span></span>
<span data-ttu-id="8248a-128">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8248a-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8248a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8248a-129">-ResourceGroupName</span></span>
<span data-ttu-id="8248a-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8248a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="8248a-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="8248a-131">-Throughput</span></span>
<span data-ttu-id="8248a-132">A produtividade do banco de dados do Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8248a-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="8248a-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="8248a-133">Default value is 400.</span></span>

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

### <span data-ttu-id="8248a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8248a-134">-WhatIf</span></span>
<span data-ttu-id="8248a-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8248a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8248a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8248a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8248a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8248a-137">CommonParameters</span></span>
<span data-ttu-id="8248a-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8248a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8248a-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8248a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8248a-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8248a-140">INPUTS</span></span>

### <span data-ttu-id="8248a-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8248a-141">None</span></span>

## <span data-ttu-id="8248a-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8248a-142">OUTPUTS</span></span>

### <span data-ttu-id="8248a-143">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8248a-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="8248a-144">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8248a-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="8248a-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8248a-145">NOTES</span></span>

## <span data-ttu-id="8248a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8248a-146">RELATED LINKS</span></span>
