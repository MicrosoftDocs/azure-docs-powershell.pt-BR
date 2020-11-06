---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: c33038289483c2cd48ac63eb09a4a38627c406da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427387"
---
# <span data-ttu-id="58da8-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="58da8-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="58da8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58da8-102">SYNOPSIS</span></span>
<span data-ttu-id="58da8-103">Obtém as métricas do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="58da8-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58da8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58da8-104">SYNTAX</span></span>

### <span data-ttu-id="58da8-105">Eles</span><span class="sxs-lookup"><span data-stu-id="58da8-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58da8-106">S2</span><span class="sxs-lookup"><span data-stu-id="58da8-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58da8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58da8-107">DESCRIPTION</span></span>
<span data-ttu-id="58da8-108">O **Get-AzureRmWebAppMetrics** Obtém as métricas do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="58da8-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="58da8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58da8-109">EXAMPLES</span></span>

### <span data-ttu-id="58da8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58da8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="58da8-111">Este comando obtém solicitações do aplicativo Web ContosoWebApp por minuto (PT1M-tempo de votação de 1 minuto) entre StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="58da8-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="58da8-112">OS</span><span class="sxs-lookup"><span data-stu-id="58da8-112">PARAMETERS</span></span>

### <span data-ttu-id="58da8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58da8-113">-DefaultProfile</span></span>
<span data-ttu-id="58da8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58da8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58da8-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="58da8-115">-EndTime</span></span>
<span data-ttu-id="58da8-116">Hora de término em UTC</span><span class="sxs-lookup"><span data-stu-id="58da8-116">End Time in UTC</span></span>

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

### <span data-ttu-id="58da8-117">-Granularidade</span><span class="sxs-lookup"><span data-stu-id="58da8-117">-Granularity</span></span>
<span data-ttu-id="58da8-118">Granularidade</span><span class="sxs-lookup"><span data-stu-id="58da8-118">Granularity</span></span>

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

### <span data-ttu-id="58da8-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="58da8-119">-InstanceDetails</span></span>
<span data-ttu-id="58da8-120">Detalhes da instância</span><span class="sxs-lookup"><span data-stu-id="58da8-120">Instance Details</span></span>

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

### <span data-ttu-id="58da8-121">-Métricas</span><span class="sxs-lookup"><span data-stu-id="58da8-121">-Metrics</span></span>
<span data-ttu-id="58da8-122">Métricas como uma matriz de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="58da8-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="58da8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="58da8-123">-Name</span></span>
<span data-ttu-id="58da8-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="58da8-124">WebApp Name</span></span>

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

### <span data-ttu-id="58da8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58da8-125">-ResourceGroupName</span></span>
<span data-ttu-id="58da8-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="58da8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="58da8-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="58da8-127">-StartTime</span></span>
<span data-ttu-id="58da8-128">Hora de início em UTC</span><span class="sxs-lookup"><span data-stu-id="58da8-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="58da8-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="58da8-129">-WebApp</span></span>
<span data-ttu-id="58da8-130">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="58da8-130">WebApp object</span></span>

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

### <span data-ttu-id="58da8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58da8-131">CommonParameters</span></span>
<span data-ttu-id="58da8-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58da8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58da8-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58da8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58da8-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58da8-134">INPUTS</span></span>

### <span data-ttu-id="58da8-135">Instalação</span><span class="sxs-lookup"><span data-stu-id="58da8-135">Site</span></span>
<span data-ttu-id="58da8-136">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="58da8-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="58da8-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58da8-137">OUTPUTS</span></span>

## <span data-ttu-id="58da8-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58da8-138">NOTES</span></span>

## <span data-ttu-id="58da8-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58da8-139">RELATED LINKS</span></span>

[<span data-ttu-id="58da8-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="58da8-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

