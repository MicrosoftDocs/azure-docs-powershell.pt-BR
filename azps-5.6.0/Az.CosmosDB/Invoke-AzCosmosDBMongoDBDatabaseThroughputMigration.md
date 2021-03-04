---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: c1ae582bcbf5fb2a19ee3c1904635dd886cbf8fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888568"
---
# <span data-ttu-id="9e399-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="9e399-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="9e399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e399-102">SYNOPSIS</span></span>
<span data-ttu-id="9e399-103">Use isso para migrar a produtividade de escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="9e399-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="9e399-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9e399-104">SYNTAX</span></span>

### <span data-ttu-id="9e399-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9e399-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e399-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e399-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e399-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e399-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e399-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9e399-108">DESCRIPTION</span></span>
<span data-ttu-id="9e399-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="9e399-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="9e399-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e399-110">EXAMPLES</span></span>

### <span data-ttu-id="9e399-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9e399-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="9e399-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9e399-112">PARAMETERS</span></span>

### <span data-ttu-id="9e399-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9e399-113">-AccountName</span></span>
<span data-ttu-id="9e399-114">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="9e399-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9e399-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e399-115">-Confirm</span></span>
<span data-ttu-id="9e399-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e399-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e399-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e399-117">-DefaultProfile</span></span>
<span data-ttu-id="9e399-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e399-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e399-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e399-119">-InputObject</span></span>
<span data-ttu-id="9e399-120">Objeto Mongo Database.</span><span class="sxs-lookup"><span data-stu-id="9e399-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="9e399-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9e399-121">-Name</span></span>
<span data-ttu-id="9e399-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9e399-122">Database name.</span></span>

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

### <span data-ttu-id="9e399-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9e399-123">-ParentObject</span></span>
<span data-ttu-id="9e399-124">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="9e399-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9e399-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e399-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e399-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e399-126">Name of resource group.</span></span>

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

### <span data-ttu-id="9e399-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="9e399-127">-ThroughputType</span></span>
<span data-ttu-id="9e399-128">Tipo de transferência para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="9e399-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="9e399-129">Os valores possíveis são: Escala automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="9e399-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="9e399-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e399-130">-WhatIf</span></span>
<span data-ttu-id="9e399-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e399-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e399-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e399-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e399-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e399-133">CommonParameters</span></span>
<span data-ttu-id="9e399-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e399-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e399-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e399-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e399-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e399-136">INPUTS</span></span>

### <span data-ttu-id="9e399-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9e399-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="9e399-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9e399-138">OUTPUTS</span></span>

### <span data-ttu-id="9e399-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9e399-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9e399-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="9e399-140">NOTES</span></span>

## <span data-ttu-id="9e399-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e399-141">RELATED LINKS</span></span>
