---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: d3a2cd8d0907d26a137df547f1599c9ed09cb7b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113133"
---
# <span data-ttu-id="2cb62-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="2cb62-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="2cb62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cb62-102">SYNOPSIS</span></span>

## <span data-ttu-id="2cb62-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cb62-103">SYNTAX</span></span>

### <span data-ttu-id="2cb62-104">Eles</span><span class="sxs-lookup"><span data-stu-id="2cb62-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb62-105">S2</span><span class="sxs-lookup"><span data-stu-id="2cb62-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cb62-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2cb62-106">DESCRIPTION</span></span>
<span data-ttu-id="2cb62-107">O **Get-AzAppServicePlanMetric** Obtém as métricas do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2cb62-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="2cb62-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cb62-108">EXAMPLES</span></span>

### <span data-ttu-id="2cb62-109">1:</span><span class="sxs-lookup"><span data-stu-id="2cb62-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="2cb62-110">Esse comando obtém a porcentagem de CPU do plano do serviço de aplicativo por minuto (PT1M-tempo de votação de 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="2cb62-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="2cb62-111">OS</span><span class="sxs-lookup"><span data-stu-id="2cb62-111">PARAMETERS</span></span>

### <span data-ttu-id="2cb62-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2cb62-112">-AppServicePlan</span></span>
<span data-ttu-id="2cb62-113">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2cb62-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb62-114">-DefaultProfile</span></span>
<span data-ttu-id="2cb62-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb62-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cb62-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2cb62-116">-EndTime</span></span>
<span data-ttu-id="2cb62-117">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="2cb62-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb62-118">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="2cb62-118">-Granularity</span></span>
<span data-ttu-id="2cb62-119">Granularidade</span><span class="sxs-lookup"><span data-stu-id="2cb62-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb62-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="2cb62-120">-InstanceDetails</span></span>
<span data-ttu-id="2cb62-121">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="2cb62-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb62-122">-Métricas</span><span class="sxs-lookup"><span data-stu-id="2cb62-122">-Metrics</span></span>
<span data-ttu-id="2cb62-123">Métricas</span><span class="sxs-lookup"><span data-stu-id="2cb62-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb62-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cb62-124">-Name</span></span>
<span data-ttu-id="2cb62-125">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2cb62-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb62-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb62-126">-ResourceGroupName</span></span>
<span data-ttu-id="2cb62-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2cb62-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb62-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2cb62-128">-StartTime</span></span>
<span data-ttu-id="2cb62-129">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="2cb62-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb62-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb62-130">CommonParameters</span></span>
<span data-ttu-id="2cb62-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb62-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb62-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cb62-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb62-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2cb62-133">INPUTS</span></span>

### <span data-ttu-id="2cb62-134">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2cb62-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="2cb62-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2cb62-135">OUTPUTS</span></span>

### <span data-ttu-id="2cb62-136">Microsoft. Azure. Management. WebSites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="2cb62-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="2cb62-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2cb62-137">NOTES</span></span>

## <span data-ttu-id="2cb62-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cb62-138">RELATED LINKS</span></span>
