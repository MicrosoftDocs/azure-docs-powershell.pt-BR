---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: a223fd71ecf65ecb34b605e79ee0d6f7670d3a4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888556"
---
# <span data-ttu-id="071ce-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="071ce-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="071ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="071ce-102">SYNOPSIS</span></span>
<span data-ttu-id="071ce-103">Atualiza o Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="071ce-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="071ce-104">Executa uma operação de patch do lado do cliente lendo o Banco de Dados existente.</span><span class="sxs-lookup"><span data-stu-id="071ce-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="071ce-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="071ce-105">SYNTAX</span></span>

### <span data-ttu-id="071ce-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="071ce-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="071ce-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="071ce-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="071ce-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="071ce-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="071ce-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="071ce-109">DESCRIPTION</span></span>
<span data-ttu-id="071ce-110">Atualiza o Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="071ce-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="071ce-111">Executa uma operação de patch do lado do cliente lendo o Banco de Dados existente.</span><span class="sxs-lookup"><span data-stu-id="071ce-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="071ce-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="071ce-112">EXAMPLES</span></span>

### <span data-ttu-id="071ce-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="071ce-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="071ce-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="071ce-114">PARAMETERS</span></span>

### <span data-ttu-id="071ce-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="071ce-115">-AccountName</span></span>
<span data-ttu-id="071ce-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="071ce-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="071ce-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="071ce-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="071ce-118">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="071ce-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="071ce-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="071ce-119">-Confirm</span></span>
<span data-ttu-id="071ce-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="071ce-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="071ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="071ce-121">-DefaultProfile</span></span>
<span data-ttu-id="071ce-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="071ce-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="071ce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="071ce-123">-InputObject</span></span>
<span data-ttu-id="071ce-124">Objeto Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="071ce-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="071ce-125">-Name</span><span class="sxs-lookup"><span data-stu-id="071ce-125">-Name</span></span>
<span data-ttu-id="071ce-126">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="071ce-126">Database name.</span></span>

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

### <span data-ttu-id="071ce-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="071ce-127">-ParentObject</span></span>
<span data-ttu-id="071ce-128">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="071ce-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="071ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="071ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="071ce-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="071ce-130">Name of resource group.</span></span>

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

### <span data-ttu-id="071ce-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="071ce-131">-Throughput</span></span>
<span data-ttu-id="071ce-132">A produtividade do Banco de Dados de Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="071ce-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="071ce-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="071ce-133">Default value is 400.</span></span>

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

### <span data-ttu-id="071ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="071ce-134">-WhatIf</span></span>
<span data-ttu-id="071ce-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="071ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="071ce-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="071ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="071ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="071ce-137">CommonParameters</span></span>
<span data-ttu-id="071ce-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="071ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="071ce-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="071ce-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="071ce-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="071ce-140">INPUTS</span></span>

### <span data-ttu-id="071ce-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="071ce-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="071ce-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="071ce-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="071ce-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="071ce-143">OUTPUTS</span></span>

### <span data-ttu-id="071ce-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="071ce-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="071ce-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="071ce-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="071ce-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="071ce-146">NOTES</span></span>

## <span data-ttu-id="071ce-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="071ce-147">RELATED LINKS</span></span>
