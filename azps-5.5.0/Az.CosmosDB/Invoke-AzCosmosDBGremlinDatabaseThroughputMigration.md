---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 3369415e3c5169695b04ccc8677c3bf0d2f99cd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112048"
---
# <span data-ttu-id="a03ce-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="a03ce-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="a03ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a03ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a03ce-103">Use isso para migrar a produtividade em escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a03ce-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="a03ce-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a03ce-104">SYNTAX</span></span>

### <span data-ttu-id="a03ce-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a03ce-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a03ce-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03ce-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a03ce-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03ce-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a03ce-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a03ce-108">DESCRIPTION</span></span>
<span data-ttu-id="a03ce-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="a03ce-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="a03ce-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a03ce-110">EXAMPLES</span></span>

### <span data-ttu-id="a03ce-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a03ce-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```

## <span data-ttu-id="a03ce-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a03ce-112">PARAMETERS</span></span>

### <span data-ttu-id="a03ce-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="a03ce-113">-AccountName</span></span>
<span data-ttu-id="a03ce-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="a03ce-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a03ce-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a03ce-115">-Confirm</span></span>
<span data-ttu-id="a03ce-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a03ce-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a03ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03ce-117">-DefaultProfile</span></span>
<span data-ttu-id="a03ce-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a03ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a03ce-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a03ce-119">-InputObject</span></span>
<span data-ttu-id="a03ce-120">Objeto de Banco de Dados de Gremlin.</span><span class="sxs-lookup"><span data-stu-id="a03ce-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="a03ce-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a03ce-121">-Name</span></span>
<span data-ttu-id="a03ce-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a03ce-122">Database name.</span></span>

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

### <span data-ttu-id="a03ce-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a03ce-123">-ParentObject</span></span>
<span data-ttu-id="a03ce-124">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="a03ce-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a03ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a03ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="a03ce-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a03ce-126">Name of resource group.</span></span>

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

### <span data-ttu-id="a03ce-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="a03ce-127">-ThroughputType</span></span>
<span data-ttu-id="a03ce-128">Tipo de produtividade para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="a03ce-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="a03ce-129">Os valores possíveis são: Escala Automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="a03ce-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="a03ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a03ce-130">-WhatIf</span></span>
<span data-ttu-id="a03ce-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a03ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a03ce-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a03ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a03ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03ce-133">CommonParameters</span></span>
<span data-ttu-id="a03ce-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03ce-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a03ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03ce-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="a03ce-136">INPUTS</span></span>

### <span data-ttu-id="a03ce-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="a03ce-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="a03ce-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a03ce-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="a03ce-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="a03ce-139">OUTPUTS</span></span>

### <span data-ttu-id="a03ce-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a03ce-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a03ce-141">Notas</span><span class="sxs-lookup"><span data-stu-id="a03ce-141">NOTES</span></span>

## <span data-ttu-id="a03ce-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a03ce-142">RELATED LINKS</span></span>
