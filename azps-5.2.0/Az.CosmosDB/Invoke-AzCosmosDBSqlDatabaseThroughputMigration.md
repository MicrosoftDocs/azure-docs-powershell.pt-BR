---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 927cdbd6c599b090a66120e95a1ac1a024360271
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262798"
---
# <span data-ttu-id="35ad6-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="35ad6-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="35ad6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="35ad6-103">Use isso para migrar a produtividade de AutoEscala para a taxa de transferência manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="35ad6-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="35ad6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35ad6-104">SYNTAX</span></span>

### <span data-ttu-id="35ad6-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="35ad6-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35ad6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35ad6-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35ad6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35ad6-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ad6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35ad6-108">DESCRIPTION</span></span>
<span data-ttu-id="35ad6-109">O parâmetro ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="35ad6-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="35ad6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35ad6-110">EXAMPLES</span></span>

### <span data-ttu-id="35ad6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35ad6-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="35ad6-112">OS</span><span class="sxs-lookup"><span data-stu-id="35ad6-112">PARAMETERS</span></span>

### <span data-ttu-id="35ad6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="35ad6-113">-AccountName</span></span>
<span data-ttu-id="35ad6-114">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="35ad6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="35ad6-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35ad6-115">-Confirm</span></span>
<span data-ttu-id="35ad6-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ad6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ad6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ad6-117">-DefaultProfile</span></span>
<span data-ttu-id="35ad6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35ad6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ad6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35ad6-119">-InputObject</span></span>
<span data-ttu-id="35ad6-120">Objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="35ad6-120">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35ad6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="35ad6-121">-Name</span></span>
<span data-ttu-id="35ad6-122">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35ad6-122">Database name.</span></span>

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

### <span data-ttu-id="35ad6-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="35ad6-123">-ParentObject</span></span>
<span data-ttu-id="35ad6-124">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="35ad6-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="35ad6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ad6-125">-ResourceGroupName</span></span>
<span data-ttu-id="35ad6-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35ad6-126">Name of resource group.</span></span>

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

### <span data-ttu-id="35ad6-127">-Throughputtype</span><span class="sxs-lookup"><span data-stu-id="35ad6-127">-ThroughputType</span></span>
<span data-ttu-id="35ad6-128">Tipo de produtividade para migração.</span><span class="sxs-lookup"><span data-stu-id="35ad6-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="35ad6-129">Os valores possíveis são: autoescala, manual.</span><span class="sxs-lookup"><span data-stu-id="35ad6-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="35ad6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ad6-130">-WhatIf</span></span>
<span data-ttu-id="35ad6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35ad6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ad6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35ad6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ad6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ad6-133">CommonParameters</span></span>
<span data-ttu-id="35ad6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ad6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ad6-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35ad6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ad6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35ad6-136">INPUTS</span></span>

### <span data-ttu-id="35ad6-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="35ad6-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="35ad6-138">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="35ad6-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="35ad6-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35ad6-139">OUTPUTS</span></span>

### <span data-ttu-id="35ad6-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="35ad6-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="35ad6-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35ad6-141">NOTES</span></span>

## <span data-ttu-id="35ad6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35ad6-142">RELATED LINKS</span></span>
