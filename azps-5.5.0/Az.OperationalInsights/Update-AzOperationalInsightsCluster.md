---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114586"
---
# <span data-ttu-id="4cc82-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="4cc82-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="4cc82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cc82-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc82-103">atualizar cluster</span><span class="sxs-lookup"><span data-stu-id="4cc82-103">update cluster</span></span>

## <span data-ttu-id="4cc82-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cc82-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc82-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cc82-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc82-106">atualizar cluster</span><span class="sxs-lookup"><span data-stu-id="4cc82-106">update cluster</span></span>

## <span data-ttu-id="4cc82-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4cc82-107">EXAMPLES</span></span>

### <span data-ttu-id="4cc82-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4cc82-108">Example 1</span></span>
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

<span data-ttu-id="4cc82-109">atualizar cluster com propriedades do cofre de chave e sku</span><span class="sxs-lookup"><span data-stu-id="4cc82-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="4cc82-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cc82-110">PARAMETERS</span></span>

### <span data-ttu-id="4cc82-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cc82-111">-AsJob</span></span>
<span data-ttu-id="4cc82-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4cc82-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cc82-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4cc82-113">-ClusterName</span></span>
<span data-ttu-id="4cc82-114">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="4cc82-114">The cluster name.</span></span>

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

### <span data-ttu-id="4cc82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc82-115">-DefaultProfile</span></span>
<span data-ttu-id="4cc82-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cc82-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4cc82-117">-KeyName</span></span>
<span data-ttu-id="4cc82-118">Nome da Chave</span><span class="sxs-lookup"><span data-stu-id="4cc82-118">Key Name</span></span>

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

### <span data-ttu-id="4cc82-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="4cc82-119">-KeyVaultUri</span></span>
<span data-ttu-id="4cc82-120">O Uri do Cofre de Teclas, "Proteção contra Limpeza" e "Exclusão Suave" devem ser habilitados para este keyvault</span><span class="sxs-lookup"><span data-stu-id="4cc82-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="4cc82-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="4cc82-121">-KeyVersion</span></span>
<span data-ttu-id="4cc82-122">Versão da chave</span><span class="sxs-lookup"><span data-stu-id="4cc82-122">Key Version</span></span>

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

### <span data-ttu-id="4cc82-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc82-123">-ResourceGroupName</span></span>
<span data-ttu-id="4cc82-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4cc82-124">The resource group name.</span></span>

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

### <span data-ttu-id="4cc82-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4cc82-125">-SkuCapacity</span></span>
<span data-ttu-id="4cc82-126">Capacidade da SKU</span><span class="sxs-lookup"><span data-stu-id="4cc82-126">Sku Capacity</span></span>

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

### <span data-ttu-id="4cc82-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4cc82-127">-SkuName</span></span>
<span data-ttu-id="4cc82-128">Nome SKU, agora pode ser somente 'CapacityReservation'</span><span class="sxs-lookup"><span data-stu-id="4cc82-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="4cc82-129">-Marcas</span><span class="sxs-lookup"><span data-stu-id="4cc82-129">-Tags</span></span>
<span data-ttu-id="4cc82-130">Marcas do cluster</span><span class="sxs-lookup"><span data-stu-id="4cc82-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="4cc82-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4cc82-131">-Confirm</span></span>
<span data-ttu-id="4cc82-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cc82-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc82-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc82-133">-WhatIf</span></span>
<span data-ttu-id="4cc82-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4cc82-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc82-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cc82-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc82-136">CommonParameters</span></span>
<span data-ttu-id="4cc82-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc82-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cc82-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc82-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="4cc82-139">INPUTS</span></span>

### <span data-ttu-id="4cc82-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4cc82-140">System.String</span></span>

## <span data-ttu-id="4cc82-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="4cc82-141">OUTPUTS</span></span>

### <span data-ttu-id="4cc82-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="4cc82-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="4cc82-143">Notas</span><span class="sxs-lookup"><span data-stu-id="4cc82-143">NOTES</span></span>

## <span data-ttu-id="4cc82-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cc82-144">RELATED LINKS</span></span>
