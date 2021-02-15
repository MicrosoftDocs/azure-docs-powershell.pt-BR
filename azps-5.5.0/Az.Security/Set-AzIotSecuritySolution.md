---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118697"
---
# <span data-ttu-id="bc15c-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="bc15c-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="bc15c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc15c-102">SYNOPSIS</span></span>
<span data-ttu-id="bc15c-103">Criar ou atualizar a solução de segurança de IoT</span><span class="sxs-lookup"><span data-stu-id="bc15c-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="bc15c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc15c-104">SYNTAX</span></span>

### <span data-ttu-id="bc15c-105">ResourceGroupLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bc15c-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc15c-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc15c-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc15c-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="bc15c-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc15c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc15c-108">DESCRIPTION</span></span>
<span data-ttu-id="bc15c-109">O Set-AzIotSecuritySolution cmdlet cria ou atualiza uma solução de segurança iot específica.</span><span class="sxs-lookup"><span data-stu-id="bc15c-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="bc15c-110">A solução de segurança de IoT coleta dados e eventos de segurança de dispositivos iot e hub iot para ajudar a evitar e detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="bc15c-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="bc15c-111">O nome da solução de segurança iot deve ser idêntico ao nome do hub iot.</span><span class="sxs-lookup"><span data-stu-id="bc15c-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="bc15c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc15c-112">EXAMPLES</span></span>

### <span data-ttu-id="bc15c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc15c-113">Example 1</span></span>
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

<span data-ttu-id="bc15c-114">Criar nova solução de segurança iot "MySample" para hub IoT com id de recurso "/subscriptions/XXXXXXXX-XXXX-XXXXXX-XXXXXXXXXXXX/resourceGroups/XxxlResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (o nome da solução deve ser idêntico ao nome do hub de IoT)</span><span class="sxs-lookup"><span data-stu-id="bc15c-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="bc15c-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc15c-115">PARAMETERS</span></span>

### <span data-ttu-id="bc15c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc15c-116">-DefaultProfile</span></span>
<span data-ttu-id="bc15c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc15c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc15c-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="bc15c-118">-DisabledDataSource</span></span>
<span data-ttu-id="bc15c-119">Fontes de dados desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="bc15c-119">Disabled data sources.</span></span>

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

### <span data-ttu-id="bc15c-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc15c-120">-DisplayName</span></span>
<span data-ttu-id="bc15c-121">Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="bc15c-121">Display name.</span></span>

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

### <span data-ttu-id="bc15c-122">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="bc15c-122">-Enabled</span></span>
<span data-ttu-id="bc15c-123">Status.</span><span class="sxs-lookup"><span data-stu-id="bc15c-123">Status .</span></span>

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

### <span data-ttu-id="bc15c-124">-Exportar</span><span class="sxs-lookup"><span data-stu-id="bc15c-124">-Export</span></span>
<span data-ttu-id="bc15c-125">Exportar dados.</span><span class="sxs-lookup"><span data-stu-id="bc15c-125">Export data.</span></span>

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

### <span data-ttu-id="bc15c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc15c-126">-InputObject</span></span>
<span data-ttu-id="bc15c-127">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="bc15c-127">Input Object.</span></span>

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

### <span data-ttu-id="bc15c-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="bc15c-128">-IotHub</span></span>
<span data-ttu-id="bc15c-129">Hubs Iot.</span><span class="sxs-lookup"><span data-stu-id="bc15c-129">Iot hubs.</span></span>

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

### <span data-ttu-id="bc15c-130">-Local</span><span class="sxs-lookup"><span data-stu-id="bc15c-130">-Location</span></span>
<span data-ttu-id="bc15c-131">Localização.</span><span class="sxs-lookup"><span data-stu-id="bc15c-131">Location.</span></span>

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

### <span data-ttu-id="bc15c-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc15c-132">-Name</span></span>
<span data-ttu-id="bc15c-133">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc15c-133">Resource name.</span></span>

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

### <span data-ttu-id="bc15c-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc15c-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="bc15c-135">Configuração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="bc15c-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="bc15c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc15c-136">-ResourceGroupName</span></span>
<span data-ttu-id="bc15c-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc15c-137">Resource group name.</span></span>

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

### <span data-ttu-id="bc15c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc15c-138">-ResourceId</span></span>
<span data-ttu-id="bc15c-139">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="bc15c-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="bc15c-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc15c-140">-Tag</span></span>
<span data-ttu-id="bc15c-141">Tags.</span><span class="sxs-lookup"><span data-stu-id="bc15c-141">Tags.</span></span>

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

### <span data-ttu-id="bc15c-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="bc15c-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="bc15c-143">Status de registro em log ip não massked.</span><span class="sxs-lookup"><span data-stu-id="bc15c-143">Unmasked ip logging status.</span></span>

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

### <span data-ttu-id="bc15c-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="bc15c-144">-UserDefinedResource</span></span>
<span data-ttu-id="bc15c-145">Recursos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bc15c-145">User defined resources.</span></span>

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

### <span data-ttu-id="bc15c-146">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="bc15c-146">-Workspace</span></span>
<span data-ttu-id="bc15c-147">ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc15c-147">Workspace ID.</span></span>

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

### <span data-ttu-id="bc15c-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bc15c-148">-Confirm</span></span>
<span data-ttu-id="bc15c-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc15c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc15c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc15c-150">-WhatIf</span></span>
<span data-ttu-id="bc15c-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bc15c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc15c-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc15c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc15c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc15c-153">CommonParameters</span></span>
<span data-ttu-id="bc15c-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc15c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc15c-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc15c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc15c-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="bc15c-156">INPUTS</span></span>

### <span data-ttu-id="bc15c-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="bc15c-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="bc15c-158">System.String</span><span class="sxs-lookup"><span data-stu-id="bc15c-158">System.String</span></span>

### <span data-ttu-id="bc15c-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc15c-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc15c-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bc15c-160">System.String[]</span></span>

### <span data-ttu-id="bc15c-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="bc15c-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="bc15c-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="bc15c-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="bc15c-163">Saídas</span><span class="sxs-lookup"><span data-stu-id="bc15c-163">OUTPUTS</span></span>

### <span data-ttu-id="bc15c-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="bc15c-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="bc15c-165">Notas</span><span class="sxs-lookup"><span data-stu-id="bc15c-165">NOTES</span></span>

## <span data-ttu-id="bc15c-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc15c-166">RELATED LINKS</span></span>
