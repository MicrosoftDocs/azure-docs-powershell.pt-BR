---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264008"
---
# <span data-ttu-id="53b35-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="53b35-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="53b35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53b35-102">SYNOPSIS</span></span>
<span data-ttu-id="53b35-103">Obter a solução de segurança da IoT</span><span class="sxs-lookup"><span data-stu-id="53b35-103">Get IoT security solution</span></span>

## <span data-ttu-id="53b35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53b35-104">SYNTAX</span></span>

### <span data-ttu-id="53b35-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="53b35-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b35-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="53b35-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b35-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="53b35-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53b35-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="53b35-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53b35-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53b35-109">DESCRIPTION</span></span>
<span data-ttu-id="53b35-110">O cmdlet Get-AzIotSecuritySolution retorna uma ou mais soluções de segurança IOT.</span><span class="sxs-lookup"><span data-stu-id="53b35-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="53b35-111">A solução de segurança da IoT coleta dados de segurança e eventos de dispositivos IOT e Hub IOT para ajudar a prevenir e a detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="53b35-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="53b35-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53b35-112">EXAMPLES</span></span>

### <span data-ttu-id="53b35-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53b35-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="53b35-114">Obter a solução "MySample" no grupo de recursos "MyResource Group"</span><span class="sxs-lookup"><span data-stu-id="53b35-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="53b35-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="53b35-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="53b35-116">Obter lista de todas as soluções de segurança no grupo de recursos "MyResource Group"</span><span class="sxs-lookup"><span data-stu-id="53b35-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="53b35-117">OS</span><span class="sxs-lookup"><span data-stu-id="53b35-117">PARAMETERS</span></span>

### <span data-ttu-id="53b35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b35-118">-DefaultProfile</span></span>
<span data-ttu-id="53b35-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53b35-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53b35-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="53b35-120">-Name</span></span>
<span data-ttu-id="53b35-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="53b35-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53b35-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53b35-122">-ResourceGroupName</span></span>
<span data-ttu-id="53b35-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53b35-123">Resource group name.</span></span>

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

### <span data-ttu-id="53b35-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53b35-124">-ResourceId</span></span>
<span data-ttu-id="53b35-125">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="53b35-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="53b35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b35-126">CommonParameters</span></span>
<span data-ttu-id="53b35-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b35-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53b35-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b35-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53b35-129">INPUTS</span></span>

### <span data-ttu-id="53b35-130">System. String</span><span class="sxs-lookup"><span data-stu-id="53b35-130">System.String</span></span>

## <span data-ttu-id="53b35-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53b35-131">OUTPUTS</span></span>

### <span data-ttu-id="53b35-132">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="53b35-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="53b35-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53b35-133">NOTES</span></span>

## <span data-ttu-id="53b35-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53b35-134">RELATED LINKS</span></span>
