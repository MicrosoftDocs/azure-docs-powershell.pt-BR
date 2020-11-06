---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: bdf81228be883d57ecc282aabdf334d7410e339b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598346"
---
# <span data-ttu-id="2e308-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="2e308-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="2e308-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e308-102">SYNOPSIS</span></span>
<span data-ttu-id="2e308-103">Obtém métricas para um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2e308-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="2e308-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e308-104">SYNTAX</span></span>

### <span data-ttu-id="2e308-105">Eles</span><span class="sxs-lookup"><span data-stu-id="2e308-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e308-106">S2</span><span class="sxs-lookup"><span data-stu-id="2e308-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e308-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e308-107">DESCRIPTION</span></span>
<span data-ttu-id="2e308-108">**Get-AzWebAppSlotMetric** Obtém métricas do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="2e308-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="2e308-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e308-109">EXAMPLES</span></span>

### <span data-ttu-id="2e308-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e308-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="2e308-111">Este comando recebe a solicitação do aplicativo Web especificado por minuto (PT1M-Poll time 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="2e308-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="2e308-112">OS</span><span class="sxs-lookup"><span data-stu-id="2e308-112">PARAMETERS</span></span>

### <span data-ttu-id="2e308-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e308-113">-DefaultProfile</span></span>
<span data-ttu-id="2e308-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e308-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e308-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2e308-115">-EndTime</span></span>
<span data-ttu-id="2e308-116">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="2e308-116">End Time in UTC</span></span>

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

### <span data-ttu-id="2e308-117">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="2e308-117">-Granularity</span></span>
<span data-ttu-id="2e308-118">Granularidade</span><span class="sxs-lookup"><span data-stu-id="2e308-118">Granularity</span></span>

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

### <span data-ttu-id="2e308-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="2e308-119">-InstanceDetails</span></span>
<span data-ttu-id="2e308-120">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="2e308-120">Instance Details</span></span>

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

### <span data-ttu-id="2e308-121">-Métricas</span><span class="sxs-lookup"><span data-stu-id="2e308-121">-Metrics</span></span>
<span data-ttu-id="2e308-122">Métricas</span><span class="sxs-lookup"><span data-stu-id="2e308-122">Metrics</span></span>

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

### <span data-ttu-id="2e308-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e308-123">-Name</span></span>
<span data-ttu-id="2e308-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="2e308-124">WebApp Name</span></span>

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

### <span data-ttu-id="2e308-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e308-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e308-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2e308-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2e308-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="2e308-127">-Slot</span></span>
<span data-ttu-id="2e308-128">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="2e308-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2e308-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2e308-129">-StartTime</span></span>
<span data-ttu-id="2e308-130">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="2e308-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="2e308-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2e308-131">-WebApp</span></span>
<span data-ttu-id="2e308-132">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="2e308-132">WebApp Object</span></span>

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

### <span data-ttu-id="2e308-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e308-133">CommonParameters</span></span>
<span data-ttu-id="2e308-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e308-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e308-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e308-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e308-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e308-136">INPUTS</span></span>

### <span data-ttu-id="2e308-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2e308-137">System.String</span></span>

### <span data-ttu-id="2e308-138">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2e308-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2e308-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e308-139">OUTPUTS</span></span>

### <span data-ttu-id="2e308-140">Microsoft. Azure. Management. WebSites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="2e308-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="2e308-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e308-141">NOTES</span></span>

## <span data-ttu-id="2e308-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e308-142">RELATED LINKS</span></span>

[<span data-ttu-id="2e308-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="2e308-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="2e308-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2e308-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="2e308-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2e308-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
