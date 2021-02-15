---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112959"
---
# <span data-ttu-id="35cbe-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="35cbe-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="35cbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="35cbe-103">Obtém definições métricas.</span><span class="sxs-lookup"><span data-stu-id="35cbe-103">Gets metric definitions.</span></span>

## <span data-ttu-id="35cbe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35cbe-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35cbe-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="35cbe-105">DESCRIPTION</span></span>
<span data-ttu-id="35cbe-106">O **cmdlet Get-AzMetricDefinition obtém** definições métricas.</span><span class="sxs-lookup"><span data-stu-id="35cbe-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="35cbe-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35cbe-107">EXAMPLES</span></span>

### <span data-ttu-id="35cbe-108">Exemplo 1: Obter definições métricas para um recurso</span><span class="sxs-lookup"><span data-stu-id="35cbe-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
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

<span data-ttu-id="35cbe-109">Esse comando obtém as definições de métrica para o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="35cbe-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="35cbe-110">Exemplo 2: Obter definições métricas com saída detalhada</span><span class="sxs-lookup"><span data-stu-id="35cbe-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
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

<span data-ttu-id="35cbe-111">Esse comando obtém as definições de métrica para o site2.</span><span class="sxs-lookup"><span data-stu-id="35cbe-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="35cbe-112">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="35cbe-112">The output is detailed.</span></span>

### <span data-ttu-id="35cbe-113">Exemplo 3: Obter definições métricas por nome</span><span class="sxs-lookup"><span data-stu-id="35cbe-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
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

<span data-ttu-id="35cbe-114">Esse comando obtém definições para as métricas BytesSent e CpuTime.</span><span class="sxs-lookup"><span data-stu-id="35cbe-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="35cbe-115">A saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="35cbe-115">The output is detailed.</span></span>

## <span data-ttu-id="35cbe-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35cbe-116">PARAMETERS</span></span>

### <span data-ttu-id="35cbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35cbe-117">-DefaultProfile</span></span>
<span data-ttu-id="35cbe-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="35cbe-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35cbe-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="35cbe-119">-DetailedOutput</span></span>
<span data-ttu-id="35cbe-120">Indica que essa operação incluiu saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="35cbe-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="35cbe-121">Se você não especificar esse parâmetro, a saída será resumida.</span><span class="sxs-lookup"><span data-stu-id="35cbe-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="35cbe-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="35cbe-122">-MetricName</span></span>
<span data-ttu-id="35cbe-123">Especifica uma matriz de nomes de métricas.</span><span class="sxs-lookup"><span data-stu-id="35cbe-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="35cbe-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="35cbe-124">-MetricNamespace</span></span>
<span data-ttu-id="35cbe-125">Especifica o namespace métrico para as definições da métrica de consulta.</span><span class="sxs-lookup"><span data-stu-id="35cbe-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="35cbe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35cbe-126">-ResourceId</span></span>
<span data-ttu-id="35cbe-127">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="35cbe-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="35cbe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cbe-128">CommonParameters</span></span>
<span data-ttu-id="35cbe-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35cbe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cbe-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35cbe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cbe-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="35cbe-131">INPUTS</span></span>

### <span data-ttu-id="35cbe-132">System.String</span><span class="sxs-lookup"><span data-stu-id="35cbe-132">System.String</span></span>

### <span data-ttu-id="35cbe-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="35cbe-133">System.String[]</span></span>

## <span data-ttu-id="35cbe-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="35cbe-134">OUTPUTS</span></span>

### <span data-ttu-id="35cbe-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="35cbe-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="35cbe-136">Notas</span><span class="sxs-lookup"><span data-stu-id="35cbe-136">NOTES</span></span>

<span data-ttu-id="35cbe-137">Mais informações sobre as métricas com suporte podem ser encontradas em: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="35cbe-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="35cbe-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35cbe-138">RELATED LINKS</span></span>

<span data-ttu-id="35cbe-139">[Get-AzMetric](./Get-AzMetric.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="35cbe-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


