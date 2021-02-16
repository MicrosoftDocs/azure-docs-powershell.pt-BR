---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 79dcea6f66d01e9bfa2dd53b990a8f38ec5b0f2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117794"
---
# <span data-ttu-id="65be1-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="65be1-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="65be1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65be1-102">SYNOPSIS</span></span>
<span data-ttu-id="65be1-103">Use isso para migrar a produtividade em escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="65be1-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="65be1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65be1-104">SYNTAX</span></span>

### <span data-ttu-id="65be1-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65be1-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65be1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65be1-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65be1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65be1-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65be1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="65be1-108">DESCRIPTION</span></span>
<span data-ttu-id="65be1-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="65be1-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="65be1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65be1-110">EXAMPLES</span></span>

### <span data-ttu-id="65be1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65be1-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="65be1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65be1-112">PARAMETERS</span></span>

### <span data-ttu-id="65be1-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="65be1-113">-AccountName</span></span>
<span data-ttu-id="65be1-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="65be1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="65be1-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="65be1-115">-Confirm</span></span>
<span data-ttu-id="65be1-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65be1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65be1-117">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="65be1-117">-DatabaseName</span></span>
<span data-ttu-id="65be1-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="65be1-118">Database name.</span></span>

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

### <span data-ttu-id="65be1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65be1-119">-DefaultProfile</span></span>
<span data-ttu-id="65be1-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65be1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65be1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65be1-121">-InputObject</span></span>
<span data-ttu-id="65be1-122">Objeto Mongo Collection.</span><span class="sxs-lookup"><span data-stu-id="65be1-122">Mongo Collection object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65be1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="65be1-123">-Name</span></span>
<span data-ttu-id="65be1-124">Nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="65be1-124">Collection name.</span></span>

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

### <span data-ttu-id="65be1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="65be1-125">-ParentObject</span></span>
<span data-ttu-id="65be1-126">Objeto banco de dados Mongo.</span><span class="sxs-lookup"><span data-stu-id="65be1-126">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65be1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65be1-127">-ResourceGroupName</span></span>
<span data-ttu-id="65be1-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65be1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="65be1-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="65be1-129">-ThroughputType</span></span>
<span data-ttu-id="65be1-130">Tipo de produtividade para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="65be1-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="65be1-131">Os valores possíveis são: Escala Automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="65be1-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="65be1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65be1-132">-WhatIf</span></span>
<span data-ttu-id="65be1-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="65be1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65be1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65be1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65be1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65be1-135">CommonParameters</span></span>
<span data-ttu-id="65be1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65be1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65be1-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65be1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65be1-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="65be1-138">INPUTS</span></span>

### <span data-ttu-id="65be1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="65be1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="65be1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="65be1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="65be1-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="65be1-141">OUTPUTS</span></span>

### <span data-ttu-id="65be1-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="65be1-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="65be1-143">Notas</span><span class="sxs-lookup"><span data-stu-id="65be1-143">NOTES</span></span>

## <span data-ttu-id="65be1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65be1-144">RELATED LINKS</span></span>
