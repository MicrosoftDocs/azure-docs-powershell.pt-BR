---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c18567cac6edbeb55b0f7442b45748bc3d62bc86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888937"
---
# <span data-ttu-id="3ee10-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ee10-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="3ee10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee10-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee10-103">Remove a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3ee10-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="3ee10-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ee10-104">SYNTAX</span></span>

### <span data-ttu-id="3ee10-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ee10-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ee10-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ee10-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ee10-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ee10-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee10-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ee10-108">DESCRIPTION</span></span>
<span data-ttu-id="3ee10-109">O cmdlet **Remove-AzHDInsightClusterAutoscaleConfiguration** remove a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3ee10-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="3ee10-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ee10-110">EXAMPLES</span></span>

### <span data-ttu-id="3ee10-111">Exemplo 1: Remover a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3ee10-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="3ee10-112">Este comando remove a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3ee10-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="3ee10-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ee10-113">PARAMETERS</span></span>

### <span data-ttu-id="3ee10-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ee10-114">-AsJob</span></span>
<span data-ttu-id="3ee10-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3ee10-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee10-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3ee10-116">-ClusterName</span></span>
<span data-ttu-id="3ee10-117">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3ee10-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee10-118">-DefaultProfile</span></span>
<span data-ttu-id="3ee10-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee10-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee10-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ee10-120">-InputObject</span></span>
<span data-ttu-id="3ee10-121">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="3ee10-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee10-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ee10-123">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ee10-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee10-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ee10-124">-ResourceId</span></span>
<span data-ttu-id="3ee10-125">Obtém ou define a id do recurso.</span><span class="sxs-lookup"><span data-stu-id="3ee10-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee10-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ee10-126">-Confirm</span></span>
<span data-ttu-id="3ee10-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ee10-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee10-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee10-128">-WhatIf</span></span>
<span data-ttu-id="3ee10-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ee10-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ee10-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ee10-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee10-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee10-131">CommonParameters</span></span>
<span data-ttu-id="3ee10-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee10-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee10-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ee10-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee10-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ee10-134">INPUTS</span></span>

### <span data-ttu-id="3ee10-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3ee10-135">System.String</span></span>

### <span data-ttu-id="3ee10-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3ee10-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="3ee10-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ee10-137">OUTPUTS</span></span>

### <span data-ttu-id="3ee10-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ee10-138">System.Boolean</span></span>

## <span data-ttu-id="3ee10-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ee10-139">NOTES</span></span>

## <span data-ttu-id="3ee10-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ee10-140">RELATED LINKS</span></span>

<span data-ttu-id="3ee10-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ee10-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
