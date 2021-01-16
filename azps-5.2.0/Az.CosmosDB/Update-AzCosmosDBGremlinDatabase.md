---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256796"
---
# <span data-ttu-id="b9cb2-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="b9cb2-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="b9cb2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="b9cb2-103">Atualiza o banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="b9cb2-104">Executa uma operação de patch do lado do cliente lendo o banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="b9cb2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9cb2-105">SYNTAX</span></span>

### <span data-ttu-id="b9cb2-106">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9cb2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9cb2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9cb2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9cb2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9cb2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9cb2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9cb2-109">DESCRIPTION</span></span>
<span data-ttu-id="b9cb2-110">Atualiza o banco de dados CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="b9cb2-111">Executa uma operação de patch do lado do cliente lendo o banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="b9cb2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9cb2-112">EXAMPLES</span></span>

### <span data-ttu-id="b9cb2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9cb2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="b9cb2-114">OS</span><span class="sxs-lookup"><span data-stu-id="b9cb2-114">PARAMETERS</span></span>

### <span data-ttu-id="b9cb2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b9cb2-115">-AccountName</span></span>
<span data-ttu-id="b9cb2-116">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b9cb2-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b9cb2-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b9cb2-118">Valor máximo de produtividade se a dimensionamento automático estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b9cb2-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9cb2-119">-Confirm</span></span>
<span data-ttu-id="b9cb2-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9cb2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9cb2-121">-DefaultProfile</span></span>
<span data-ttu-id="b9cb2-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9cb2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9cb2-123">-InputObject</span></span>
<span data-ttu-id="b9cb2-124">Objeto de banco de dados Gremlin.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9cb2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9cb2-125">-Name</span></span>
<span data-ttu-id="b9cb2-126">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-126">Database name.</span></span>

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

### <span data-ttu-id="b9cb2-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b9cb2-127">-ParentObject</span></span>
<span data-ttu-id="b9cb2-128">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b9cb2-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b9cb2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9cb2-129">-ResourceGroupName</span></span>
<span data-ttu-id="b9cb2-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b9cb2-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="b9cb2-131">-Throughput</span></span>
<span data-ttu-id="b9cb2-132">A produtividade do banco de dados do Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b9cb2-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="b9cb2-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b9cb2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9cb2-134">-WhatIf</span></span>
<span data-ttu-id="b9cb2-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9cb2-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9cb2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9cb2-137">CommonParameters</span></span>
<span data-ttu-id="b9cb2-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9cb2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9cb2-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9cb2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9cb2-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9cb2-140">INPUTS</span></span>

### <span data-ttu-id="b9cb2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b9cb2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="b9cb2-142">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b9cb2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b9cb2-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9cb2-143">OUTPUTS</span></span>

### <span data-ttu-id="b9cb2-144">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b9cb2-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="b9cb2-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b9cb2-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b9cb2-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9cb2-146">NOTES</span></span>

## <span data-ttu-id="b9cb2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9cb2-147">RELATED LINKS</span></span>
