---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c336c1bb2c2485c5bef691a5d5560a1b8795360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426246"
---
# <span data-ttu-id="ef5f5-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ef5f5-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="ef5f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5f5-103">Obtém métricas para um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ef5f5-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef5f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef5f5-104">SYNTAX</span></span>

### <span data-ttu-id="ef5f5-105">Eles</span><span class="sxs-lookup"><span data-stu-id="ef5f5-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef5f5-106">S2</span><span class="sxs-lookup"><span data-stu-id="ef5f5-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef5f5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef5f5-107">DESCRIPTION</span></span>
<span data-ttu-id="ef5f5-108">**Get-AzureRmWebAppSlotMetrics** Obtém métricas do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="ef5f5-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="ef5f5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef5f5-109">EXAMPLES</span></span>

### <span data-ttu-id="ef5f5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef5f5-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="ef5f5-111">Este comando recebe a solicitação do aplicativo Web especificado por minuto (PT1M-Poll time 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="ef5f5-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="ef5f5-112">OS</span><span class="sxs-lookup"><span data-stu-id="ef5f5-112">PARAMETERS</span></span>

### <span data-ttu-id="ef5f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5f5-113">-DefaultProfile</span></span>
<span data-ttu-id="ef5f5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef5f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef5f5-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ef5f5-115">-EndTime</span></span>
<span data-ttu-id="ef5f5-116">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="ef5f5-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f5-117">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="ef5f5-117">-Granularity</span></span>
<span data-ttu-id="ef5f5-118">Granularidade</span><span class="sxs-lookup"><span data-stu-id="ef5f5-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f5-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="ef5f5-119">-InstanceDetails</span></span>
<span data-ttu-id="ef5f5-120">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="ef5f5-120">Instance Details</span></span>

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

### <span data-ttu-id="ef5f5-121">-Métricas</span><span class="sxs-lookup"><span data-stu-id="ef5f5-121">-Metrics</span></span>
<span data-ttu-id="ef5f5-122">Métricas</span><span class="sxs-lookup"><span data-stu-id="ef5f5-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef5f5-123">-Name</span></span>
<span data-ttu-id="ef5f5-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ef5f5-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef5f5-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ef5f5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ef5f5-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="ef5f5-127">-Slot</span></span>
<span data-ttu-id="ef5f5-128">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="ef5f5-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f5-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ef5f5-129">-StartTime</span></span>
<span data-ttu-id="ef5f5-130">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="ef5f5-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f5-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ef5f5-131">-WebApp</span></span>
<span data-ttu-id="ef5f5-132">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ef5f5-132">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5f5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5f5-133">CommonParameters</span></span>
<span data-ttu-id="ef5f5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef5f5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5f5-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef5f5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5f5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef5f5-136">INPUTS</span></span>

### <span data-ttu-id="ef5f5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ef5f5-137">System.String</span></span>

### <span data-ttu-id="ef5f5-138">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="ef5f5-138">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ef5f5-139">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef5f5-139">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ef5f5-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef5f5-140">OUTPUTS</span></span>

### <span data-ttu-id="ef5f5-141">Microsoft. Azure. Management. WebSites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="ef5f5-141">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="ef5f5-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef5f5-142">NOTES</span></span>

## <span data-ttu-id="ef5f5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef5f5-143">RELATED LINKS</span></span>

[<span data-ttu-id="ef5f5-144">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="ef5f5-144">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="ef5f5-145">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef5f5-145">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ef5f5-146">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ef5f5-146">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
