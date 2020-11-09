---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281311"
---
# <span data-ttu-id="e164d-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="e164d-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="e164d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e164d-102">SYNOPSIS</span></span>
<span data-ttu-id="e164d-103">Cria um novo banco de dados CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="e164d-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="e164d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e164d-104">SYNTAX</span></span>

### <span data-ttu-id="e164d-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e164d-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e164d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e164d-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e164d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e164d-107">DESCRIPTION</span></span>
<span data-ttu-id="e164d-108">Cria um novo banco de dados CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="e164d-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="e164d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e164d-109">EXAMPLES</span></span>

### <span data-ttu-id="e164d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e164d-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="e164d-111">OS</span><span class="sxs-lookup"><span data-stu-id="e164d-111">PARAMETERS</span></span>

### <span data-ttu-id="e164d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e164d-112">-AccountName</span></span>
<span data-ttu-id="e164d-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="e164d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e164d-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e164d-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e164d-115">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="e164d-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e164d-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e164d-116">-Confirm</span></span>
<span data-ttu-id="e164d-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e164d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e164d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e164d-118">-DefaultProfile</span></span>
<span data-ttu-id="e164d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e164d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e164d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e164d-120">-Name</span></span>
<span data-ttu-id="e164d-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e164d-121">Database name.</span></span>

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

### <span data-ttu-id="e164d-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e164d-122">-ParentObject</span></span>
<span data-ttu-id="e164d-123">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e164d-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e164d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e164d-124">-ResourceGroupName</span></span>
<span data-ttu-id="e164d-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e164d-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e164d-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e164d-126">-Throughput</span></span>
<span data-ttu-id="e164d-127">A produtividade do banco de dados do Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e164d-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="e164d-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="e164d-128">Default value is 400.</span></span>

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

### <span data-ttu-id="e164d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e164d-129">-WhatIf</span></span>
<span data-ttu-id="e164d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e164d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e164d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e164d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e164d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e164d-132">CommonParameters</span></span>
<span data-ttu-id="e164d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e164d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e164d-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e164d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e164d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e164d-135">INPUTS</span></span>

### <span data-ttu-id="e164d-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e164d-136">None</span></span>

## <span data-ttu-id="e164d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e164d-137">OUTPUTS</span></span>

### <span data-ttu-id="e164d-138">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e164d-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="e164d-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="e164d-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="e164d-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e164d-140">NOTES</span></span>

## <span data-ttu-id="e164d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e164d-141">RELATED LINKS</span></span>
