---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: 65892738ac244a0af82e017efc015c0113a6ed72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603077"
---
# <span data-ttu-id="62ce8-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="62ce8-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="62ce8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62ce8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62ce8-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62ce8-103">SYNTAX</span></span>

### <span data-ttu-id="62ce8-104">Eles</span><span class="sxs-lookup"><span data-stu-id="62ce8-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ce8-105">S2</span><span class="sxs-lookup"><span data-stu-id="62ce8-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62ce8-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62ce8-106">DESCRIPTION</span></span>
<span data-ttu-id="62ce8-107">O **Get-AzureRmAppServicePlanMetrics** Obtém as métricas do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="62ce8-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="62ce8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62ce8-108">EXAMPLES</span></span>

### <span data-ttu-id="62ce8-109">1:</span><span class="sxs-lookup"><span data-stu-id="62ce8-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="62ce8-110">Esse comando obtém a porcentagem de CPU do plano do serviço de aplicativo por minuto (PT1M-tempo de votação de 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="62ce8-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="62ce8-111">OS</span><span class="sxs-lookup"><span data-stu-id="62ce8-111">PARAMETERS</span></span>

### <span data-ttu-id="62ce8-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="62ce8-112">-AppServicePlan</span></span>
<span data-ttu-id="62ce8-113">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="62ce8-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62ce8-114">-EndTime</span><span class="sxs-lookup"><span data-stu-id="62ce8-114">-EndTime</span></span>
<span data-ttu-id="62ce8-115">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="62ce8-115">End Time in UTC</span></span>

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

### <span data-ttu-id="62ce8-116">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="62ce8-116">-Granularity</span></span>
<span data-ttu-id="62ce8-117">Granularidade</span><span class="sxs-lookup"><span data-stu-id="62ce8-117">Granularity</span></span>

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

### <span data-ttu-id="62ce8-118">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="62ce8-118">-InstanceDetails</span></span>
<span data-ttu-id="62ce8-119">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="62ce8-119">Instance Details</span></span>

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

### <span data-ttu-id="62ce8-120">-Métricas</span><span class="sxs-lookup"><span data-stu-id="62ce8-120">-Metrics</span></span>
<span data-ttu-id="62ce8-121">Métricas</span><span class="sxs-lookup"><span data-stu-id="62ce8-121">Metrics</span></span>

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

### <span data-ttu-id="62ce8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="62ce8-122">-Name</span></span>
<span data-ttu-id="62ce8-123">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="62ce8-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="62ce8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ce8-124">-ResourceGroupName</span></span>
<span data-ttu-id="62ce8-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="62ce8-125">Resource Group Name</span></span>

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

### <span data-ttu-id="62ce8-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="62ce8-126">-StartTime</span></span>
<span data-ttu-id="62ce8-127">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="62ce8-127">Start Time in UTC</span></span>

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

### <span data-ttu-id="62ce8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ce8-128">-DefaultProfile</span></span>
<span data-ttu-id="62ce8-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62ce8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ce8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ce8-130">CommonParameters</span></span>
<span data-ttu-id="62ce8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ce8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ce8-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ce8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ce8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62ce8-133">INPUTS</span></span>

### <span data-ttu-id="62ce8-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="62ce8-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="62ce8-135">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="62ce8-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="62ce8-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62ce8-136">OUTPUTS</span></span>

## <span data-ttu-id="62ce8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62ce8-137">NOTES</span></span>

## <span data-ttu-id="62ce8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62ce8-138">RELATED LINKS</span></span>

