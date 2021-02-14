---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: ac15f6ba4d8db1e4f3ab35c34b33b78fdefa05a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111046"
---
# <span data-ttu-id="9e3d7-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="9e3d7-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="9e3d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3d7-103">Use-a para migrar a produtividade em escala automática para a produtividade manual e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="9e3d7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e3d7-104">SYNTAX</span></span>

### <span data-ttu-id="9e3d7-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9e3d7-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3d7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3d7-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3d7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e3d7-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e3d7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e3d7-108">DESCRIPTION</span></span>
<span data-ttu-id="9e3d7-109">O paramter ThroughpyteType define a produtividade para a qual você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="9e3d7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9e3d7-110">EXAMPLES</span></span>

### <span data-ttu-id="9e3d7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9e3d7-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="9e3d7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e3d7-112">PARAMETERS</span></span>

### <span data-ttu-id="9e3d7-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="9e3d7-113">-AccountName</span></span>
<span data-ttu-id="9e3d7-114">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9e3d7-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9e3d7-115">-Confirm</span></span>
<span data-ttu-id="9e3d7-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e3d7-117">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="9e3d7-117">-DatabaseName</span></span>
<span data-ttu-id="9e3d7-118">Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-118">Database name.</span></span>

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

### <span data-ttu-id="9e3d7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3d7-119">-DefaultProfile</span></span>
<span data-ttu-id="9e3d7-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3d7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e3d7-121">-InputObject</span></span>
<span data-ttu-id="9e3d7-122">Objeto Contêiner Sql.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e3d7-123">-Name</span></span>
<span data-ttu-id="9e3d7-124">Nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-124">Container name.</span></span>

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

### <span data-ttu-id="9e3d7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9e3d7-125">-ParentObject</span></span>
<span data-ttu-id="9e3d7-126">Objeto banco de dados sql.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e3d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e3d7-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-128">Name of resource group.</span></span>

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

### <span data-ttu-id="9e3d7-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="9e3d7-129">-ThroughputType</span></span>
<span data-ttu-id="9e3d7-130">Tipo de produtividade para o qual migrar.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="9e3d7-131">Os valores possíveis são: Escala Automática, Manual.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="9e3d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e3d7-132">-WhatIf</span></span>
<span data-ttu-id="9e3d7-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e3d7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e3d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3d7-135">CommonParameters</span></span>
<span data-ttu-id="9e3d7-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3d7-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e3d7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3d7-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="9e3d7-138">INPUTS</span></span>

### <span data-ttu-id="9e3d7-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9e3d7-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="9e3d7-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="9e3d7-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="9e3d7-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="9e3d7-141">OUTPUTS</span></span>

### <span data-ttu-id="9e3d7-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9e3d7-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9e3d7-143">Notas</span><span class="sxs-lookup"><span data-stu-id="9e3d7-143">NOTES</span></span>

## <span data-ttu-id="9e3d7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e3d7-144">RELATED LINKS</span></span>
