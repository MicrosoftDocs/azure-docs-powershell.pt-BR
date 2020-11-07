---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944436"
---
# <span data-ttu-id="e6687-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="e6687-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="e6687-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6687-102">SYNOPSIS</span></span>
<span data-ttu-id="e6687-103">Define o banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e6687-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e6687-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6687-104">SYNTAX</span></span>

### <span data-ttu-id="e6687-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6687-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6687-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6687-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6687-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6687-107">DESCRIPTION</span></span>
<span data-ttu-id="e6687-108">O cmdlet **set-AzCosmosDBGremlinDatabase** define o banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e6687-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e6687-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6687-109">EXAMPLES</span></span>

### <span data-ttu-id="e6687-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e6687-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="e6687-111">Objeto de recurso contém _rid, _ts _etag.</span><span class="sxs-lookup"><span data-stu-id="e6687-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="e6687-112">OS</span><span class="sxs-lookup"><span data-stu-id="e6687-112">PARAMETERS</span></span>

### <span data-ttu-id="e6687-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e6687-113">-AccountName</span></span>
<span data-ttu-id="e6687-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="e6687-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e6687-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e6687-115">-Confirm</span></span>
<span data-ttu-id="e6687-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6687-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6687-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6687-117">-DefaultProfile</span></span>
<span data-ttu-id="e6687-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6687-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6687-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6687-119">-InputObject</span></span>
<span data-ttu-id="e6687-120">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e6687-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e6687-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6687-121">-Name</span></span>
<span data-ttu-id="e6687-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e6687-122">Database name.</span></span>

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

### <span data-ttu-id="e6687-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6687-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6687-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6687-124">Name of resource group.</span></span>

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

### <span data-ttu-id="e6687-125">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e6687-125">-Throughput</span></span>
<span data-ttu-id="e6687-126">A produtividade do banco de dados do Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e6687-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="e6687-127">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="e6687-127">Default value is 400.</span></span>

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

### <span data-ttu-id="e6687-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6687-128">-WhatIf</span></span>
<span data-ttu-id="e6687-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e6687-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6687-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6687-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6687-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6687-131">CommonParameters</span></span>
<span data-ttu-id="e6687-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6687-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6687-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6687-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6687-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6687-134">INPUTS</span></span>

### <span data-ttu-id="e6687-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e6687-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e6687-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6687-136">OUTPUTS</span></span>

### <span data-ttu-id="e6687-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e6687-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="e6687-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6687-138">NOTES</span></span>

## <span data-ttu-id="e6687-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6687-139">RELATED LINKS</span></span>
