---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: c2fcc4112bb2fb62b73531bd6bd580ba3bcd7648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892781"
---
# <span data-ttu-id="3ba9b-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="3ba9b-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="3ba9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ba9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba9b-103">Cria a condição de escala automática baseada em agendamento.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="3ba9b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ba9b-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ba9b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ba9b-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba9b-106">O cmdlet **New-AzHDInsightClusterAutoscaleScheduleCondition** cria a condição de escala automática baseada em agendamento.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="3ba9b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ba9b-107">EXAMPLES</span></span>

### <span data-ttu-id="3ba9b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ba9b-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="3ba9b-109">Este comando cria uma condição em que o cluster escala automaticamente para 5 nós de trabalho às 09:00 todas as segundas-feiras, quarta-feiras.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="3ba9b-110">Exemplo 2: Habilitar a escala automática baseada em cronograma de um cluster com condição de escala automática.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="3ba9b-111">Este comando cria uma condição em que o cluster escala automaticamente para 5 nós de trabalho às 09:00 todas as segundas-feiras, quarta-feiras.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="3ba9b-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ba9b-112">PARAMETERS</span></span>

### <span data-ttu-id="3ba9b-113">-Day</span><span class="sxs-lookup"><span data-stu-id="3ba9b-113">-Day</span></span>
<span data-ttu-id="3ba9b-114">Obtém ou define os dias da condição de agendamento de escala automática.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba9b-115">-DefaultProfile</span></span>
<span data-ttu-id="3ba9b-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ba9b-117">-Time</span><span class="sxs-lookup"><span data-stu-id="3ba9b-117">-Time</span></span>
<span data-ttu-id="3ba9b-118">Obtém ou define a hora da condição de agendamento de escala automática.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba9b-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="3ba9b-119">-WorkerNodeCount</span></span>
<span data-ttu-id="3ba9b-120">Obtém ou define a contagem de escala de trabalho agendada da condição de agendamento de escala automática.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba9b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba9b-121">CommonParameters</span></span>
<span data-ttu-id="3ba9b-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ba9b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba9b-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ba9b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba9b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ba9b-124">INPUTS</span></span>

### <span data-ttu-id="3ba9b-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3ba9b-125">None</span></span>

## <span data-ttu-id="3ba9b-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ba9b-126">OUTPUTS</span></span>

### <span data-ttu-id="3ba9b-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="3ba9b-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="3ba9b-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ba9b-128">NOTES</span></span>

## <span data-ttu-id="3ba9b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ba9b-129">RELATED LINKS</span></span>

<span data-ttu-id="3ba9b-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3ba9b-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
