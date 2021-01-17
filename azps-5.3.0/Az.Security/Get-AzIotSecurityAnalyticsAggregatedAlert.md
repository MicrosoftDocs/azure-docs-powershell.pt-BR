---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433306"
---
# <span data-ttu-id="fbe45-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="fbe45-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="fbe45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbe45-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe45-103">Obter alerta de agregação de segurança de IoT</span><span class="sxs-lookup"><span data-stu-id="fbe45-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="fbe45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbe45-104">SYNTAX</span></span>

### <span data-ttu-id="fbe45-105">SolutionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="fbe45-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbe45-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fbe45-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbe45-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbe45-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe45-108">O cmdlet Get-AzIotSecurityAnalyticsAggregatedAlert retorna um ou mais alertas agregados em dispositivos de Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="fbe45-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="fbe45-109">O nome dos alertas agregados é uma combinação do tipo de alerta e a data de aggragted do alerta, separados por '/'.</span><span class="sxs-lookup"><span data-stu-id="fbe45-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="fbe45-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbe45-110">EXAMPLES</span></span>

### <span data-ttu-id="fbe45-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fbe45-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="fbe45-112">Obter o alerta agregado "IoT_Bruteforce_Fail/2019-02-02" (o nome combinado do tipo de alerta e sua data de agregação) em solução "MySolution" e grupo de recursos "MyResource Group"</span><span class="sxs-lookup"><span data-stu-id="fbe45-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="fbe45-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fbe45-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="fbe45-114">Obter uma lista de todos os alertas agregados na solução "MySolution" e grupo de recursos "MyResource Group"</span><span class="sxs-lookup"><span data-stu-id="fbe45-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="fbe45-115">OS</span><span class="sxs-lookup"><span data-stu-id="fbe45-115">PARAMETERS</span></span>

### <span data-ttu-id="fbe45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe45-116">-DefaultProfile</span></span>
<span data-ttu-id="fbe45-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbe45-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbe45-118">-Name</span></span>
<span data-ttu-id="fbe45-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="fbe45-119">Resource name.</span></span>

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

### <span data-ttu-id="fbe45-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe45-120">-ResourceGroupName</span></span>
<span data-ttu-id="fbe45-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbe45-121">Resource group name.</span></span>

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

### <span data-ttu-id="fbe45-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="fbe45-122">-SolutionName</span></span>
<span data-ttu-id="fbe45-123">Nome da solução</span><span class="sxs-lookup"><span data-stu-id="fbe45-123">Solution name</span></span>

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

### <span data-ttu-id="fbe45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe45-124">CommonParameters</span></span>
<span data-ttu-id="fbe45-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe45-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbe45-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe45-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbe45-127">INPUTS</span></span>

### <span data-ttu-id="fbe45-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fbe45-128">None</span></span>

## <span data-ttu-id="fbe45-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbe45-129">OUTPUTS</span></span>

### <span data-ttu-id="fbe45-130">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="fbe45-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="fbe45-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbe45-131">NOTES</span></span>

## <span data-ttu-id="fbe45-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbe45-132">RELATED LINKS</span></span>
