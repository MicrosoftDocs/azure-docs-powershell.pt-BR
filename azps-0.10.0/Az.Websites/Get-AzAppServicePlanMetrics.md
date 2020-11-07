---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776125"
---
# <span data-ttu-id="af6c7-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="af6c7-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="af6c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af6c7-102">SYNOPSIS</span></span>
<span data-ttu-id="af6c7-103">Obtém as métricas de plano de serviço Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="af6c7-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="af6c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af6c7-104">SYNTAX</span></span>

### <span data-ttu-id="af6c7-105">Eles</span><span class="sxs-lookup"><span data-stu-id="af6c7-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af6c7-106">S2</span><span class="sxs-lookup"><span data-stu-id="af6c7-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af6c7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af6c7-107">DESCRIPTION</span></span>
<span data-ttu-id="af6c7-108">O **Get-AzAppServicePlanMetrics** Obtém as métricas do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="af6c7-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="af6c7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af6c7-109">EXAMPLES</span></span>

### <span data-ttu-id="af6c7-110">1:</span><span class="sxs-lookup"><span data-stu-id="af6c7-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="af6c7-111">Esse comando obtém a porcentagem de CPU do plano do serviço de aplicativo por minuto (PT1M-tempo de votação de 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="af6c7-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="af6c7-112">OS</span><span class="sxs-lookup"><span data-stu-id="af6c7-112">PARAMETERS</span></span>

### <span data-ttu-id="af6c7-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="af6c7-113">-AppServicePlan</span></span>
<span data-ttu-id="af6c7-114">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="af6c7-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6c7-115">-DefaultProfile</span></span>
<span data-ttu-id="af6c7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af6c7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="af6c7-117">-EndTime</span></span>
<span data-ttu-id="af6c7-118">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="af6c7-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-119">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="af6c7-119">-Granularity</span></span>
<span data-ttu-id="af6c7-120">Granularidade</span><span class="sxs-lookup"><span data-stu-id="af6c7-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="af6c7-121">-InstanceDetails</span></span>
<span data-ttu-id="af6c7-122">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="af6c7-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-123">-Métricas</span><span class="sxs-lookup"><span data-stu-id="af6c7-123">-Metrics</span></span>
<span data-ttu-id="af6c7-124">Métricas</span><span class="sxs-lookup"><span data-stu-id="af6c7-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="af6c7-125">-Name</span></span>
<span data-ttu-id="af6c7-126">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="af6c7-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af6c7-127">-ResourceGroupName</span></span>
<span data-ttu-id="af6c7-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="af6c7-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="af6c7-129">-StartTime</span></span>
<span data-ttu-id="af6c7-130">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="af6c7-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6c7-131">CommonParameters</span></span>
<span data-ttu-id="af6c7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af6c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6c7-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af6c7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6c7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af6c7-134">INPUTS</span></span>

### <span data-ttu-id="af6c7-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="af6c7-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="af6c7-136">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="af6c7-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="af6c7-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af6c7-137">OUTPUTS</span></span>

## <span data-ttu-id="af6c7-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af6c7-138">NOTES</span></span>

## <span data-ttu-id="af6c7-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af6c7-139">RELATED LINKS</span></span>

