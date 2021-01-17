---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426860"
---
# <span data-ttu-id="9afc8-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="9afc8-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="9afc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9afc8-102">SYNOPSIS</span></span>
<span data-ttu-id="9afc8-103">Cria uma condição de autoescala baseada em cronograma.</span><span class="sxs-lookup"><span data-stu-id="9afc8-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="9afc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9afc8-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9afc8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9afc8-105">DESCRIPTION</span></span>
<span data-ttu-id="9afc8-106">O cmdlet **New-AzHDInsightClusterAutoscaleScheduleCondition** cria uma condição de autoescala baseada em cronograma.</span><span class="sxs-lookup"><span data-stu-id="9afc8-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="9afc8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9afc8-107">EXAMPLES</span></span>

### <span data-ttu-id="9afc8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9afc8-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="9afc8-109">Esse comando cria uma condição em que o dimensionamento automático do cluster é de 5 nós de trabalho em 09:00 a cada segunda-feira, quarta-feira.</span><span class="sxs-lookup"><span data-stu-id="9afc8-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="9afc8-110">Exemplo 2: habilitar a escala automática baseada em cronograma de um cluster com uma condição de autoescala.</span><span class="sxs-lookup"><span data-stu-id="9afc8-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="9afc8-111">Esse comando cria uma condição em que o dimensionamento automático do cluster é de 5 nós de trabalho em 09:00 a cada segunda-feira, quarta-feira.</span><span class="sxs-lookup"><span data-stu-id="9afc8-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="9afc8-112">OS</span><span class="sxs-lookup"><span data-stu-id="9afc8-112">PARAMETERS</span></span>

### <span data-ttu-id="9afc8-113">-Dia</span><span class="sxs-lookup"><span data-stu-id="9afc8-113">-Day</span></span>
<span data-ttu-id="9afc8-114">Obtém ou define os dias de condição de agendamento de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="9afc8-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="9afc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9afc8-115">-DefaultProfile</span></span>
<span data-ttu-id="9afc8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9afc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9afc8-117">-Time</span><span class="sxs-lookup"><span data-stu-id="9afc8-117">-Time</span></span>
<span data-ttu-id="9afc8-118">Obtém ou define a hora da condição de agendamento de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="9afc8-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="9afc8-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="9afc8-119">-WorkerNodeCount</span></span>
<span data-ttu-id="9afc8-120">Obtém ou define a contagem de agendamento do agendamento de autodimensionamento workernode.</span><span class="sxs-lookup"><span data-stu-id="9afc8-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="9afc8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9afc8-121">CommonParameters</span></span>
<span data-ttu-id="9afc8-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9afc8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9afc8-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9afc8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9afc8-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9afc8-124">INPUTS</span></span>

### <span data-ttu-id="9afc8-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9afc8-125">None</span></span>

## <span data-ttu-id="9afc8-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9afc8-126">OUTPUTS</span></span>

### <span data-ttu-id="9afc8-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="9afc8-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="9afc8-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9afc8-128">NOTES</span></span>

## <span data-ttu-id="9afc8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9afc8-129">RELATED LINKS</span></span>

<span data-ttu-id="9afc8-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9afc8-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
