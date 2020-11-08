---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117571"
---
# <span data-ttu-id="291a7-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="291a7-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="291a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="291a7-102">SYNOPSIS</span></span>
<span data-ttu-id="291a7-103">atualizar cluster</span><span class="sxs-lookup"><span data-stu-id="291a7-103">update cluster</span></span>

## <span data-ttu-id="291a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="291a7-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="291a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="291a7-105">DESCRIPTION</span></span>
<span data-ttu-id="291a7-106">atualizar cluster</span><span class="sxs-lookup"><span data-stu-id="291a7-106">update cluster</span></span>

## <span data-ttu-id="291a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="291a7-107">EXAMPLES</span></span>

### <span data-ttu-id="291a7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="291a7-108">Example 1</span></span>
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

<span data-ttu-id="291a7-109">atualizar cluster com propriedades e SKU do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="291a7-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="291a7-110">OS</span><span class="sxs-lookup"><span data-stu-id="291a7-110">PARAMETERS</span></span>

### <span data-ttu-id="291a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="291a7-111">-AsJob</span></span>
<span data-ttu-id="291a7-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="291a7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="291a7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="291a7-113">-ClusterName</span></span>
<span data-ttu-id="291a7-114">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="291a7-114">The cluster name.</span></span>

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

### <span data-ttu-id="291a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="291a7-115">-DefaultProfile</span></span>
<span data-ttu-id="291a7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="291a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="291a7-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="291a7-117">-KeyName</span></span>
<span data-ttu-id="291a7-118">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="291a7-118">Key Name</span></span>

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

### <span data-ttu-id="291a7-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="291a7-119">-KeyVaultUri</span></span>
<span data-ttu-id="291a7-120">O URI do cofre de chaves, "remover proteção" e "exclusão reversível" precisa estar habilitado para este keyvault</span><span class="sxs-lookup"><span data-stu-id="291a7-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="291a7-121">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="291a7-121">-KeyVersion</span></span>
<span data-ttu-id="291a7-122">Versão de chave</span><span class="sxs-lookup"><span data-stu-id="291a7-122">Key Version</span></span>

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

### <span data-ttu-id="291a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="291a7-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="291a7-124">The resource group name.</span></span>

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

### <span data-ttu-id="291a7-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="291a7-125">-SkuCapacity</span></span>
<span data-ttu-id="291a7-126">Capacidade do SKU</span><span class="sxs-lookup"><span data-stu-id="291a7-126">Sku Capacity</span></span>

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

### <span data-ttu-id="291a7-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="291a7-127">-SkuName</span></span>
<span data-ttu-id="291a7-128">O nome do SKU agora pode ser ' CapacityReservation ' apenas</span><span class="sxs-lookup"><span data-stu-id="291a7-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="291a7-129">-Marcas</span><span class="sxs-lookup"><span data-stu-id="291a7-129">-Tags</span></span>
<span data-ttu-id="291a7-130">Marcas do cluster</span><span class="sxs-lookup"><span data-stu-id="291a7-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="291a7-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="291a7-131">-Confirm</span></span>
<span data-ttu-id="291a7-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="291a7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="291a7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="291a7-133">-WhatIf</span></span>
<span data-ttu-id="291a7-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="291a7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="291a7-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="291a7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="291a7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291a7-136">CommonParameters</span></span>
<span data-ttu-id="291a7-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="291a7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291a7-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="291a7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291a7-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="291a7-139">INPUTS</span></span>

### <span data-ttu-id="291a7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="291a7-140">System.String</span></span>

## <span data-ttu-id="291a7-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="291a7-141">OUTPUTS</span></span>

### <span data-ttu-id="291a7-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="291a7-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="291a7-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="291a7-143">NOTES</span></span>

## <span data-ttu-id="291a7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="291a7-144">RELATED LINKS</span></span>
