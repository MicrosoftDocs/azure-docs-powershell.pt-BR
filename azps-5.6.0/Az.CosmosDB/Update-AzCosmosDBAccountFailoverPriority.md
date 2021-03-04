---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 2d3555d879d05e1235fb8713e75c9b27fca46b51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892987"
---
# <span data-ttu-id="89dbe-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="89dbe-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="89dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="89dbe-103">{{ Preencha a Synopsis }}</span><span class="sxs-lookup"><span data-stu-id="89dbe-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="89dbe-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="89dbe-104">SYNTAX</span></span>

### <span data-ttu-id="89dbe-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="89dbe-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89dbe-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89dbe-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89dbe-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89dbe-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89dbe-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="89dbe-108">DESCRIPTION</span></span>
<span data-ttu-id="89dbe-109">{{ Preencha a Descrição }}</span><span class="sxs-lookup"><span data-stu-id="89dbe-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="89dbe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89dbe-110">EXAMPLES</span></span>

### <span data-ttu-id="89dbe-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89dbe-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="89dbe-112">FailoverPolicies atualizadas com a região1 como FailoverPriority 1, região2 como FailoverPriority 2 e região3 como FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="89dbe-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="89dbe-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="89dbe-113">PARAMETERS</span></span>

### <span data-ttu-id="89dbe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89dbe-114">-AsJob</span></span>
<span data-ttu-id="89dbe-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89dbe-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dbe-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89dbe-116">-Confirm</span></span>
<span data-ttu-id="89dbe-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89dbe-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89dbe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89dbe-118">-DefaultProfile</span></span>
<span data-ttu-id="89dbe-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89dbe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89dbe-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="89dbe-120">-FailoverPolicy</span></span>
<span data-ttu-id="89dbe-121">Matriz de cadeias de caracteres com nomes de região, ordenadas por prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="89dbe-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="89dbe-122">Por exemplo, eastus, westus</span><span class="sxs-lookup"><span data-stu-id="89dbe-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dbe-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89dbe-123">-InputObject</span></span>
<span data-ttu-id="89dbe-124">Objeto Conta do CosmosDB</span><span class="sxs-lookup"><span data-stu-id="89dbe-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89dbe-125">-Name</span><span class="sxs-lookup"><span data-stu-id="89dbe-125">-Name</span></span>
<span data-ttu-id="89dbe-126">Nome da conta de banco de dados db do Cosmos.</span><span class="sxs-lookup"><span data-stu-id="89dbe-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="89dbe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89dbe-127">-ResourceGroupName</span></span>
<span data-ttu-id="89dbe-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="89dbe-128">Name of resource group.</span></span>

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

### <span data-ttu-id="89dbe-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89dbe-129">-ResourceId</span></span>
<span data-ttu-id="89dbe-130">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="89dbe-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dbe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89dbe-131">-WhatIf</span></span>
<span data-ttu-id="89dbe-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89dbe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89dbe-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89dbe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89dbe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89dbe-134">CommonParameters</span></span>
<span data-ttu-id="89dbe-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89dbe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89dbe-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89dbe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89dbe-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89dbe-137">INPUTS</span></span>

### <span data-ttu-id="89dbe-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="89dbe-138">None</span></span>

## <span data-ttu-id="89dbe-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="89dbe-139">OUTPUTS</span></span>

### <span data-ttu-id="89dbe-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="89dbe-140">System.Void</span></span>

## <span data-ttu-id="89dbe-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="89dbe-141">NOTES</span></span>

## <span data-ttu-id="89dbe-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89dbe-142">RELATED LINKS</span></span>
