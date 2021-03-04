---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: c34bb862d3928e6dbbaa55a9660c4868e38941b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893126"
---
# <span data-ttu-id="8880d-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="8880d-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="8880d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8880d-102">SYNOPSIS</span></span>
<span data-ttu-id="8880d-103">Criar cluster</span><span class="sxs-lookup"><span data-stu-id="8880d-103">Create cluster</span></span>

## <span data-ttu-id="8880d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8880d-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8880d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8880d-105">DESCRIPTION</span></span>

<span data-ttu-id="8880d-106">Criar cluster</span><span class="sxs-lookup"><span data-stu-id="8880d-106">Create cluster</span></span>

## <span data-ttu-id="8880d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8880d-107">EXAMPLES</span></span>

### <span data-ttu-id="8880d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8880d-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="8880d-109">Criar cluster</span><span class="sxs-lookup"><span data-stu-id="8880d-109">Create cluster</span></span>

## <span data-ttu-id="8880d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8880d-110">PARAMETERS</span></span>

### <span data-ttu-id="8880d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8880d-111">-AsJob</span></span>
<span data-ttu-id="8880d-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8880d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8880d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8880d-113">-ClusterName</span></span>
<span data-ttu-id="8880d-114">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="8880d-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8880d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8880d-115">-DefaultProfile</span></span>
<span data-ttu-id="8880d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8880d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8880d-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8880d-117">-IdentityType</span></span>
<span data-ttu-id="8880d-118">o tipo de identidade, o valor pode ser 'SystemAssigned', 'None'.</span><span class="sxs-lookup"><span data-stu-id="8880d-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8880d-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8880d-119">-Location</span></span>
<span data-ttu-id="8880d-120">A região geográfica que o cluster será implantado.</span><span class="sxs-lookup"><span data-stu-id="8880d-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8880d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8880d-121">-ResourceGroupName</span></span>
<span data-ttu-id="8880d-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8880d-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8880d-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8880d-123">-SkuCapacity</span></span>
<span data-ttu-id="8880d-124">Capacidade Sku, o valor precisa ser múltiplo de 100 e no intervalo de 1000 a 2000.</span><span class="sxs-lookup"><span data-stu-id="8880d-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8880d-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8880d-125">-SkuName</span></span>
<span data-ttu-id="8880d-126">Nome Sku, agora pode ser somente 'CapacityReservation'</span><span class="sxs-lookup"><span data-stu-id="8880d-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8880d-127">-Tags</span><span class="sxs-lookup"><span data-stu-id="8880d-127">-Tags</span></span>
<span data-ttu-id="8880d-128">Marcas do cluster</span><span class="sxs-lookup"><span data-stu-id="8880d-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8880d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8880d-129">-Confirm</span></span>
<span data-ttu-id="8880d-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8880d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8880d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8880d-131">-WhatIf</span></span>
<span data-ttu-id="8880d-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8880d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8880d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8880d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8880d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8880d-134">CommonParameters</span></span>
<span data-ttu-id="8880d-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8880d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8880d-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8880d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8880d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8880d-137">INPUTS</span></span>

### <span data-ttu-id="8880d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8880d-138">System.String</span></span>

## <span data-ttu-id="8880d-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8880d-139">OUTPUTS</span></span>

### <span data-ttu-id="8880d-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="8880d-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="8880d-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="8880d-141">NOTES</span></span>

## <span data-ttu-id="8880d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8880d-142">RELATED LINKS</span></span>
