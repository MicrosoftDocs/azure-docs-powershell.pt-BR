---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 696332f18074108fd0294248223777c15be0435d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774427"
---
# <span data-ttu-id="8c06d-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="8c06d-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="8c06d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c06d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c06d-103">Obtém métricas para um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8c06d-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="8c06d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c06d-104">SYNTAX</span></span>

### <span data-ttu-id="8c06d-105">Eles</span><span class="sxs-lookup"><span data-stu-id="8c06d-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c06d-106">S2</span><span class="sxs-lookup"><span data-stu-id="8c06d-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c06d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c06d-107">DESCRIPTION</span></span>
<span data-ttu-id="8c06d-108">**Get-AzWebAppSlotMetric** Obtém métricas do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="8c06d-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="8c06d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c06d-109">EXAMPLES</span></span>

### <span data-ttu-id="8c06d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8c06d-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="8c06d-111">Este comando recebe a solicitação do aplicativo Web especificado por minuto (PT1M-Poll time 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="8c06d-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="8c06d-112">OS</span><span class="sxs-lookup"><span data-stu-id="8c06d-112">PARAMETERS</span></span>

### <span data-ttu-id="8c06d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c06d-113">-DefaultProfile</span></span>
<span data-ttu-id="8c06d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c06d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c06d-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8c06d-115">-EndTime</span></span>
<span data-ttu-id="8c06d-116">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="8c06d-116">End Time in UTC</span></span>

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

### <span data-ttu-id="8c06d-117">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="8c06d-117">-Granularity</span></span>
<span data-ttu-id="8c06d-118">Granularidade</span><span class="sxs-lookup"><span data-stu-id="8c06d-118">Granularity</span></span>

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

### <span data-ttu-id="8c06d-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="8c06d-119">-InstanceDetails</span></span>
<span data-ttu-id="8c06d-120">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="8c06d-120">Instance Details</span></span>

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

### <span data-ttu-id="8c06d-121">-Métricas</span><span class="sxs-lookup"><span data-stu-id="8c06d-121">-Metrics</span></span>
<span data-ttu-id="8c06d-122">Métricas</span><span class="sxs-lookup"><span data-stu-id="8c06d-122">Metrics</span></span>

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

### <span data-ttu-id="8c06d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c06d-123">-Name</span></span>
<span data-ttu-id="8c06d-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="8c06d-124">WebApp Name</span></span>

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

### <span data-ttu-id="8c06d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c06d-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c06d-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8c06d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8c06d-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="8c06d-127">-Slot</span></span>
<span data-ttu-id="8c06d-128">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="8c06d-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8c06d-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8c06d-129">-StartTime</span></span>
<span data-ttu-id="8c06d-130">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="8c06d-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="8c06d-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8c06d-131">-WebApp</span></span>
<span data-ttu-id="8c06d-132">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="8c06d-132">WebApp Object</span></span>

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

### <span data-ttu-id="8c06d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c06d-133">CommonParameters</span></span>
<span data-ttu-id="8c06d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c06d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c06d-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c06d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c06d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c06d-136">INPUTS</span></span>

### <span data-ttu-id="8c06d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8c06d-137">System.String</span></span>

### <span data-ttu-id="8c06d-138">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8c06d-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8c06d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c06d-139">OUTPUTS</span></span>

### <span data-ttu-id="8c06d-140">Microsoft. Azure. Management. WebSites. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="8c06d-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="8c06d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c06d-141">NOTES</span></span>

## <span data-ttu-id="8c06d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c06d-142">RELATED LINKS</span></span>

[<span data-ttu-id="8c06d-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="8c06d-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="8c06d-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8c06d-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="8c06d-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c06d-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)