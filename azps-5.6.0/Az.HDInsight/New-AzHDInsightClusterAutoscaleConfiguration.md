---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bfc14e0fba2b384766495dde9e3ef11fafd4653c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892782"
---
# <span data-ttu-id="9af8b-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9af8b-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="9af8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af8b-102">SYNOPSIS</span></span>
<span data-ttu-id="9af8b-103">Cria um objeto não persistente que descreve a configuração de escala automática de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="9af8b-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9af8b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9af8b-104">SYNTAX</span></span>

### <span data-ttu-id="9af8b-105">LoadAutoscaleParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9af8b-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af8b-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="9af8b-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9af8b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9af8b-107">DESCRIPTION</span></span>
<span data-ttu-id="9af8b-108">O cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** cria um objeto não persistente que descreve a configuração de escala automática de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="9af8b-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9af8b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9af8b-109">EXAMPLES</span></span>

### <span data-ttu-id="9af8b-110">Exemplo 1: Criar um objeto que descreve a configuração de escala automática baseada em carga</span><span class="sxs-lookup"><span data-stu-id="9af8b-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="9af8b-111">Este comando cria um objeto que descreve a configuração de escala automática baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="9af8b-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="9af8b-112">Exemplo 2: Criar um objeto que descreve a configuração de escala automática baseada em agendamento</span><span class="sxs-lookup"><span data-stu-id="9af8b-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="9af8b-113">Este comando cria um objeto que descreve a configuração de escala automática baseada em agendamento.</span><span class="sxs-lookup"><span data-stu-id="9af8b-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="9af8b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9af8b-114">PARAMETERS</span></span>

### <span data-ttu-id="9af8b-115">-Condition</span><span class="sxs-lookup"><span data-stu-id="9af8b-115">-Condition</span></span>
<span data-ttu-id="9af8b-116">Obtém ou define a condição de escala automática baseada em agendamento.</span><span class="sxs-lookup"><span data-stu-id="9af8b-116">Gets or sets the condition of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="9af8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af8b-117">-DefaultProfile</span></span>
<span data-ttu-id="9af8b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9af8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9af8b-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="9af8b-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="9af8b-120">Obtém ou define a contagem máxima de workernode da escala automática baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="9af8b-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="9af8b-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="9af8b-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="9af8b-122">Obtém ou define a contagem mínima de workernode da escala automática baseada em carga.</span><span class="sxs-lookup"><span data-stu-id="9af8b-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="9af8b-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="9af8b-123">-TimeZone</span></span>
<span data-ttu-id="9af8b-124">Obtém ou define o fuso horário da escala automática baseada em agendamento.</span><span class="sxs-lookup"><span data-stu-id="9af8b-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="9af8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af8b-125">CommonParameters</span></span>
<span data-ttu-id="9af8b-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af8b-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9af8b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af8b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9af8b-128">INPUTS</span></span>

### <span data-ttu-id="9af8b-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9af8b-129">None</span></span>

## <span data-ttu-id="9af8b-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9af8b-130">OUTPUTS</span></span>

### <span data-ttu-id="9af8b-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="9af8b-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="9af8b-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="9af8b-132">NOTES</span></span>

## <span data-ttu-id="9af8b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9af8b-133">RELATED LINKS</span></span>

<span data-ttu-id="9af8b-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9af8b-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
