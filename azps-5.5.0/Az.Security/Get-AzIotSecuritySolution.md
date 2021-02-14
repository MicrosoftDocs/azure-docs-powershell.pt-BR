---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110807"
---
# <span data-ttu-id="8bf66-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="8bf66-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="8bf66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bf66-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf66-103">Obter solução de segurança de IoT</span><span class="sxs-lookup"><span data-stu-id="8bf66-103">Get IoT security solution</span></span>

## <span data-ttu-id="8bf66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bf66-104">SYNTAX</span></span>

### <span data-ttu-id="8bf66-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8bf66-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bf66-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="8bf66-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bf66-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="8bf66-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bf66-108">Resourceid</span><span class="sxs-lookup"><span data-stu-id="8bf66-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bf66-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bf66-109">DESCRIPTION</span></span>
<span data-ttu-id="8bf66-110">O Get-AzIotSecuritySolution cmdlet retorna uma ou mais soluções de segurança iot.</span><span class="sxs-lookup"><span data-stu-id="8bf66-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="8bf66-111">A solução de segurança de IoT coleta dados e eventos de segurança de dispositivos iot e hub iot para ajudar a evitar e detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="8bf66-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="8bf66-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8bf66-112">EXAMPLES</span></span>

### <span data-ttu-id="8bf66-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bf66-113">Example 1</span></span>
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

<span data-ttu-id="8bf66-114">Obter a solução "MySample" no grupo de recursos "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="8bf66-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="8bf66-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8bf66-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="8bf66-116">Obter uma lista de todas as soluções de segurança no grupo de recursos "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="8bf66-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="8bf66-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bf66-117">PARAMETERS</span></span>

### <span data-ttu-id="8bf66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf66-118">-DefaultProfile</span></span>
<span data-ttu-id="8bf66-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bf66-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bf66-120">-Name</span></span>
<span data-ttu-id="8bf66-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="8bf66-121">Resource name.</span></span>

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

### <span data-ttu-id="8bf66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bf66-122">-ResourceGroupName</span></span>
<span data-ttu-id="8bf66-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bf66-123">Resource group name.</span></span>

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

### <span data-ttu-id="8bf66-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bf66-124">-ResourceId</span></span>
<span data-ttu-id="8bf66-125">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="8bf66-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8bf66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf66-126">CommonParameters</span></span>
<span data-ttu-id="8bf66-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf66-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bf66-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf66-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="8bf66-129">INPUTS</span></span>

### <span data-ttu-id="8bf66-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8bf66-130">System.String</span></span>

## <span data-ttu-id="8bf66-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="8bf66-131">OUTPUTS</span></span>

### <span data-ttu-id="8bf66-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="8bf66-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="8bf66-133">Notas</span><span class="sxs-lookup"><span data-stu-id="8bf66-133">NOTES</span></span>

## <span data-ttu-id="8bf66-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bf66-134">RELATED LINKS</span></span>
