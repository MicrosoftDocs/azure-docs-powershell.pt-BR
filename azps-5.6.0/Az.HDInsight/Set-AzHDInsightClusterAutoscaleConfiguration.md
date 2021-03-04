---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1919c773eb51f5e2d57333f42cbcc0793d4dad63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891844"
---
# <span data-ttu-id="7ca75-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ca75-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="7ca75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ca75-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca75-103">Define a configuração de escala automática de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca75-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7ca75-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ca75-104">SYNTAX</span></span>

### <span data-ttu-id="7ca75-105">LoadAutoscaleByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7ca75-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca75-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca75-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca75-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca75-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca75-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca75-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ca75-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca75-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca75-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca75-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca75-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca75-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca75-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca75-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca75-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca75-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ca75-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ca75-114">DESCRIPTION</span></span>
<span data-ttu-id="7ca75-115">Este cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** define a configuração de escala automática de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca75-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7ca75-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ca75-116">EXAMPLES</span></span>

### <span data-ttu-id="7ca75-117">Exemplo 1: definir a configuração de escala automática baseada em carga do cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ca75-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="7ca75-118">Este comando define a configuração de escala automática baseada em carga de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca75-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="7ca75-119">Exemplo 2: definir a escala automática baseada em Cronograma do cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="7ca75-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="7ca75-120">Este comando define a configuração de escala automática baseada em Agenda do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7ca75-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="7ca75-121">Exemplo 3: definir a configuração de escala automática do cluster HDInsight com base em outro cluster que tenha definido a configuração de escala automática</span><span class="sxs-lookup"><span data-stu-id="7ca75-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="7ca75-122">Este comando define a configuração de escala automática do cluster HDInsight com base em outro cluster.</span><span class="sxs-lookup"><span data-stu-id="7ca75-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="7ca75-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ca75-123">PARAMETERS</span></span>

### <span data-ttu-id="7ca75-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ca75-124">-AsJob</span></span>
<span data-ttu-id="7ca75-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7ca75-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ca75-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ca75-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="7ca75-127">Obtém ou define a configuração de escala automática</span><span class="sxs-lookup"><span data-stu-id="7ca75-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7ca75-128">-ClusterName</span></span>
<span data-ttu-id="7ca75-129">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="7ca75-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-130">-Condition</span><span class="sxs-lookup"><span data-stu-id="7ca75-130">-Condition</span></span>
<span data-ttu-id="7ca75-131">Obtém ou define a condição de escala automática baseada em agendamento.</span><span class="sxs-lookup"><span data-stu-id="7ca75-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca75-132">-DefaultProfile</span></span>
<span data-ttu-id="7ca75-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca75-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca75-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ca75-134">-InputObject</span></span>
<span data-ttu-id="7ca75-135">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="7ca75-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="7ca75-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="7ca75-137">Obtém ou define a contagem máxima de workernode da escala automática baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="7ca75-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="7ca75-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="7ca75-139">Obtém ou define a contagem mínima de workernode da escala automática baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="7ca75-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca75-140">-ResourceGroupName</span></span>
<span data-ttu-id="7ca75-141">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ca75-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ca75-142">-ResourceId</span></span>
<span data-ttu-id="7ca75-143">Obtém ou define a id do recurso.</span><span class="sxs-lookup"><span data-stu-id="7ca75-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-144">-Schedule</span><span class="sxs-lookup"><span data-stu-id="7ca75-144">-Schedule</span></span>
<span data-ttu-id="7ca75-145">Definir parâmetros baseados em cronograma</span><span class="sxs-lookup"><span data-stu-id="7ca75-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="7ca75-146">-TimeZone</span></span>
<span data-ttu-id="7ca75-147">Obtém ou define o fuso horário da escala automática baseada em agendamento.</span><span class="sxs-lookup"><span data-stu-id="7ca75-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca75-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ca75-148">-Confirm</span></span>
<span data-ttu-id="7ca75-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ca75-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca75-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca75-150">-WhatIf</span></span>
<span data-ttu-id="7ca75-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ca75-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ca75-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ca75-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca75-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca75-153">CommonParameters</span></span>
<span data-ttu-id="7ca75-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ca75-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca75-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ca75-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca75-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ca75-156">INPUTS</span></span>

### <span data-ttu-id="7ca75-157">System.String</span><span class="sxs-lookup"><span data-stu-id="7ca75-157">System.String</span></span>

### <span data-ttu-id="7ca75-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7ca75-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="7ca75-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ca75-159">OUTPUTS</span></span>

### <span data-ttu-id="7ca75-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="7ca75-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="7ca75-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ca75-161">NOTES</span></span>

## <span data-ttu-id="7ca75-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ca75-162">RELATED LINKS</span></span>

<span data-ttu-id="7ca75-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ca75-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
