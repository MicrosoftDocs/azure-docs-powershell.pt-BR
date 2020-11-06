---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: de839f4b56f4aa1111e130bdf6396875f9aeb185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430484"
---
# <span data-ttu-id="98ca1-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="98ca1-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="98ca1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="98ca1-103">Obtém definições métricas.</span><span class="sxs-lookup"><span data-stu-id="98ca1-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98ca1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98ca1-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98ca1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98ca1-105">DESCRIPTION</span></span>
<span data-ttu-id="98ca1-106">O cmdlet **Get-AzureRmMetricDefinition** Obtém definições métricas.</span><span class="sxs-lookup"><span data-stu-id="98ca1-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="98ca1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98ca1-107">EXAMPLES</span></span>

### <span data-ttu-id="98ca1-108">Exemplo 1: obter definições de métrica para um recurso</span><span class="sxs-lookup"><span data-stu-id="98ca1-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="98ca1-109">Este comando obtém as definições de métricas do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="98ca1-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="98ca1-110">Exemplo 2: obter definições de métrica com saída detalhada</span><span class="sxs-lookup"><span data-stu-id="98ca1-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="98ca1-111">Esse comando obtém as definições de métrica para website2.</span><span class="sxs-lookup"><span data-stu-id="98ca1-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="98ca1-112">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="98ca1-112">The output is detailed.</span></span>

### <span data-ttu-id="98ca1-113">Exemplo 3: obter definições métricas por nome</span><span class="sxs-lookup"><span data-stu-id="98ca1-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="98ca1-114">Este comando obtém definições para as métricas BytesSent e CpuTime.</span><span class="sxs-lookup"><span data-stu-id="98ca1-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="98ca1-115">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="98ca1-115">The output is detailed.</span></span>

## <span data-ttu-id="98ca1-116">OS</span><span class="sxs-lookup"><span data-stu-id="98ca1-116">PARAMETERS</span></span>

### <span data-ttu-id="98ca1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ca1-117">-DefaultProfile</span></span>
<span data-ttu-id="98ca1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="98ca1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ca1-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="98ca1-119">-DetailedOutput</span></span>
<span data-ttu-id="98ca1-120">Indica que esta operação incluiu uma saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="98ca1-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="98ca1-121">Se você não especificar esse parâmetro, a saída será resumida.</span><span class="sxs-lookup"><span data-stu-id="98ca1-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ca1-122">-Metricname</span><span class="sxs-lookup"><span data-stu-id="98ca1-122">-MetricName</span></span>
<span data-ttu-id="98ca1-123">Especifica uma matriz de nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="98ca1-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ca1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98ca1-124">-ResourceId</span></span>
<span data-ttu-id="98ca1-125">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="98ca1-125">Specifies the resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98ca1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ca1-126">CommonParameters</span></span>
<span data-ttu-id="98ca1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ca1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ca1-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98ca1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ca1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98ca1-129">INPUTS</span></span>

### <span data-ttu-id="98ca1-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="98ca1-130">None</span></span>
<span data-ttu-id="98ca1-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="98ca1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98ca1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98ca1-132">OUTPUTS</span></span>

### <span data-ttu-id="98ca1-133">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricDefinition []</span><span class="sxs-lookup"><span data-stu-id="98ca1-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="98ca1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98ca1-134">NOTES</span></span>

## <span data-ttu-id="98ca1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98ca1-135">RELATED LINKS</span></span>

[<span data-ttu-id="98ca1-136">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="98ca1-136">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


