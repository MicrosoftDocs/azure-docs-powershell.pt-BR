---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111864"
---
# <span data-ttu-id="c8a31-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8a31-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="c8a31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8a31-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a31-103">Cria um objeto não persistente que descreve a configuração de escala automática de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a31-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c8a31-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8a31-104">SYNTAX</span></span>

### <span data-ttu-id="c8a31-105">LoadAutoscaleParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8a31-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8a31-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a31-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8a31-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8a31-107">DESCRIPTION</span></span>
<span data-ttu-id="c8a31-108">O cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** cria um objeto não persistente que descreve a configuração de escala automática de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a31-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c8a31-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8a31-109">EXAMPLES</span></span>

### <span data-ttu-id="c8a31-110">Exemplo 1: Criar um objeto que descreva a configuração de escala automática baseada em carga</span><span class="sxs-lookup"><span data-stu-id="c8a31-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="c8a31-111">Esse comando cria um objeto que descreve a configuração de escala automática baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="c8a31-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="c8a31-112">Exemplo 2: Criar um objeto que descreva a configuração de escala automática baseada em agenda</span><span class="sxs-lookup"><span data-stu-id="c8a31-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="c8a31-113">Esse comando cria um objeto que descreve a configuração de escala automática baseada em Agenda.</span><span class="sxs-lookup"><span data-stu-id="c8a31-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="c8a31-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8a31-114">PARAMETERS</span></span>

### <span data-ttu-id="c8a31-115">-Condição</span><span class="sxs-lookup"><span data-stu-id="c8a31-115">-Condition</span></span>
<span data-ttu-id="c8a31-116">Obtém ou define a condição de escala automática baseada em cronograma.</span><span class="sxs-lookup"><span data-stu-id="c8a31-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a31-117">-DefaultProfile</span></span>
<span data-ttu-id="c8a31-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a31-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="c8a31-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="c8a31-120">Obtém ou define a contagem máxima de escala automática baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="c8a31-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a31-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="c8a31-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="c8a31-122">Obtém ou define a contagem mínima de escala automática baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="c8a31-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a31-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="c8a31-123">-TimeZone</span></span>
<span data-ttu-id="c8a31-124">Obtém ou define o fuso horário da escala automática baseada em cronograma.</span><span class="sxs-lookup"><span data-stu-id="c8a31-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a31-125">CommonParameters</span></span>
<span data-ttu-id="c8a31-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a31-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8a31-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a31-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8a31-128">INPUTS</span></span>

### <span data-ttu-id="c8a31-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c8a31-129">None</span></span>

## <span data-ttu-id="c8a31-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8a31-130">OUTPUTS</span></span>

### <span data-ttu-id="c8a31-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="c8a31-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="c8a31-132">Notas</span><span class="sxs-lookup"><span data-stu-id="c8a31-132">NOTES</span></span>

## <span data-ttu-id="c8a31-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8a31-133">RELATED LINKS</span></span>

<span data-ttu-id="c8a31-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c8a31-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
