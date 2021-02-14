---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116785"
---
# <span data-ttu-id="67ffe-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="67ffe-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="67ffe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="67ffe-103">Cria uma condição de escala automática baseada em cronograma.</span><span class="sxs-lookup"><span data-stu-id="67ffe-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="67ffe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67ffe-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67ffe-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="67ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="67ffe-106">O cmdlet **New-AzHDInsightClusterAutoscaleScheduleCondition** cria uma condição de escala automática baseada em Cronograma.</span><span class="sxs-lookup"><span data-stu-id="67ffe-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="67ffe-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="67ffe-107">EXAMPLES</span></span>

### <span data-ttu-id="67ffe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67ffe-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="67ffe-109">Esse comando cria uma condição em que o cluster escala automaticamente para 5 nós de trabalhadores às 09:00 todas as segundas-feiras, quartas-feiras.</span><span class="sxs-lookup"><span data-stu-id="67ffe-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="67ffe-110">Exemplo 2: Habilitar a escala automática baseada em agenda de um cluster com condição de escala automática.</span><span class="sxs-lookup"><span data-stu-id="67ffe-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="67ffe-111">Esse comando cria uma condição em que o cluster escala automaticamente para 5 nós de trabalhadores às 09:00 todas as segundas-feiras, quartas-feiras.</span><span class="sxs-lookup"><span data-stu-id="67ffe-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="67ffe-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67ffe-112">PARAMETERS</span></span>

### <span data-ttu-id="67ffe-113">-Dia</span><span class="sxs-lookup"><span data-stu-id="67ffe-113">-Day</span></span>
<span data-ttu-id="67ffe-114">Obtém ou define os dias da condição de agendamento em Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="67ffe-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="67ffe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ffe-115">-DefaultProfile</span></span>
<span data-ttu-id="67ffe-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67ffe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ffe-117">-Hora</span><span class="sxs-lookup"><span data-stu-id="67ffe-117">-Time</span></span>
<span data-ttu-id="67ffe-118">Obtém ou define o horário da condição de agendamento em Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="67ffe-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="67ffe-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="67ffe-119">-WorkerNodeCount</span></span>
<span data-ttu-id="67ffe-120">Obtém ou define a contagem de escala de trabalho agendada da condição de agendamento de escala automática.</span><span class="sxs-lookup"><span data-stu-id="67ffe-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="67ffe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ffe-121">CommonParameters</span></span>
<span data-ttu-id="67ffe-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ffe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ffe-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67ffe-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ffe-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="67ffe-124">INPUTS</span></span>

### <span data-ttu-id="67ffe-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="67ffe-125">None</span></span>

## <span data-ttu-id="67ffe-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="67ffe-126">OUTPUTS</span></span>

### <span data-ttu-id="67ffe-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="67ffe-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="67ffe-128">Notas</span><span class="sxs-lookup"><span data-stu-id="67ffe-128">NOTES</span></span>

## <span data-ttu-id="67ffe-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67ffe-129">RELATED LINKS</span></span>

<span data-ttu-id="67ffe-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="67ffe-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
