---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115364"
---
# <span data-ttu-id="1d0ad-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d0ad-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="1d0ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0ad-103">Cria um objeto não persistente que descreve a configuração de autoescala de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1d0ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d0ad-104">SYNTAX</span></span>

### <span data-ttu-id="1d0ad-105">LoadAutoscaleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d0ad-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d0ad-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d0ad-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d0ad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d0ad-107">DESCRIPTION</span></span>
<span data-ttu-id="1d0ad-108">O cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** cria um objeto não persistente que descreve a configuração de autoescala de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1d0ad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d0ad-109">EXAMPLES</span></span>

### <span data-ttu-id="1d0ad-110">Exemplo 1: criar um objeto que descreva a configuração de autoescala baseada em carga</span><span class="sxs-lookup"><span data-stu-id="1d0ad-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="1d0ad-111">Esse comando cria um objeto que descreve a configuração de autoescala baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="1d0ad-112">Exemplo 2: criar um objeto que descreva a configuração de autoescala baseada em cronograma</span><span class="sxs-lookup"><span data-stu-id="1d0ad-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="1d0ad-113">Esse comando cria um objeto que descreve a configuração de autoescala baseada em cronograma.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="1d0ad-114">OS</span><span class="sxs-lookup"><span data-stu-id="1d0ad-114">PARAMETERS</span></span>

### <span data-ttu-id="1d0ad-115">-Condition</span><span class="sxs-lookup"><span data-stu-id="1d0ad-115">-Condition</span></span>
<span data-ttu-id="1d0ad-116">Obtém ou define a condição de dimensionamento automático baseado em agenda.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-116">Gets or sets the condition of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="1d0ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0ad-117">-DefaultProfile</span></span>
<span data-ttu-id="1d0ad-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d0ad-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="1d0ad-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="1d0ad-120">Obtém ou define a contagem workernode máxima da escalabilidade baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="1d0ad-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="1d0ad-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="1d0ad-122">Obtém ou define a contagem mínima de workernode da escalabilidade baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="1d0ad-123">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="1d0ad-123">-TimeZone</span></span>
<span data-ttu-id="1d0ad-124">Obtém ou define o fuso horário da escalabilidade baseada em cronograma.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="1d0ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0ad-125">CommonParameters</span></span>
<span data-ttu-id="1d0ad-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d0ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0ad-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d0ad-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0ad-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d0ad-128">INPUTS</span></span>

### <span data-ttu-id="1d0ad-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1d0ad-129">None</span></span>

## <span data-ttu-id="1d0ad-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d0ad-130">OUTPUTS</span></span>

### <span data-ttu-id="1d0ad-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="1d0ad-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="1d0ad-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d0ad-132">NOTES</span></span>

## <span data-ttu-id="1d0ad-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d0ad-133">RELATED LINKS</span></span>

<span data-ttu-id="1d0ad-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d0ad-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
