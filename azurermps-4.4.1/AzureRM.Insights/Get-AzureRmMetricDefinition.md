---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: 4cb978b33b6bcb68d400f33fb2da06747ce9b763
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609671"
---
# <span data-ttu-id="8b98b-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="8b98b-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="8b98b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b98b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b98b-103">Obtém definições métricas.</span><span class="sxs-lookup"><span data-stu-id="8b98b-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b98b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b98b-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b98b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b98b-105">DESCRIPTION</span></span>
<span data-ttu-id="8b98b-106">O cmdlet **Get-AzureRmMetricDefinition** Obtém definições métricas.</span><span class="sxs-lookup"><span data-stu-id="8b98b-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="8b98b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b98b-107">EXAMPLES</span></span>

### <span data-ttu-id="8b98b-108">Exemplo 1: obter definições de métrica para um recurso</span><span class="sxs-lookup"><span data-stu-id="8b98b-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="8b98b-109">Este comando obtém as definições de métricas do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="8b98b-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="8b98b-110">Exemplo 2: obter definições de métrica com saída detalhada</span><span class="sxs-lookup"><span data-stu-id="8b98b-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="8b98b-111">Esse comando obtém as definições de métrica para website2.</span><span class="sxs-lookup"><span data-stu-id="8b98b-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="8b98b-112">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="8b98b-112">The output is detailed.</span></span>

### <span data-ttu-id="8b98b-113">Exemplo 3: obter definições métricas por nome</span><span class="sxs-lookup"><span data-stu-id="8b98b-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="8b98b-114">Este comando obtém definições para as métricas BytesSent e CpuTime.</span><span class="sxs-lookup"><span data-stu-id="8b98b-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="8b98b-115">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="8b98b-115">The output is detailed.</span></span>

## <span data-ttu-id="8b98b-116">OS</span><span class="sxs-lookup"><span data-stu-id="8b98b-116">PARAMETERS</span></span>

### <span data-ttu-id="8b98b-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="8b98b-117">-DetailedOutput</span></span>
<span data-ttu-id="8b98b-118">Indica que esta operação incluiu uma saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="8b98b-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="8b98b-119">Se você não especificar esse parâmetro, a saída será resumida.</span><span class="sxs-lookup"><span data-stu-id="8b98b-119">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b98b-120">-Metricnames</span><span class="sxs-lookup"><span data-stu-id="8b98b-120">-MetricNames</span></span>
<span data-ttu-id="8b98b-121">Especifica uma matriz de nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="8b98b-121">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b98b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b98b-122">-ResourceId</span></span>
<span data-ttu-id="8b98b-123">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8b98b-123">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b98b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b98b-124">-DefaultProfile</span></span>
<span data-ttu-id="8b98b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b98b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b98b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b98b-126">CommonParameters</span></span>
<span data-ttu-id="8b98b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b98b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b98b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b98b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b98b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b98b-129">INPUTS</span></span>

## <span data-ttu-id="8b98b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b98b-130">OUTPUTS</span></span>

### <span data-ttu-id="8b98b-131">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricDefinition []</span><span class="sxs-lookup"><span data-stu-id="8b98b-131">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="8b98b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b98b-132">NOTES</span></span>

## <span data-ttu-id="8b98b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b98b-133">RELATED LINKS</span></span>

[<span data-ttu-id="8b98b-134">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="8b98b-134">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


