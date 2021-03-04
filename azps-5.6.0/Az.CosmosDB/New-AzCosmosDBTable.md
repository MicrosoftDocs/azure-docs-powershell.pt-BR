---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: d2a4dacb929587fb0f06c002ad26df3144f32f56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886485"
---
# <span data-ttu-id="96608-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="96608-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="96608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96608-102">SYNOPSIS</span></span>
<span data-ttu-id="96608-103">Cria uma nova Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="96608-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="96608-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="96608-104">SYNTAX</span></span>

### <span data-ttu-id="96608-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96608-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96608-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96608-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96608-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="96608-107">DESCRIPTION</span></span>
<span data-ttu-id="96608-108">Cria uma nova Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="96608-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="96608-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96608-109">EXAMPLES</span></span>

### <span data-ttu-id="96608-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96608-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="96608-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="96608-111">PARAMETERS</span></span>

### <span data-ttu-id="96608-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="96608-112">-AccountName</span></span>
<span data-ttu-id="96608-113">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="96608-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="96608-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="96608-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="96608-115">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="96608-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="96608-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96608-116">-Confirm</span></span>
<span data-ttu-id="96608-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96608-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96608-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96608-118">-DefaultProfile</span></span>
<span data-ttu-id="96608-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96608-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96608-120">-Name</span><span class="sxs-lookup"><span data-stu-id="96608-120">-Name</span></span>
<span data-ttu-id="96608-121">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="96608-121">Name of the Table.</span></span>

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

### <span data-ttu-id="96608-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="96608-122">-ParentObject</span></span>
<span data-ttu-id="96608-123">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="96608-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="96608-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96608-124">-ResourceGroupName</span></span>
<span data-ttu-id="96608-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96608-125">Name of resource group.</span></span>

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

### <span data-ttu-id="96608-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="96608-126">-Throughput</span></span>
<span data-ttu-id="96608-127">A produtividade de Tabela (RU/s).</span><span class="sxs-lookup"><span data-stu-id="96608-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="96608-128">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="96608-128">Default value is 400.</span></span>

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

### <span data-ttu-id="96608-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96608-129">-WhatIf</span></span>
<span data-ttu-id="96608-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96608-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96608-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96608-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96608-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96608-132">CommonParameters</span></span>
<span data-ttu-id="96608-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96608-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96608-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96608-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96608-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96608-135">INPUTS</span></span>

### <span data-ttu-id="96608-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="96608-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="96608-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="96608-137">OUTPUTS</span></span>

### <span data-ttu-id="96608-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="96608-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="96608-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="96608-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="96608-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="96608-140">NOTES</span></span>

## <span data-ttu-id="96608-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96608-141">RELATED LINKS</span></span>
