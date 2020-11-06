---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
ms.openlocfilehash: 6afe0a9ce4882b0d04c07db351bf841f6d12b9c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609799"
---
# <span data-ttu-id="22953-101">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="22953-101">Get-AzureRmAutoscaleHistory</span></span>

## <span data-ttu-id="22953-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22953-102">SYNOPSIS</span></span>
<span data-ttu-id="22953-103">Obtém o histórico de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="22953-103">Gets the Autoscale history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22953-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22953-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Status <String>] [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22953-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22953-105">DESCRIPTION</span></span>
<span data-ttu-id="22953-106">O cmdlet **Get-AzureRmAutoscaleHistory** Obtém o histórico de eventos relacionados a uma configuração de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="22953-106">The **Get-AzureRmAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="22953-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22953-107">EXAMPLES</span></span>

### <span data-ttu-id="22953-108">Exemplo 1: obter todos os eventos associados a uma assinatura</span><span class="sxs-lookup"><span data-stu-id="22953-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="22953-109">Esse comando obtém todos os eventos relacionados à autoescala associados à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="22953-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="22953-110">Exemplo 2: GetAutoscaleHistory para um determinado recurso</span><span class="sxs-lookup"><span data-stu-id="22953-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="22953-111">Esse comando obtém todos os eventos relacionados à autoescala associados a um determinado recurso identificado pela ID do recurso (essencialmente, o ResourceURI).</span><span class="sxs-lookup"><span data-stu-id="22953-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="22953-112">OS</span><span class="sxs-lookup"><span data-stu-id="22953-112">PARAMETERS</span></span>

### <span data-ttu-id="22953-113">-Chamador</span><span class="sxs-lookup"><span data-stu-id="22953-113">-Caller</span></span>
<span data-ttu-id="22953-114">Especifica um chamador.</span><span class="sxs-lookup"><span data-stu-id="22953-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="22953-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22953-115">-DefaultProfile</span></span>
<span data-ttu-id="22953-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="22953-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22953-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="22953-117">-DetailedOutput</span></span>
<span data-ttu-id="22953-118">Indica que esta operação incluiu uma saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="22953-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="22953-119">Se você não especificar esse parâmetro, a saída será resumida.</span><span class="sxs-lookup"><span data-stu-id="22953-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="22953-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="22953-120">-EndTime</span></span>
<span data-ttu-id="22953-121">Especifica a hora de término da consulta na hora local.</span><span class="sxs-lookup"><span data-stu-id="22953-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="22953-122">O padrão é a hora atual.</span><span class="sxs-lookup"><span data-stu-id="22953-122">The default is the current time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22953-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22953-123">-ResourceId</span></span>
<span data-ttu-id="22953-124">Especifica a ID do recurso à qual a configuração de autoescala está associada.</span><span class="sxs-lookup"><span data-stu-id="22953-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="22953-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="22953-125">-StartTime</span></span>
<span data-ttu-id="22953-126">Especifica a hora de início da consulta na hora local.</span><span class="sxs-lookup"><span data-stu-id="22953-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="22953-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="22953-127">This parameter is optional.</span></span>
<span data-ttu-id="22953-128">O padrão é a hora local atual menos uma hora.</span><span class="sxs-lookup"><span data-stu-id="22953-128">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22953-129">-Status</span><span class="sxs-lookup"><span data-stu-id="22953-129">-Status</span></span>
<span data-ttu-id="22953-130">Especifica um filtro por status.</span><span class="sxs-lookup"><span data-stu-id="22953-130">Specifies a filter by status.</span></span>
<span data-ttu-id="22953-131">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="22953-131">This parameter is optional.</span></span>
<span data-ttu-id="22953-132">A falha é uma cadeia de caracteres vazia (isto é, sem filtro)</span><span class="sxs-lookup"><span data-stu-id="22953-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="22953-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22953-133">CommonParameters</span></span>
<span data-ttu-id="22953-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22953-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22953-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22953-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22953-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22953-136">INPUTS</span></span>

### <span data-ttu-id="22953-137">System. String</span><span class="sxs-lookup"><span data-stu-id="22953-137">System.String</span></span>

### <span data-ttu-id="22953-138">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22953-138">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="22953-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22953-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22953-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22953-140">OUTPUTS</span></span>

### <span data-ttu-id="22953-141">Microsoft. Azure. Commands. insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="22953-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="22953-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22953-142">NOTES</span></span>

## <span data-ttu-id="22953-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22953-143">RELATED LINKS</span></span>

[<span data-ttu-id="22953-144">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="22953-144">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="22953-145">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="22953-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="22953-146">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="22953-146">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


