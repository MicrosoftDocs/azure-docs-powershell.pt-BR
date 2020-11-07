---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
ms.openlocfilehash: 1382ec0f4a2eaa61493e05a762616d9fac54a7f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785410"
---
# <span data-ttu-id="3ea6b-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="3ea6b-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="3ea6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ea6b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea6b-103">Obtém as métricas do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ea6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ea6b-104">SYNTAX</span></span>

### <span data-ttu-id="3ea6b-105">Eles</span><span class="sxs-lookup"><span data-stu-id="3ea6b-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ea6b-106">S2</span><span class="sxs-lookup"><span data-stu-id="3ea6b-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ea6b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ea6b-107">DESCRIPTION</span></span>
<span data-ttu-id="3ea6b-108">O **Get-AzureRmWebAppMetrics** Obtém as métricas do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="3ea6b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-109">EXAMPLES</span></span>

### <span data-ttu-id="3ea6b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ea6b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="3ea6b-111">Este comando obtém solicitações do aplicativo Web ContosoWebApp por minuto (PT1M-tempo de votação de 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="3ea6b-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="3ea6b-112">OS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-112">PARAMETERS</span></span>

### <span data-ttu-id="3ea6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea6b-113">-DefaultProfile</span></span>
<span data-ttu-id="3ea6b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ea6b-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3ea6b-115">-EndTime</span></span>
<span data-ttu-id="3ea6b-116">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="3ea6b-116">End Time in UTC</span></span>

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

### <span data-ttu-id="3ea6b-117">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="3ea6b-117">-Granularity</span></span>
<span data-ttu-id="3ea6b-118">Granularidade</span><span class="sxs-lookup"><span data-stu-id="3ea6b-118">Granularity</span></span>

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

### <span data-ttu-id="3ea6b-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="3ea6b-119">-InstanceDetails</span></span>
<span data-ttu-id="3ea6b-120">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="3ea6b-120">Instance Details</span></span>

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

### <span data-ttu-id="3ea6b-121">-Métricas</span><span class="sxs-lookup"><span data-stu-id="3ea6b-121">-Metrics</span></span>
<span data-ttu-id="3ea6b-122">Métricas como uma matriz de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="3ea6b-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="3ea6b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ea6b-123">-Name</span></span>
<span data-ttu-id="3ea6b-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="3ea6b-124">WebApp Name</span></span>

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

### <span data-ttu-id="3ea6b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea6b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ea6b-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3ea6b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3ea6b-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3ea6b-127">-StartTime</span></span>
<span data-ttu-id="3ea6b-128">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="3ea6b-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="3ea6b-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3ea6b-129">-WebApp</span></span>
<span data-ttu-id="3ea6b-130">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="3ea6b-130">WebApp object</span></span>

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

### <span data-ttu-id="3ea6b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea6b-131">CommonParameters</span></span>
<span data-ttu-id="3ea6b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea6b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea6b-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea6b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea6b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ea6b-134">INPUTS</span></span>

### <span data-ttu-id="3ea6b-135">Instalação</span><span class="sxs-lookup"><span data-stu-id="3ea6b-135">Site</span></span>
<span data-ttu-id="3ea6b-136">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="3ea6b-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3ea6b-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ea6b-137">OUTPUTS</span></span>

## <span data-ttu-id="3ea6b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ea6b-138">NOTES</span></span>

## <span data-ttu-id="3ea6b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ea6b-139">RELATED LINKS</span></span>

[<span data-ttu-id="3ea6b-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="3ea6b-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

