---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: 8dea2e61d6d64fbb59363d157dc0b8c1096ba259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602722"
---
# <span data-ttu-id="c8ab4-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="c8ab4-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="c8ab4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ab4-103">Obtém definições métricas.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8ab4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8ab4-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8ab4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8ab4-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ab4-106">O cmdlet **Get-AzureRmMetricDefinition** Obtém definições métricas.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="c8ab4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8ab4-107">EXAMPLES</span></span>

### <span data-ttu-id="c8ab4-108">Exemplo 1: obter definições de métrica para um recurso</span><span class="sxs-lookup"><span data-stu-id="c8ab4-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="c8ab4-109">Este comando obtém as definições de métricas do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="c8ab4-110">Exemplo 2: obter definições de métrica com saída detalhada</span><span class="sxs-lookup"><span data-stu-id="c8ab4-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="c8ab4-111">Esse comando obtém as definições de métrica para website2.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="c8ab4-112">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-112">The output is detailed.</span></span>

### <span data-ttu-id="c8ab4-113">Exemplo 3: obter definições métricas por nome</span><span class="sxs-lookup"><span data-stu-id="c8ab4-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="c8ab4-114">Este comando obtém definições para as métricas BytesSent e CpuTime.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="c8ab4-115">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-115">The output is detailed.</span></span>

## <span data-ttu-id="c8ab4-116">OS</span><span class="sxs-lookup"><span data-stu-id="c8ab4-116">PARAMETERS</span></span>

### <span data-ttu-id="c8ab4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ab4-117">-DefaultProfile</span></span>
<span data-ttu-id="c8ab4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c8ab4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8ab4-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="c8ab4-119">-DetailedOutput</span></span>
<span data-ttu-id="c8ab4-120">Indica que esta operação incluiu uma saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="c8ab4-121">Se você não especificar esse parâmetro, a saída será resumida.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="c8ab4-122">-Metricname</span><span class="sxs-lookup"><span data-stu-id="c8ab4-122">-MetricName</span></span>
<span data-ttu-id="c8ab4-123">Especifica uma matriz de nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="c8ab4-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="c8ab4-124">-MetricNamespace</span></span>
<span data-ttu-id="c8ab4-125">Especifica o namespace de métrica para consulta de definições de métrica.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8ab4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8ab4-126">-ResourceId</span></span>
<span data-ttu-id="c8ab4-127">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="c8ab4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ab4-128">CommonParameters</span></span>
<span data-ttu-id="c8ab4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8ab4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ab4-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8ab4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ab4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8ab4-131">INPUTS</span></span>

### <span data-ttu-id="c8ab4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c8ab4-132">System.String</span></span>

### <span data-ttu-id="c8ab4-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="c8ab4-133">System.String[]</span></span>

## <span data-ttu-id="c8ab4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8ab4-134">OUTPUTS</span></span>

### <span data-ttu-id="c8ab4-135">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="c8ab4-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="c8ab4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8ab4-136">NOTES</span></span>

## <span data-ttu-id="c8ab4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8ab4-137">RELATED LINKS</span></span>

<span data-ttu-id="c8ab4-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="c8ab4-138">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


