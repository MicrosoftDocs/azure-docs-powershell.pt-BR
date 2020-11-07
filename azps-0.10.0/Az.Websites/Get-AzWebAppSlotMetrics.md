---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotMetrics.md
ms.openlocfilehash: 474f5a450adba9f01ef56fe99875d062ece1689d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776102"
---
# <span data-ttu-id="20497-101">Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="20497-101">Get-AzWebAppSlotMetrics</span></span>

## <span data-ttu-id="20497-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20497-102">SYNOPSIS</span></span>
<span data-ttu-id="20497-103">Obtém métricas para um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="20497-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="20497-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20497-104">SYNTAX</span></span>

### <span data-ttu-id="20497-105">Eles</span><span class="sxs-lookup"><span data-stu-id="20497-105">S1</span></span>
```
Get-AzWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20497-106">S2</span><span class="sxs-lookup"><span data-stu-id="20497-106">S2</span></span>
```
Get-AzWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20497-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20497-107">DESCRIPTION</span></span>
<span data-ttu-id="20497-108">**Get-AzWebAppSlotMetrics** Obtém métricas do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="20497-108">The **Get-AzWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="20497-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20497-109">EXAMPLES</span></span>

### <span data-ttu-id="20497-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20497-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="20497-111">Este comando recebe a solicitação do aplicativo Web especificado por minuto (PT1M-Poll time 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="20497-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="20497-112">OS</span><span class="sxs-lookup"><span data-stu-id="20497-112">PARAMETERS</span></span>

### <span data-ttu-id="20497-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20497-113">-DefaultProfile</span></span>
<span data-ttu-id="20497-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20497-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20497-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="20497-115">-EndTime</span></span>
<span data-ttu-id="20497-116">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="20497-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20497-117">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="20497-117">-Granularity</span></span>
<span data-ttu-id="20497-118">Granularidade</span><span class="sxs-lookup"><span data-stu-id="20497-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20497-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="20497-119">-InstanceDetails</span></span>
<span data-ttu-id="20497-120">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="20497-120">Instance Details</span></span>

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

### <span data-ttu-id="20497-121">-Métricas</span><span class="sxs-lookup"><span data-stu-id="20497-121">-Metrics</span></span>
<span data-ttu-id="20497-122">Métricas</span><span class="sxs-lookup"><span data-stu-id="20497-122">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20497-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="20497-123">-Name</span></span>
<span data-ttu-id="20497-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="20497-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20497-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20497-125">-ResourceGroupName</span></span>
<span data-ttu-id="20497-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="20497-126">Resource Group Name</span></span>

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

### <span data-ttu-id="20497-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="20497-127">-Slot</span></span>
<span data-ttu-id="20497-128">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="20497-128">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20497-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="20497-129">-StartTime</span></span>
<span data-ttu-id="20497-130">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="20497-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20497-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="20497-131">-WebApp</span></span>
<span data-ttu-id="20497-132">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="20497-132">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20497-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20497-133">CommonParameters</span></span>
<span data-ttu-id="20497-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20497-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20497-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20497-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20497-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20497-136">INPUTS</span></span>

### <span data-ttu-id="20497-137">Instalação</span><span class="sxs-lookup"><span data-stu-id="20497-137">Site</span></span>
<span data-ttu-id="20497-138">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="20497-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="20497-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20497-139">OUTPUTS</span></span>

## <span data-ttu-id="20497-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20497-140">NOTES</span></span>

## <span data-ttu-id="20497-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20497-141">RELATED LINKS</span></span>

[<span data-ttu-id="20497-142">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="20497-142">Get-AzAppServicePlanMetrics</span></span>](./Get-AzAppServicePlanMetrics.md)

[<span data-ttu-id="20497-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="20497-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="20497-144">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="20497-144">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
