---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948376"
---
# <span data-ttu-id="56f95-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="56f95-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="56f95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56f95-102">SYNOPSIS</span></span>
<span data-ttu-id="56f95-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="56f95-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="56f95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56f95-104">SYNTAX</span></span>

### <span data-ttu-id="56f95-105">ByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="56f95-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56f95-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56f95-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56f95-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56f95-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56f95-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56f95-108">DESCRIPTION</span></span>
<span data-ttu-id="56f95-109">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="56f95-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="56f95-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56f95-110">EXAMPLES</span></span>

### <span data-ttu-id="56f95-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56f95-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="56f95-112">FailoverPolicies atualizado com region1 como FailoverPriority 1, region2 como FailoverPriority 2 e region3 como FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="56f95-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="56f95-113">OS</span><span class="sxs-lookup"><span data-stu-id="56f95-113">PARAMETERS</span></span>

### <span data-ttu-id="56f95-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56f95-114">-AsJob</span></span>
<span data-ttu-id="56f95-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="56f95-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56f95-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="56f95-116">-Confirm</span></span>
<span data-ttu-id="56f95-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56f95-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56f95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f95-118">-DefaultProfile</span></span>
<span data-ttu-id="56f95-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56f95-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56f95-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="56f95-120">-FailoverPolicy</span></span>
<span data-ttu-id="56f95-121">Matriz de cadeias de caracteres com nomes de regiões, ordenados pela prioridade de failover.</span><span class="sxs-lookup"><span data-stu-id="56f95-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="56f95-122">Por exemplo, eastus, westus</span><span class="sxs-lookup"><span data-stu-id="56f95-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="56f95-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56f95-123">-InputObject</span></span>
<span data-ttu-id="56f95-124">Objeto da conta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="56f95-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="56f95-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="56f95-125">-Name</span></span>
<span data-ttu-id="56f95-126">Nome da conta de banco de dados de banco de dados do cosmos.</span><span class="sxs-lookup"><span data-stu-id="56f95-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="56f95-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f95-127">-ResourceGroupName</span></span>
<span data-ttu-id="56f95-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56f95-128">Name of resource group.</span></span>

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

### <span data-ttu-id="56f95-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56f95-129">-ResourceId</span></span>
<span data-ttu-id="56f95-130">ResourceId do recurso.</span><span class="sxs-lookup"><span data-stu-id="56f95-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="56f95-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56f95-131">-WhatIf</span></span>
<span data-ttu-id="56f95-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56f95-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56f95-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56f95-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56f95-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f95-134">CommonParameters</span></span>
<span data-ttu-id="56f95-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f95-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f95-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56f95-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f95-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56f95-137">INPUTS</span></span>

### <span data-ttu-id="56f95-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="56f95-138">None</span></span>

## <span data-ttu-id="56f95-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56f95-139">OUTPUTS</span></span>

### <span data-ttu-id="56f95-140">System. void</span><span class="sxs-lookup"><span data-stu-id="56f95-140">System.Void</span></span>

## <span data-ttu-id="56f95-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56f95-141">NOTES</span></span>

## <span data-ttu-id="56f95-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56f95-142">RELATED LINKS</span></span>
