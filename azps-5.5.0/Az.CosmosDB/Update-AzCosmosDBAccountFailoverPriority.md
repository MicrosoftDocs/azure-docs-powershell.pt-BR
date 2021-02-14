---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111024"
---
# <span data-ttu-id="f0b1f-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="f0b1f-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="f0b1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b1f-103">{{ Fill in the Synopsis }}</span><span class="sxs-lookup"><span data-stu-id="f0b1f-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="f0b1f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0b1f-104">SYNTAX</span></span>

### <span data-ttu-id="f0b1f-105">ByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f0b1f-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b1f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b1f-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b1f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b1f-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0b1f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0b1f-108">DESCRIPTION</span></span>
<span data-ttu-id="f0b1f-109">{{ Preencha a Descrição }}</span><span class="sxs-lookup"><span data-stu-id="f0b1f-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="f0b1f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0b1f-110">EXAMPLES</span></span>

### <span data-ttu-id="f0b1f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0b1f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="f0b1f-112">FailoverPolicies atualizados com região1 como FailoverPriority 1, região2 como FailoverPriority 2 e região3 como FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="f0b1f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0b1f-113">PARAMETERS</span></span>

### <span data-ttu-id="f0b1f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0b1f-114">-AsJob</span></span>
<span data-ttu-id="f0b1f-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f0b1f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0b1f-116">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f0b1f-116">-Confirm</span></span>
<span data-ttu-id="f0b1f-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b1f-118">-DefaultProfile</span></span>
<span data-ttu-id="f0b1f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0b1f-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f0b1f-120">-FailoverPolicy</span></span>
<span data-ttu-id="f0b1f-121">Matriz de cadeias de caracteres com nomes de região, ordenadas por prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="f0b1f-122">Por exemplo, eastus, westus</span><span class="sxs-lookup"><span data-stu-id="f0b1f-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="f0b1f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0b1f-123">-InputObject</span></span>
<span data-ttu-id="f0b1f-124">Objeto conta doDbDb</span><span class="sxs-lookup"><span data-stu-id="f0b1f-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f0b1f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0b1f-125">-Name</span></span>
<span data-ttu-id="f0b1f-126">Nome da conta de banco de dados Do Db Db.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f0b1f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b1f-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0b1f-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="f0b1f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b1f-129">-ResourceId</span></span>
<span data-ttu-id="f0b1f-130">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="f0b1f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b1f-131">-WhatIf</span></span>
<span data-ttu-id="f0b1f-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b1f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b1f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b1f-134">CommonParameters</span></span>
<span data-ttu-id="f0b1f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b1f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b1f-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0b1f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b1f-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="f0b1f-137">INPUTS</span></span>

### <span data-ttu-id="f0b1f-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f0b1f-138">None</span></span>

## <span data-ttu-id="f0b1f-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="f0b1f-139">OUTPUTS</span></span>

### <span data-ttu-id="f0b1f-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="f0b1f-140">System.Void</span></span>

## <span data-ttu-id="f0b1f-141">Notas</span><span class="sxs-lookup"><span data-stu-id="f0b1f-141">NOTES</span></span>

## <span data-ttu-id="f0b1f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0b1f-142">RELATED LINKS</span></span>
