---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113413"
---
# <span data-ttu-id="2e8d2-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="2e8d2-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="2e8d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8d2-103">Criar cluster</span><span class="sxs-lookup"><span data-stu-id="2e8d2-103">Create cluster</span></span>

## <span data-ttu-id="2e8d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e8d2-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e8d2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e8d2-105">DESCRIPTION</span></span>

<span data-ttu-id="2e8d2-106">Criar cluster</span><span class="sxs-lookup"><span data-stu-id="2e8d2-106">Create cluster</span></span>

## <span data-ttu-id="2e8d2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e8d2-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8d2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e8d2-108">Example 1</span></span>
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

<span data-ttu-id="2e8d2-109">Criar cluster</span><span class="sxs-lookup"><span data-stu-id="2e8d2-109">Create cluster</span></span>

## <span data-ttu-id="2e8d2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e8d2-110">PARAMETERS</span></span>

### <span data-ttu-id="2e8d2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e8d2-111">-AsJob</span></span>
<span data-ttu-id="2e8d2-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2e8d2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e8d2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2e8d2-113">-ClusterName</span></span>
<span data-ttu-id="2e8d2-114">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-114">The cluster name.</span></span>

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

### <span data-ttu-id="2e8d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8d2-115">-DefaultProfile</span></span>
<span data-ttu-id="2e8d2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e8d2-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2e8d2-117">-IdentityType</span></span>
<span data-ttu-id="2e8d2-118">o tipo de identidade, o valor pode ser "SystemAssigned", "None".</span><span class="sxs-lookup"><span data-stu-id="2e8d2-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

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

### <span data-ttu-id="2e8d2-119">-Local</span><span class="sxs-lookup"><span data-stu-id="2e8d2-119">-Location</span></span>
<span data-ttu-id="2e8d2-120">A região geográfica em que o cluster será implantado.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-120">The geographic region that the cluster will be deployed.</span></span>

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

### <span data-ttu-id="2e8d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e8d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e8d2-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-122">The resource group name.</span></span>

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

### <span data-ttu-id="2e8d2-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2e8d2-123">-SkuCapacity</span></span>
<span data-ttu-id="2e8d2-124">Capacidade da SKU, o valor precisa ser múltiplo de 100 e no intervalo de 1000 a 2000.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

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

### <span data-ttu-id="2e8d2-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2e8d2-125">-SkuName</span></span>
<span data-ttu-id="2e8d2-126">Nome SKU, agora pode ser somente 'CapacityReservation'</span><span class="sxs-lookup"><span data-stu-id="2e8d2-126">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="2e8d2-127">-Marcas</span><span class="sxs-lookup"><span data-stu-id="2e8d2-127">-Tags</span></span>
<span data-ttu-id="2e8d2-128">Marcas do cluster</span><span class="sxs-lookup"><span data-stu-id="2e8d2-128">Tags of the cluster</span></span>

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

### <span data-ttu-id="2e8d2-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2e8d2-129">-Confirm</span></span>
<span data-ttu-id="2e8d2-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e8d2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e8d2-131">-WhatIf</span></span>
<span data-ttu-id="2e8d2-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e8d2-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e8d2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8d2-134">CommonParameters</span></span>
<span data-ttu-id="2e8d2-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8d2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8d2-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e8d2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8d2-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="2e8d2-137">INPUTS</span></span>

### <span data-ttu-id="2e8d2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2e8d2-138">System.String</span></span>

## <span data-ttu-id="2e8d2-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="2e8d2-139">OUTPUTS</span></span>

### <span data-ttu-id="2e8d2-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="2e8d2-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="2e8d2-141">Notas</span><span class="sxs-lookup"><span data-stu-id="2e8d2-141">NOTES</span></span>

## <span data-ttu-id="2e8d2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e8d2-142">RELATED LINKS</span></span>
