---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 965aaeaba9d77b28389c4493e4a891b9e01aa2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892935"
---
# <span data-ttu-id="0872a-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0872a-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="0872a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0872a-102">SYNOPSIS</span></span>
<span data-ttu-id="0872a-103">Criar ou atualizar a solução de segurança da IoT</span><span class="sxs-lookup"><span data-stu-id="0872a-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="0872a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0872a-104">SYNTAX</span></span>

### <span data-ttu-id="0872a-105">ResourceGroupLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0872a-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0872a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0872a-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0872a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0872a-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0872a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0872a-108">DESCRIPTION</span></span>
<span data-ttu-id="0872a-109">O Set-AzIotSecuritySolution cmdlet cria ou atualiza uma solução de segurança iot específica.</span><span class="sxs-lookup"><span data-stu-id="0872a-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="0872a-110">A solução de segurança da IoT coleta dados e eventos de segurança de dispositivos iot e hub iot para ajudar a evitar e detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="0872a-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="0872a-111">O nome da solução de segurança iot deve ser idêntico ao nome do hub de iot.</span><span class="sxs-lookup"><span data-stu-id="0872a-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="0872a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0872a-112">EXAMPLES</span></span>

### <span data-ttu-id="0872a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0872a-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
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

<span data-ttu-id="0872a-114">Criar nova solução de segurança iot "MySample" para hub IoT com id de recurso "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (o nome da solução deve ser idêntico ao nome do hub IoT)</span><span class="sxs-lookup"><span data-stu-id="0872a-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="0872a-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0872a-115">PARAMETERS</span></span>

### <span data-ttu-id="0872a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0872a-116">-DefaultProfile</span></span>
<span data-ttu-id="0872a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0872a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0872a-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="0872a-118">-DisabledDataSource</span></span>
<span data-ttu-id="0872a-119">Fontes de dados desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="0872a-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0872a-120">-DisplayName</span></span>
<span data-ttu-id="0872a-121">Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="0872a-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="0872a-122">-Enabled</span></span>
<span data-ttu-id="0872a-123">Status .</span><span class="sxs-lookup"><span data-stu-id="0872a-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-124">-Export</span><span class="sxs-lookup"><span data-stu-id="0872a-124">-Export</span></span>
<span data-ttu-id="0872a-125">Exportar dados.</span><span class="sxs-lookup"><span data-stu-id="0872a-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0872a-126">-InputObject</span></span>
<span data-ttu-id="0872a-127">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="0872a-127">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="0872a-128">-IotHub</span></span>
<span data-ttu-id="0872a-129">Hubs de Iot.</span><span class="sxs-lookup"><span data-stu-id="0872a-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-130">-Location</span><span class="sxs-lookup"><span data-stu-id="0872a-130">-Location</span></span>
<span data-ttu-id="0872a-131">Local.</span><span class="sxs-lookup"><span data-stu-id="0872a-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-132">-Name</span><span class="sxs-lookup"><span data-stu-id="0872a-132">-Name</span></span>
<span data-ttu-id="0872a-133">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0872a-133">Resource name.</span></span>

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

### <span data-ttu-id="0872a-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="0872a-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="0872a-135">Configuração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="0872a-135">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0872a-136">-ResourceGroupName</span></span>
<span data-ttu-id="0872a-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0872a-137">Resource group name.</span></span>

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

### <span data-ttu-id="0872a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0872a-138">-ResourceId</span></span>
<span data-ttu-id="0872a-139">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="0872a-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0872a-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="0872a-140">-Tag</span></span>
<span data-ttu-id="0872a-141">Marcas.</span><span class="sxs-lookup"><span data-stu-id="0872a-141">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="0872a-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="0872a-143">Status de registro em log ip não máscarado.</span><span class="sxs-lookup"><span data-stu-id="0872a-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="0872a-144">-UserDefinedResource</span></span>
<span data-ttu-id="0872a-145">Recursos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0872a-145">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-146">-Workspace</span><span class="sxs-lookup"><span data-stu-id="0872a-146">-Workspace</span></span>
<span data-ttu-id="0872a-147">ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0872a-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0872a-148">-Confirm</span></span>
<span data-ttu-id="0872a-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0872a-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0872a-150">-WhatIf</span></span>
<span data-ttu-id="0872a-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0872a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0872a-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0872a-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0872a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0872a-153">CommonParameters</span></span>
<span data-ttu-id="0872a-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0872a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0872a-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0872a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0872a-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0872a-156">INPUTS</span></span>

### <span data-ttu-id="0872a-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0872a-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="0872a-158">System.String</span><span class="sxs-lookup"><span data-stu-id="0872a-158">System.String</span></span>

### <span data-ttu-id="0872a-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0872a-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0872a-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0872a-160">System.String[]</span></span>

### <span data-ttu-id="0872a-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="0872a-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="0872a-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="0872a-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="0872a-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0872a-163">OUTPUTS</span></span>

### <span data-ttu-id="0872a-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0872a-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="0872a-165">NOTES</span><span class="sxs-lookup"><span data-stu-id="0872a-165">NOTES</span></span>

## <span data-ttu-id="0872a-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0872a-166">RELATED LINKS</span></span>
