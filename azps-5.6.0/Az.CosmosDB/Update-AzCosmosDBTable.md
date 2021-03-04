---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: 3463a07219375db06495bd5d50a2fe3b5916e173
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892862"
---
# <span data-ttu-id="8ef4f-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="8ef4f-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="8ef4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ef4f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef4f-103">Atualiza a Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="8ef4f-104">Executa uma operação de patch do lado do cliente lendo a Tabela existente.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="8ef4f-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8ef4f-105">SYNTAX</span></span>

### <span data-ttu-id="8ef4f-106">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8ef4f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef4f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef4f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef4f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ef4f-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8ef4f-109">DESCRIPTION</span></span>
<span data-ttu-id="8ef4f-110">Atualiza a Tabela Do CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="8ef4f-111">Executa uma operação de patch do lado do cliente lendo a Tabela existente.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="8ef4f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ef4f-112">EXAMPLES</span></span>

### <span data-ttu-id="8ef4f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ef4f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="8ef4f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8ef4f-114">PARAMETERS</span></span>

### <span data-ttu-id="8ef4f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ef4f-115">-AccountName</span></span>
<span data-ttu-id="8ef4f-116">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8ef4f-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8ef4f-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8ef4f-118">Valor máximo de Produtividade se a escala automática estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8ef4f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ef4f-119">-Confirm</span></span>
<span data-ttu-id="8ef4f-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ef4f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef4f-121">-DefaultProfile</span></span>
<span data-ttu-id="8ef4f-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ef4f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ef4f-123">-InputObject</span></span>
<span data-ttu-id="8ef4f-124">Objeto Table.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-124">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef4f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8ef4f-125">-Name</span></span>
<span data-ttu-id="8ef4f-126">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-126">Name of the Table.</span></span>

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

### <span data-ttu-id="8ef4f-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8ef4f-127">-ParentObject</span></span>
<span data-ttu-id="8ef4f-128">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8ef4f-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8ef4f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef4f-129">-ResourceGroupName</span></span>
<span data-ttu-id="8ef4f-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-130">Name of resource group.</span></span>

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

### <span data-ttu-id="8ef4f-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="8ef4f-131">-Throughput</span></span>
<span data-ttu-id="8ef4f-132">A produtividade de Tabela (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8ef4f-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="8ef4f-133">O valor padrão é 400.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-133">Default value is 400.</span></span>

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

### <span data-ttu-id="8ef4f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ef4f-134">-WhatIf</span></span>
<span data-ttu-id="8ef4f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ef4f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ef4f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef4f-137">CommonParameters</span></span>
<span data-ttu-id="8ef4f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef4f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef4f-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ef4f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef4f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ef4f-140">INPUTS</span></span>

### <span data-ttu-id="8ef4f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8ef4f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="8ef4f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="8ef4f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="8ef4f-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8ef4f-143">OUTPUTS</span></span>

### <span data-ttu-id="8ef4f-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="8ef4f-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="8ef4f-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8ef4f-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="8ef4f-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="8ef4f-146">NOTES</span></span>

## <span data-ttu-id="8ef4f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ef4f-147">RELATED LINKS</span></span>
