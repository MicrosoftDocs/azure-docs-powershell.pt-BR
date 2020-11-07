---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAlert.md
ms.openlocfilehash: 451815b5a342a4a870e50f7ffc65af7476b46683
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944685"
---
# <span data-ttu-id="a4091-101">Get-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="a4091-101">Get-AzSecurityAlert</span></span>

## <span data-ttu-id="a4091-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4091-102">SYNOPSIS</span></span>
<span data-ttu-id="a4091-103">Obtém alertas de segurança detectados pela central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="a4091-103">Gets security alerts that were detected by Azure Security Center</span></span>

## <span data-ttu-id="a4091-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4091-104">SYNTAX</span></span>

### <span data-ttu-id="a4091-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="a4091-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAlert [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4091-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="a4091-106">ResourceGroupScope</span></span>
```
Get-AzSecurityAlert -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4091-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="a4091-107">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAlert -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4091-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a4091-108">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAlert -Name <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4091-109">Identificação</span><span class="sxs-lookup"><span data-stu-id="a4091-109">ResourceId</span></span>
```
Get-AzSecurityAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4091-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4091-110">DESCRIPTION</span></span>
<span data-ttu-id="a4091-111">Obtém alertas de segurança detectados pela central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="a4091-111">Gets security alerts that were detected by Azure Security Center</span></span>

## <span data-ttu-id="a4091-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4091-112">EXAMPLES</span></span>

### <span data-ttu-id="a4091-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4091-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAlert


Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/RSG/providers/Microsoft.Securit
                     y/locations/centralus/alerts/2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF
Name               : 2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF
ActionTaken        : Undefined
AlertDisplayName   : PREVIEW - Vulnerability scanner detected
AlertName          : APPS_WpScanner
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/RSG/providers/Microsoft.Web/sit
                     es/testSite1
CanBeInvestigated  : True
CompromisedEntity  : testSite1
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Azure App Services activity log indicates a possible vulnerability scanner usage on your App 
                     Service resource.
                     The suspicious activity detected resembles that of tools targeting WordPress applications.
DetectedTimeUtc    : 10/07/2018 11:49:30
Entities           : {}
ExtendedProperties : {[sample User Agents, WPScan+v2.9.3+(http://wpscan.org)], [last Event Time, 6/23/2018 12:18:58 
                     AM], [sample URIs, /wp-config.php.original, /wp-includes/css/editor.min.css, 
                     /wp-includes/js/wp-emoji.js, /wp-config.old, /xmlrpc.php, /wp-admin/css/wp-admin-rtl.css, 
                     /#wp-config.php#, /wp-includes/js/tinymce/plugins/wplink/plugin.js, 
                     /wp-includes/js/tinymce/plugins/wordpress/editor_plugin.js, /wp-admin/js/post.js], [sample 
                     Referer, https://www.stone.com.br/]...}
InstanceId         : fff23c70-80ef-4a8b-9122-507b0ea8dfff
RemediationSteps   : 1. If WordPress is installed, make sure that the application is up to date and automatic updates 
                     are enabled.
                     2. If only specific IPs should access to the web application, use IP Restrictions 
                     (https://docs.microsoft.com/en-us/azure/app-service/app-service-ip-restrictions).
ReportedSeverity   : High
ReportedTimeUtc    : 10/07/2018 16:31:52
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : 
VendorName         : Microsoft
WorkspaceArmId     : 

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/central
                     us/alerts/2518710774894070750_EEE23C70-80EF-4A8B-9122-507B0EA8DFFF
Name               : 2518710774894070750_EEE23C70-80EF-4A8B-9122-507B0EA8DFFF
ActionTaken        : Undefined
AlertDisplayName   : PREVIEW - Spam folder referrer detected
AlertName          : APPS_SpamReferrer
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Web/sites/testSite2
CanBeInvestigated  : True
CompromisedEntity  : testSite2
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Azure App Services activity log indicates web activity that was identified as originating from a 
                     web site associated with SPAM activity.
                     This could occur if your web site is compromised and used for spam activity.
DetectedTimeUtc    : 10/07/2018 11:48:30
Entities           : {}
ExtendedProperties : {[sample User Agents, Mozilla/4.0+(compatible;+MSIE+6.0;+Windows+NT+5.1)], [last Event Time, 
                     6/23/2018 4:53:58 PM], [sample URIs, /acropolis.php, /wp-content/animator.php, /bandpass.php, 
                     /wp-content/base.php, /candid.php, /wp-content/uploads/2018/christina.php, 
                     /wp-content/climax.php, /wp-content/uploads/conditioning.php, /wp-content/corkscrew.php, 
                     /wp-content/uploads/2018/countermeasures.php], [sample Referer, 
                     https://google.com/mail/inbox/spam/]...}
InstanceId         : eee23c70-80ef-4a8b-9122-507b0ea8dfff
RemediationSteps   : Review the URIs in the alert details. Check whether the corresponding files contain malicious or 
                     suspicious content. 
                     If they do, escalate the alert to the information security team.
ReportedSeverity   : High
ReportedTimeUtc    : 10/07/2018 16:31:52
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : 
VendorName         : Microsoft
WorkspaceArmId     : 

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Security/locations/westeurope/alerts/2518675199999999999_0501972d-06cd-47c7-a276-036f67d89262
Name               : 2518675199999999999_0501972d-06cd-47c7-a276-036f67d89262
ActionTaken        : Detected
AlertDisplayName   : PROTOCOL-ENFORCEMENT
AlertName          : PROTOCOL-ENFORCEMENT
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Network/applicationGateways/ContosoWAF
CanBeInvestigated  : True
CompromisedEntity  : 10.1.0.4
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Detail:Host header is a numeric IP address 13.69.131.117:80
DetectedTimeUtc    : 20/08/2018 16:00:00
Entities           : {}
ExtendedProperties : {[hit Count, 1], [source IPs, 177.189.28.238], [management URL, https://portal.azure.com#resource/
                     subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.N
                     etwork/applicationGateways/ContosoWAF/overview], [resourceType, Networking]}
InstanceId         : 0501972d-06cd-47c7-a276-036f67d89262
RemediationSteps   : 
ReportedSeverity   : Low
ReportedTimeUtc    : 20/08/2018 17:00:18
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : Azure
VendorName         : Microsoft WAF
WorkspaceArmId     : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provid
                     ers/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869
                     -eus

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Security/locations/westeurope/alerts/2518675235999999999_0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
Name               : 2518675235999999999_0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
ActionTaken        : Detected
AlertDisplayName   : PROTOCOL-ENFORCEMENT
AlertName          : PROTOCOL-ENFORCEMENT
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Network/applicationGateways/ContosoWAF
CanBeInvestigated  : True
CompromisedEntity  : 10.1.0.4
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Detail:Host header is a numeric IP address 13.69.131.117
DetectedTimeUtc    : 20/08/2018 15:00:00
Entities           : {}
ExtendedProperties : {[hit Count, 1], [source IPs, 217.91.251.86], [management URL, https://portal.azure.com#resource/s
                     ubscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Ne
                     twork/applicationGateways/ContosoWAF/overview], [resourceType, Networking]}
InstanceId         : 0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
RemediationSteps   : 
ReportedSeverity   : Low
ReportedTimeUtc    : 20/08/2018 16:00:03
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : Azure
VendorName         : Microsoft WAF
WorkspaceArmId     : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provid
                     ers/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869
                     -eus
```

<span data-ttu-id="a4091-114">Obtém todos os alertas de segurança detectados nos recursos dentro de uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a4091-114">Gets all the security alerts that were detected on resources inside a subscription</span></span>

### <span data-ttu-id="a4091-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a4091-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAlert -ResourceGroupName "myService1"


Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Security/locations/westeurope/alerts/2518675199999999999_0501972d-06cd-47c7-a276-036f67d89262
Name               : 2518675199999999999_0501972d-06cd-47c7-a276-036f67d89262
ActionTaken        : Detected
AlertDisplayName   : PROTOCOL-ENFORCEMENT
AlertName          : PROTOCOL-ENFORCEMENT
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Network/applicationGateways/ContosoWAF
CanBeInvestigated  : True
CompromisedEntity  : 10.1.0.4
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Detail:Host header is a numeric IP address 13.69.131.117:80
DetectedTimeUtc    : 20/08/2018 16:00:00
Entities           : {}
ExtendedProperties : {[hit Count, 1], [source IPs, 177.189.28.238], [management URL, https://portal.azure.com#resource/
                     subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.N
                     etwork/applicationGateways/ContosoWAF/overview], [resourceType, Networking]}
InstanceId         : 0501972d-06cd-47c7-a276-036f67d89262
RemediationSteps   : 
ReportedSeverity   : Low
ReportedTimeUtc    : 20/08/2018 17:00:18
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : Azure
VendorName         : Microsoft WAF
WorkspaceArmId     : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provid
                     ers/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869
                     -eus

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Security/locations/westeurope/alerts/2518675235999999999_0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
Name               : 2518675235999999999_0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
ActionTaken        : Detected
AlertDisplayName   : PROTOCOL-ENFORCEMENT
AlertName          : PROTOCOL-ENFORCEMENT
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Network/applicationGateways/ContosoWAF
CanBeInvestigated  : True
CompromisedEntity  : 10.1.0.4
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Detail:Host header is a numeric IP address 13.69.131.117
DetectedTimeUtc    : 20/08/2018 15:00:00
Entities           : {}
ExtendedProperties : {[hit Count, 1], [source IPs, 217.91.251.86], [management URL, https://portal.azure.com#resource/s
                     ubscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Ne
                     twork/applicationGateways/ContosoWAF/overview], [resourceType, Networking]}
InstanceId         : 0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
RemediationSteps   : 
ReportedSeverity   : Low
ReportedTimeUtc    : 20/08/2018 16:00:03
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : Azure
VendorName         : Microsoft WAF
WorkspaceArmId     : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provid
                     ers/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869
                     -eus

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Security/locations/westeurope/alerts/2518675235999999999_3cc2c984-3d3d-4af2-a2d9-ed7c6d078315
Name               : 2518675235999999999_3cc2c984-3d3d-4af2-a2d9-ed7c6d078315
ActionTaken        : Detected
AlertDisplayName   : PROTOCOL-ENFORCEMENT
AlertName          : PROTOCOL-ENFORCEMENT
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Network/applicationGateways/ContosoWAF
CanBeInvestigated  : True
CompromisedEntity  : 10.1.0.5
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Detail:Host header is a numeric IP address 13.69.131.117
DetectedTimeUtc    : 20/08/2018 15:00:00
Entities           : {}
ExtendedProperties : {[hit Count, 1], [source IPs, 217.91.251.86], [management URL, https://portal.azure.com#resource/s
                     ubscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Ne
                     twork/applicationGateways/ContosoWAF/overview], [resourceType, Networking]}
InstanceId         : 3cc2c984-3d3d-4af2-a2d9-ed7c6d078315
RemediationSteps   : 
ReportedSeverity   : Low
ReportedTimeUtc    : 20/08/2018 16:00:04
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : Azure
VendorName         : Microsoft WAF
WorkspaceArmId     : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provid
                     ers/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869
                     -eus

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Security/locations/westeurope/alerts/2518675307999999999_bbbda0ad-b149-49f4-a4ba-3e95540cbf1c
Name               : 2518675307999999999_bbbda0ad-b149-49f4-a4ba-3e95540cbf1c
ActionTaken        : Detected
AlertDisplayName   : PROTOCOL-ENFORCEMENT
AlertName          : PROTOCOL-ENFORCEMENT
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Network/applicationGateways/ContosoWAF
CanBeInvestigated  : True
CompromisedEntity  : 10.1.0.4
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Detail:Host header is a numeric IP address 13.69.131.117:80
DetectedTimeUtc    : 20/08/2018 13:00:00
Entities           : {}
ExtendedProperties : {[hit Count, 1], [source IPs, 177.86.202.171], [management URL, https://portal.azure.com#resource/
                     subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.N
                     etwork/applicationGateways/ContosoWAF/overview], [resourceType, Networking]}
InstanceId         : bbbda0ad-b149-49f4-a4ba-3e95540cbf1c
RemediationSteps   : 
ReportedSeverity   : Low
ReportedTimeUtc    : 20/08/2018 14:00:36
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : Azure
VendorName         : Microsoft WAF
WorkspaceArmId     : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provid
                     ers/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869
                     -eus
```

<span data-ttu-id="a4091-116">Obtém todos os alertas de segurança detectados nos recursos dentro do grupo de recursos "myService1"</span><span class="sxs-lookup"><span data-stu-id="a4091-116">Gets all the security alerts that were detected on resources inside the "myService1" resource group</span></span>

### <span data-ttu-id="a4091-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a4091-117">Example 3</span></span>
```powershell
PS C:\> Get-AzSecurityAlert -ResourceGroupName "myService1" -Location "westeurope" -Name "2518675235999999999_0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0"


Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Security/locations/westeurope/alerts/2518675235999999999_0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
Name               : 2518675235999999999_0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
ActionTaken        : Detected
AlertDisplayName   : PROTOCOL-ENFORCEMENT
AlertName          : PROTOCOL-ENFORCEMENT
AssociatedResource : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                     Network/applicationGateways/ContosoWAF
CanBeInvestigated  : True
CompromisedEntity  : 10.1.0.4
ConfidenceReasons  : {}
ConfidenceScore    : 
Description        : Detail:Host header is a numeric IP address 13.69.131.117
DetectedTimeUtc    : 20/08/2018 15:00:00
Entities           : {}
ExtendedProperties : {[hit Count, 1], [source IPs, 217.91.251.86], [management URL, https://portal.azure.com#resource/s
                     ubscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Ne
                     twork/applicationGateways/ContosoWAF/overview], [resourceType, Networking]}
InstanceId         : 0cd957d9-8101-47f7-88cc-0c5d0ebdbfd0
RemediationSteps   : 
ReportedSeverity   : Low
ReportedTimeUtc    : 20/08/2018 16:00:03
State              : Active
SubscriptionId     : 487bb485-b5b0-471e-9c0d-10717612f869
SystemSource       : Azure
VendorName         : Microsoft WAF
WorkspaceArmId     : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provid
                     ers/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869
                     -eus
```

<span data-ttu-id="a4091-118">Obtém um alerta de segurança específico detectado em recursos dentro do grupo de recursos "myService1"</span><span class="sxs-lookup"><span data-stu-id="a4091-118">Gets a specific security alert that were detected on resources inside the "myService1" resource group</span></span>

## <span data-ttu-id="a4091-119">OS</span><span class="sxs-lookup"><span data-stu-id="a4091-119">PARAMETERS</span></span>

### <span data-ttu-id="a4091-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4091-120">-DefaultProfile</span></span>
<span data-ttu-id="a4091-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4091-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4091-122">-Local</span><span class="sxs-lookup"><span data-stu-id="a4091-122">-Location</span></span>
<span data-ttu-id="a4091-123">Ponto.</span><span class="sxs-lookup"><span data-stu-id="a4091-123">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4091-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4091-124">-Name</span></span>
<span data-ttu-id="a4091-125">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a4091-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4091-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4091-126">-ResourceGroupName</span></span>
<span data-ttu-id="a4091-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4091-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4091-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4091-128">-ResourceId</span></span>
<span data-ttu-id="a4091-129">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a4091-129">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4091-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4091-130">CommonParameters</span></span>
<span data-ttu-id="a4091-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4091-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4091-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4091-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4091-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4091-133">INPUTS</span></span>

### <span data-ttu-id="a4091-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4091-134">System.String</span></span>

## <span data-ttu-id="a4091-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4091-135">OUTPUTS</span></span>

### <span data-ttu-id="a4091-136">Microsoft. Azure. Commands. Security. Models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="a4091-136">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="a4091-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4091-137">NOTES</span></span>

## <span data-ttu-id="a4091-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4091-138">RELATED LINKS</span></span>
