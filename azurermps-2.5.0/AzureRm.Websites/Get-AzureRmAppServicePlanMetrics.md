---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
ms.openlocfilehash: 097b4c5ff6a4a9be32889f104c8e2c8fe0058b13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785132"
---
# <span data-ttu-id="7ab52-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="7ab52-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="7ab52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ab52-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ab52-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ab52-103">SYNTAX</span></span>

### <span data-ttu-id="7ab52-104">Eles</span><span class="sxs-lookup"><span data-stu-id="7ab52-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ab52-105">S2</span><span class="sxs-lookup"><span data-stu-id="7ab52-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ab52-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ab52-106">DESCRIPTION</span></span>
<span data-ttu-id="7ab52-107">O **Get-AzureRmAppServicePlanMetrics** Obtém as métricas do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ab52-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="7ab52-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ab52-108">EXAMPLES</span></span>

### <span data-ttu-id="7ab52-109">1:</span><span class="sxs-lookup"><span data-stu-id="7ab52-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="7ab52-110">Esse comando obtém a porcentagem de CPU do plano do serviço de aplicativo por minuto (PT1M-tempo de votação de 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="7ab52-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="7ab52-111">OS</span><span class="sxs-lookup"><span data-stu-id="7ab52-111">PARAMETERS</span></span>

### <span data-ttu-id="7ab52-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7ab52-112">-AppServicePlan</span></span>
<span data-ttu-id="7ab52-113">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7ab52-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="7ab52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab52-114">-DefaultProfile</span></span>
<span data-ttu-id="7ab52-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab52-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ab52-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7ab52-116">-EndTime</span></span>
<span data-ttu-id="7ab52-117">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="7ab52-117">End Time in UTC</span></span>

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

### <span data-ttu-id="7ab52-118">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="7ab52-118">-Granularity</span></span>
<span data-ttu-id="7ab52-119">Granularidade</span><span class="sxs-lookup"><span data-stu-id="7ab52-119">Granularity</span></span>

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

### <span data-ttu-id="7ab52-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="7ab52-120">-InstanceDetails</span></span>
<span data-ttu-id="7ab52-121">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="7ab52-121">Instance Details</span></span>

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

### <span data-ttu-id="7ab52-122">-Métricas</span><span class="sxs-lookup"><span data-stu-id="7ab52-122">-Metrics</span></span>
<span data-ttu-id="7ab52-123">Métricas</span><span class="sxs-lookup"><span data-stu-id="7ab52-123">Metrics</span></span>

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

### <span data-ttu-id="7ab52-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ab52-124">-Name</span></span>
<span data-ttu-id="7ab52-125">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7ab52-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="7ab52-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab52-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ab52-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7ab52-127">Resource Group Name</span></span>

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

### <span data-ttu-id="7ab52-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7ab52-128">-StartTime</span></span>
<span data-ttu-id="7ab52-129">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="7ab52-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="7ab52-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab52-130">CommonParameters</span></span>
<span data-ttu-id="7ab52-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab52-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab52-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab52-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab52-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ab52-133">INPUTS</span></span>

### <span data-ttu-id="7ab52-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7ab52-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="7ab52-135">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7ab52-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="7ab52-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ab52-136">OUTPUTS</span></span>

## <span data-ttu-id="7ab52-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ab52-137">NOTES</span></span>

## <span data-ttu-id="7ab52-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ab52-138">RELATED LINKS</span></span>

