---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280327"
---
# <span data-ttu-id="9d51b-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d51b-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="9d51b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d51b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d51b-103">Define a configuração de autoescala de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9d51b-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9d51b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d51b-104">SYNTAX</span></span>

### <span data-ttu-id="9d51b-105">LoadAutoscaleByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d51b-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51b-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51b-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51b-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51b-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51b-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51b-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d51b-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51b-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51b-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51b-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51b-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51b-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51b-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51b-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d51b-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d51b-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d51b-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d51b-114">DESCRIPTION</span></span>
<span data-ttu-id="9d51b-115">Este cmdlet **set-AzHDInsightClusterAutoscaleConfiguration** define a configuração de autoescala de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9d51b-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9d51b-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d51b-116">EXAMPLES</span></span>

### <span data-ttu-id="9d51b-117">Exemplo 1: definir a configuração de autoescala baseada em carga do cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="9d51b-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="9d51b-118">Esse comando define a configuração de autoescala baseada em carga de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9d51b-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="9d51b-119">Exemplo 2: definir a escala automática baseada em cronograma do cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="9d51b-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="9d51b-120">Esse comando define a configuração de autoescala baseada em cronograma do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9d51b-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="9d51b-121">Exemplo 3: definir a configuração de autoescala do cluster HDInsight com base em outro cluster que tem a configuração de autoescala definida</span><span class="sxs-lookup"><span data-stu-id="9d51b-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
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

<span data-ttu-id="9d51b-122">Esse comando define a configuração de autoescala do cluster HDInsight com base em outro cluster.</span><span class="sxs-lookup"><span data-stu-id="9d51b-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="9d51b-123">OS</span><span class="sxs-lookup"><span data-stu-id="9d51b-123">PARAMETERS</span></span>

### <span data-ttu-id="9d51b-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d51b-124">-AsJob</span></span>
<span data-ttu-id="9d51b-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9d51b-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d51b-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d51b-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="9d51b-127">Obtém ou define a configuração de dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="9d51b-127">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="9d51b-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9d51b-128">-ClusterName</span></span>
<span data-ttu-id="9d51b-129">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="9d51b-129">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="9d51b-130">-Condition</span><span class="sxs-lookup"><span data-stu-id="9d51b-130">-Condition</span></span>
<span data-ttu-id="9d51b-131">Obtém ou define a condição de dimensionamento automático baseado em agenda.</span><span class="sxs-lookup"><span data-stu-id="9d51b-131">Gets or sets the condition of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="9d51b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d51b-132">-DefaultProfile</span></span>
<span data-ttu-id="9d51b-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d51b-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d51b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d51b-134">-InputObject</span></span>
<span data-ttu-id="9d51b-135">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="9d51b-135">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="9d51b-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="9d51b-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="9d51b-137">Obtém ou define a contagem workernode máxima da escalabilidade baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="9d51b-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="9d51b-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="9d51b-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="9d51b-139">Obtém ou define a contagem mínima de workernode da escalabilidade baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="9d51b-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="9d51b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d51b-140">-ResourceGroupName</span></span>
<span data-ttu-id="9d51b-141">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d51b-141">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="9d51b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d51b-142">-ResourceId</span></span>
<span data-ttu-id="9d51b-143">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9d51b-143">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="9d51b-144">-Cronograma</span><span class="sxs-lookup"><span data-stu-id="9d51b-144">-Schedule</span></span>
<span data-ttu-id="9d51b-145">Definir parâmetros baseados em cronograma</span><span class="sxs-lookup"><span data-stu-id="9d51b-145">Set schedule-based parameters</span></span>

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

### <span data-ttu-id="9d51b-146">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="9d51b-146">-TimeZone</span></span>
<span data-ttu-id="9d51b-147">Obtém ou define o fuso horário da escalabilidade baseada em cronograma.</span><span class="sxs-lookup"><span data-stu-id="9d51b-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="9d51b-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d51b-148">-Confirm</span></span>
<span data-ttu-id="9d51b-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d51b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d51b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d51b-150">-WhatIf</span></span>
<span data-ttu-id="9d51b-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d51b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d51b-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d51b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d51b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d51b-153">CommonParameters</span></span>
<span data-ttu-id="9d51b-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d51b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d51b-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d51b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d51b-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d51b-156">INPUTS</span></span>

### <span data-ttu-id="9d51b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9d51b-157">System.String</span></span>

### <span data-ttu-id="9d51b-158">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9d51b-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="9d51b-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d51b-159">OUTPUTS</span></span>

### <span data-ttu-id="9d51b-160">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="9d51b-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="9d51b-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d51b-161">NOTES</span></span>

## <span data-ttu-id="9d51b-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d51b-162">RELATED LINKS</span></span>

<span data-ttu-id="9d51b-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9d51b-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
