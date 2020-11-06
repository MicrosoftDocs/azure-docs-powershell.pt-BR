---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c4399146d99da6317c70fc08f7b01dc9679525a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428681"
---
# <span data-ttu-id="dace2-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="dace2-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="dace2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dace2-102">SYNOPSIS</span></span>
<span data-ttu-id="dace2-103">Obtém métricas para um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dace2-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dace2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dace2-104">SYNTAX</span></span>

### <span data-ttu-id="dace2-105">Eles</span><span class="sxs-lookup"><span data-stu-id="dace2-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dace2-106">S2</span><span class="sxs-lookup"><span data-stu-id="dace2-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dace2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dace2-107">DESCRIPTION</span></span>
<span data-ttu-id="dace2-108">**Get-AzureRmWebAppSlotMetrics** Obtém métricas do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="dace2-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="dace2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dace2-109">EXAMPLES</span></span>

### <span data-ttu-id="dace2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dace2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="dace2-111">Este comando recebe a solicitação do aplicativo Web especificado por minuto (PT1M-Poll time 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="dace2-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="dace2-112">OS</span><span class="sxs-lookup"><span data-stu-id="dace2-112">PARAMETERS</span></span>

### <span data-ttu-id="dace2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dace2-113">-DefaultProfile</span></span>
<span data-ttu-id="dace2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dace2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dace2-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dace2-115">-EndTime</span></span>
<span data-ttu-id="dace2-116">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="dace2-116">End Time in UTC</span></span>

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

### <span data-ttu-id="dace2-117">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="dace2-117">-Granularity</span></span>
<span data-ttu-id="dace2-118">Granularidade</span><span class="sxs-lookup"><span data-stu-id="dace2-118">Granularity</span></span>

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

### <span data-ttu-id="dace2-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="dace2-119">-InstanceDetails</span></span>
<span data-ttu-id="dace2-120">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="dace2-120">Instance Details</span></span>

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

### <span data-ttu-id="dace2-121">-Métricas</span><span class="sxs-lookup"><span data-stu-id="dace2-121">-Metrics</span></span>
<span data-ttu-id="dace2-122">Métricas</span><span class="sxs-lookup"><span data-stu-id="dace2-122">Metrics</span></span>

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

### <span data-ttu-id="dace2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="dace2-123">-Name</span></span>
<span data-ttu-id="dace2-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="dace2-124">WebApp Name</span></span>

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

### <span data-ttu-id="dace2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dace2-125">-ResourceGroupName</span></span>
<span data-ttu-id="dace2-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dace2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dace2-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="dace2-127">-Slot</span></span>
<span data-ttu-id="dace2-128">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="dace2-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="dace2-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dace2-129">-StartTime</span></span>
<span data-ttu-id="dace2-130">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="dace2-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="dace2-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dace2-131">-WebApp</span></span>
<span data-ttu-id="dace2-132">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="dace2-132">WebApp Object</span></span>

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

### <span data-ttu-id="dace2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dace2-133">CommonParameters</span></span>
<span data-ttu-id="dace2-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dace2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dace2-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dace2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dace2-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dace2-136">INPUTS</span></span>

### <span data-ttu-id="dace2-137">Instalação</span><span class="sxs-lookup"><span data-stu-id="dace2-137">Site</span></span>
<span data-ttu-id="dace2-138">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="dace2-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="dace2-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dace2-139">OUTPUTS</span></span>

## <span data-ttu-id="dace2-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dace2-140">NOTES</span></span>

## <span data-ttu-id="dace2-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dace2-141">RELATED LINKS</span></span>

[<span data-ttu-id="dace2-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="dace2-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="dace2-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="dace2-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="dace2-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dace2-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)