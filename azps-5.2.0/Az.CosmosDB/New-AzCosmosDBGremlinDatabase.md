---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260876"
---
# <span data-ttu-id="b8c74-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c74-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="b8c74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8c74-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c74-103">Cria um novo banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b8c74-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b8c74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8c74-104">SYNTAX</span></span>

### <span data-ttu-id="b8c74-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8c74-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c74-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8c74-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c74-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8c74-107">DESCRIPTION</span></span>
<span data-ttu-id="b8c74-108">Cria um novo banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b8c74-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b8c74-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8c74-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c74-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8c74-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="b8c74-111">OS</span><span class="sxs-lookup"><span data-stu-id="b8c74-111">PARAMETERS</span></span>

### <span data-ttu-id="b8c74-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b8c74-112">-AccountName</span></span>
<span data-ttu-id="b8c74-113">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="b8c74-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b8c74-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b8c74-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b8c74-115">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="b8c74-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b8c74-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8c74-116">-Confirm</span></span>
<span data-ttu-id="b8c74-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c74-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c74-118">-DefaultProfile</span></span>
<span data-ttu-id="b8c74-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c74-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c74-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8c74-120">-Name</span></span>
<span data-ttu-id="b8c74-121">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b8c74-121">Database name.</span></span>

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

### <span data-ttu-id="b8c74-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b8c74-122">-ParentObject</span></span>
<span data-ttu-id="b8c74-123">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b8c74-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b8c74-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c74-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8c74-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8c74-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b8c74-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="b8c74-126">-Throughput</span></span>
<span data-ttu-id="b8c74-127">A produtividade do banco de dados do Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b8c74-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="b8c74-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="b8c74-128">Default value is 400.</span></span>

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

### <span data-ttu-id="b8c74-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c74-129">-WhatIf</span></span>
<span data-ttu-id="b8c74-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8c74-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c74-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8c74-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c74-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c74-132">CommonParameters</span></span>
<span data-ttu-id="b8c74-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c74-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c74-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8c74-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c74-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8c74-135">INPUTS</span></span>

### <span data-ttu-id="b8c74-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b8c74-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b8c74-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8c74-137">OUTPUTS</span></span>

### <span data-ttu-id="b8c74-138">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b8c74-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="b8c74-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="b8c74-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="b8c74-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8c74-140">NOTES</span></span>

## <span data-ttu-id="b8c74-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8c74-141">RELATED LINKS</span></span>
