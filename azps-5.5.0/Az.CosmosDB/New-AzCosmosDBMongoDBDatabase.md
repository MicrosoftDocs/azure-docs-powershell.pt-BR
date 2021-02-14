---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111029"
---
# <span data-ttu-id="8ce50-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="8ce50-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="8ce50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ce50-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce50-103">Cria um novo Banco de Dados MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8ce50-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="8ce50-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ce50-104">SYNTAX</span></span>

### <span data-ttu-id="8ce50-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8ce50-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ce50-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ce50-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ce50-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ce50-107">DESCRIPTION</span></span>
<span data-ttu-id="8ce50-108">Cria um novo Banco de Dados MongoDB do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8ce50-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="8ce50-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ce50-109">EXAMPLES</span></span>

### <span data-ttu-id="8ce50-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ce50-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="8ce50-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ce50-111">PARAMETERS</span></span>

### <span data-ttu-id="8ce50-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="8ce50-112">-AccountName</span></span>
<span data-ttu-id="8ce50-113">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="8ce50-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8ce50-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8ce50-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8ce50-115">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="8ce50-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8ce50-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8ce50-116">-Confirm</span></span>
<span data-ttu-id="8ce50-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ce50-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce50-118">-DefaultProfile</span></span>
<span data-ttu-id="8ce50-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ce50-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ce50-120">-Name</span></span>
<span data-ttu-id="8ce50-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8ce50-121">Database name.</span></span>

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

### <span data-ttu-id="8ce50-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8ce50-122">-ParentObject</span></span>
<span data-ttu-id="8ce50-123">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="8ce50-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8ce50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce50-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ce50-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ce50-125">Name of resource group.</span></span>

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

### <span data-ttu-id="8ce50-126">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="8ce50-126">-Throughput</span></span>
<span data-ttu-id="8ce50-127">A produtividade do banco de dados Mongo (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8ce50-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="8ce50-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="8ce50-128">Default value is 400.</span></span>

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

### <span data-ttu-id="8ce50-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce50-129">-WhatIf</span></span>
<span data-ttu-id="8ce50-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8ce50-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ce50-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ce50-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce50-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce50-132">CommonParameters</span></span>
<span data-ttu-id="8ce50-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce50-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce50-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ce50-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce50-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="8ce50-135">INPUTS</span></span>

### <span data-ttu-id="8ce50-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8ce50-136">None</span></span>

## <span data-ttu-id="8ce50-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="8ce50-137">OUTPUTS</span></span>

### <span data-ttu-id="8ce50-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8ce50-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="8ce50-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="8ce50-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="8ce50-140">Notas</span><span class="sxs-lookup"><span data-stu-id="8ce50-140">NOTES</span></span>

## <span data-ttu-id="8ce50-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ce50-141">RELATED LINKS</span></span>
