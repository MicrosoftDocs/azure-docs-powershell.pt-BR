---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281602"
---
# <span data-ttu-id="5ce95-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="5ce95-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="5ce95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ce95-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce95-103">Obter recomendação agregada de segurança de IoT</span><span class="sxs-lookup"><span data-stu-id="5ce95-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="5ce95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ce95-104">SYNTAX</span></span>

### <span data-ttu-id="5ce95-105">SolutionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="5ce95-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ce95-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="5ce95-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ce95-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ce95-107">DESCRIPTION</span></span>
<span data-ttu-id="5ce95-108">O cmdlet Get-AzIotSecurityAnalyticsAggregatedAlert retorna uma ou mais recomendações agregadas em dispositivos de Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="5ce95-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="5ce95-109">O nome de uma recomendação agregada é seu tipo</span><span class="sxs-lookup"><span data-stu-id="5ce95-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="5ce95-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ce95-110">EXAMPLES</span></span>

### <span data-ttu-id="5ce95-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ce95-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="5ce95-112">Obter a recomendação agregada "IoT_OpenPorts" na solução de segurança "MySolution" e grupo de recursos "MyResource Group"</span><span class="sxs-lookup"><span data-stu-id="5ce95-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="5ce95-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5ce95-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="5ce95-114">Obter uma lista de recomendações agregadas na solução de segurança "MySolution" e grupo de recursos "MyResource Group"</span><span class="sxs-lookup"><span data-stu-id="5ce95-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="5ce95-115">OS</span><span class="sxs-lookup"><span data-stu-id="5ce95-115">PARAMETERS</span></span>

### <span data-ttu-id="5ce95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce95-116">-DefaultProfile</span></span>
<span data-ttu-id="5ce95-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce95-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ce95-118">-Name</span></span>
<span data-ttu-id="5ce95-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5ce95-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce95-120">-ResourceGroupName</span></span>
<span data-ttu-id="5ce95-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ce95-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce95-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="5ce95-122">-SolutionName</span></span>
<span data-ttu-id="5ce95-123">Nome da solução</span><span class="sxs-lookup"><span data-stu-id="5ce95-123">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce95-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce95-124">CommonParameters</span></span>
<span data-ttu-id="5ce95-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce95-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce95-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ce95-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce95-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ce95-127">INPUTS</span></span>

### <span data-ttu-id="5ce95-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5ce95-128">None</span></span>

## <span data-ttu-id="5ce95-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ce95-129">OUTPUTS</span></span>

### <span data-ttu-id="5ce95-130">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="5ce95-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="5ce95-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ce95-131">NOTES</span></span>

## <span data-ttu-id="5ce95-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ce95-132">RELATED LINKS</span></span>
