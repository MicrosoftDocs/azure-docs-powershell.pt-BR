---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112040"
---
# <span data-ttu-id="9bf6a-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="9bf6a-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="9bf6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf6a-103">Atualiza o Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="9bf6a-104">Executa uma operação de patch do lado do cliente lendo o Banco de Dados existente.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="9bf6a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bf6a-105">SYNTAX</span></span>

### <span data-ttu-id="9bf6a-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9bf6a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf6a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bf6a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bf6a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bf6a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bf6a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bf6a-109">DESCRIPTION</span></span>
<span data-ttu-id="9bf6a-110">Atualiza o Banco de Dados de Gremlin do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="9bf6a-111">Executa uma operação de patch do lado do cliente lendo o Banco de Dados existente.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="9bf6a-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bf6a-112">EXAMPLES</span></span>

### <span data-ttu-id="9bf6a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9bf6a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="9bf6a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bf6a-114">PARAMETERS</span></span>

### <span data-ttu-id="9bf6a-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="9bf6a-115">-AccountName</span></span>
<span data-ttu-id="9bf6a-116">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9bf6a-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9bf6a-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9bf6a-118">Valor máximo de produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9bf6a-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9bf6a-119">-Confirm</span></span>
<span data-ttu-id="9bf6a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf6a-121">-DefaultProfile</span></span>
<span data-ttu-id="9bf6a-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf6a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bf6a-123">-InputObject</span></span>
<span data-ttu-id="9bf6a-124">Objeto de Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="9bf6a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bf6a-125">-Name</span></span>
<span data-ttu-id="9bf6a-126">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-126">Database name.</span></span>

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

### <span data-ttu-id="9bf6a-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9bf6a-127">-ParentObject</span></span>
<span data-ttu-id="9bf6a-128">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="9bf6a-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9bf6a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf6a-129">-ResourceGroupName</span></span>
<span data-ttu-id="9bf6a-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="9bf6a-131">-Produtividade</span><span class="sxs-lookup"><span data-stu-id="9bf6a-131">-Throughput</span></span>
<span data-ttu-id="9bf6a-132">A produtividade do Banco de Dados de Gremlin (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9bf6a-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="9bf6a-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-133">Default value is 400.</span></span>

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

### <span data-ttu-id="9bf6a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf6a-134">-WhatIf</span></span>
<span data-ttu-id="9bf6a-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf6a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf6a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf6a-137">CommonParameters</span></span>
<span data-ttu-id="9bf6a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf6a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf6a-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bf6a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf6a-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="9bf6a-140">INPUTS</span></span>

### <span data-ttu-id="9bf6a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9bf6a-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="9bf6a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9bf6a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="9bf6a-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="9bf6a-143">OUTPUTS</span></span>

### <span data-ttu-id="9bf6a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9bf6a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="9bf6a-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="9bf6a-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="9bf6a-146">Notas</span><span class="sxs-lookup"><span data-stu-id="9bf6a-146">NOTES</span></span>

## <span data-ttu-id="9bf6a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bf6a-147">RELATED LINKS</span></span>
