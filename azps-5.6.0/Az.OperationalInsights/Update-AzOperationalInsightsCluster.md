---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: f76ca0db3f4203bf1906c29c32c1973ea098789c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890183"
---
# <span data-ttu-id="fcaba-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="fcaba-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="fcaba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcaba-102">SYNOPSIS</span></span>
<span data-ttu-id="fcaba-103">cluster de atualização</span><span class="sxs-lookup"><span data-stu-id="fcaba-103">update cluster</span></span>

## <span data-ttu-id="fcaba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fcaba-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcaba-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fcaba-105">DESCRIPTION</span></span>
<span data-ttu-id="fcaba-106">cluster de atualização</span><span class="sxs-lookup"><span data-stu-id="fcaba-106">update cluster</span></span>

## <span data-ttu-id="fcaba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcaba-107">EXAMPLES</span></span>

### <span data-ttu-id="fcaba-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fcaba-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="fcaba-109">atualizar cluster com as principais propriedades do cofre e sku</span><span class="sxs-lookup"><span data-stu-id="fcaba-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="fcaba-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fcaba-110">PARAMETERS</span></span>

### <span data-ttu-id="fcaba-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcaba-111">-AsJob</span></span>
<span data-ttu-id="fcaba-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fcaba-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fcaba-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fcaba-113">-ClusterName</span></span>
<span data-ttu-id="fcaba-114">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="fcaba-114">The cluster name.</span></span>

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

### <span data-ttu-id="fcaba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcaba-115">-DefaultProfile</span></span>
<span data-ttu-id="fcaba-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcaba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcaba-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fcaba-117">-KeyName</span></span>
<span data-ttu-id="fcaba-118">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="fcaba-118">Key Name</span></span>

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

### <span data-ttu-id="fcaba-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="fcaba-119">-KeyVaultUri</span></span>
<span data-ttu-id="fcaba-120">Key Vault Uri, "Purge Protection" e "Soft Delete" devem ser habilitados para este keyvault</span><span class="sxs-lookup"><span data-stu-id="fcaba-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="fcaba-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="fcaba-121">-KeyVersion</span></span>
<span data-ttu-id="fcaba-122">Versão chave</span><span class="sxs-lookup"><span data-stu-id="fcaba-122">Key Version</span></span>

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

### <span data-ttu-id="fcaba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcaba-123">-ResourceGroupName</span></span>
<span data-ttu-id="fcaba-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcaba-124">The resource group name.</span></span>

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

### <span data-ttu-id="fcaba-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fcaba-125">-SkuCapacity</span></span>
<span data-ttu-id="fcaba-126">Capacidade Sku</span><span class="sxs-lookup"><span data-stu-id="fcaba-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcaba-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fcaba-127">-SkuName</span></span>
<span data-ttu-id="fcaba-128">Nome Sku, agora pode ser somente 'CapacityReservation'</span><span class="sxs-lookup"><span data-stu-id="fcaba-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="fcaba-129">-Tags</span><span class="sxs-lookup"><span data-stu-id="fcaba-129">-Tags</span></span>
<span data-ttu-id="fcaba-130">Marcas do cluster</span><span class="sxs-lookup"><span data-stu-id="fcaba-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="fcaba-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcaba-131">-Confirm</span></span>
<span data-ttu-id="fcaba-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcaba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcaba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcaba-133">-WhatIf</span></span>
<span data-ttu-id="fcaba-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcaba-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcaba-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcaba-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcaba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcaba-136">CommonParameters</span></span>
<span data-ttu-id="fcaba-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcaba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcaba-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcaba-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcaba-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcaba-139">INPUTS</span></span>

### <span data-ttu-id="fcaba-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fcaba-140">System.String</span></span>

## <span data-ttu-id="fcaba-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fcaba-141">OUTPUTS</span></span>

### <span data-ttu-id="fcaba-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="fcaba-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="fcaba-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="fcaba-143">NOTES</span></span>

## <span data-ttu-id="fcaba-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcaba-144">RELATED LINKS</span></span>
