---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110891"
---
# <span data-ttu-id="a2d6a-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a2d6a-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="a2d6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d6a-103">Criar ou atualizar a solução de segurança IoT</span><span class="sxs-lookup"><span data-stu-id="a2d6a-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="a2d6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2d6a-104">SYNTAX</span></span>

### <span data-ttu-id="a2d6a-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="a2d6a-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d6a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a2d6a-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d6a-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="a2d6a-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d6a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2d6a-108">DESCRIPTION</span></span>
<span data-ttu-id="a2d6a-109">O cmdlet Set-AzIotSecuritySolution cria ou atualiza uma solução de segurança IOT específica.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="a2d6a-110">A solução de segurança da IoT coleta dados de segurança e eventos de dispositivos IOT e Hub IOT para ajudar a prevenir e a detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="a2d6a-111">O nome da solução de segurança IOT deve ser idêntico ao nome do Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="a2d6a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2d6a-112">EXAMPLES</span></span>

### <span data-ttu-id="a2d6a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2d6a-113">Example 1</span></span>
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

<span data-ttu-id="a2d6a-114">Criar uma nova solução de segurança IOT "MySample" para o Hub IoT com ID de recurso "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (o nome da solução deve ser idêntico ao nome do Hub IoT)</span><span class="sxs-lookup"><span data-stu-id="a2d6a-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="a2d6a-115">OS</span><span class="sxs-lookup"><span data-stu-id="a2d6a-115">PARAMETERS</span></span>

### <span data-ttu-id="a2d6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d6a-116">-DefaultProfile</span></span>
<span data-ttu-id="a2d6a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d6a-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="a2d6a-118">-DisabledDataSource</span></span>
<span data-ttu-id="a2d6a-119">Fontes de dados desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-119">Disabled data sources.</span></span>

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

### <span data-ttu-id="a2d6a-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2d6a-120">-DisplayName</span></span>
<span data-ttu-id="a2d6a-121">Nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-121">Display name.</span></span>

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

### <span data-ttu-id="a2d6a-122">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="a2d6a-122">-Enabled</span></span>
<span data-ttu-id="a2d6a-123">Situação.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-123">Status .</span></span>

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

### <span data-ttu-id="a2d6a-124">-Exportar</span><span class="sxs-lookup"><span data-stu-id="a2d6a-124">-Export</span></span>
<span data-ttu-id="a2d6a-125">Exportar dados.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-125">Export data.</span></span>

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

### <span data-ttu-id="a2d6a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2d6a-126">-InputObject</span></span>
<span data-ttu-id="a2d6a-127">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-127">Input Object.</span></span>

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

### <span data-ttu-id="a2d6a-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="a2d6a-128">-IotHub</span></span>
<span data-ttu-id="a2d6a-129">Hubs IOT.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-129">Iot hubs.</span></span>

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

### <span data-ttu-id="a2d6a-130">-Local</span><span class="sxs-lookup"><span data-stu-id="a2d6a-130">-Location</span></span>
<span data-ttu-id="a2d6a-131">Ponto.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-131">Location.</span></span>

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

### <span data-ttu-id="a2d6a-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2d6a-132">-Name</span></span>
<span data-ttu-id="a2d6a-133">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-133">Resource name.</span></span>

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

### <span data-ttu-id="a2d6a-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2d6a-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="a2d6a-135">Configuração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="a2d6a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d6a-136">-ResourceGroupName</span></span>
<span data-ttu-id="a2d6a-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-137">Resource group name.</span></span>

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

### <span data-ttu-id="a2d6a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2d6a-138">-ResourceId</span></span>
<span data-ttu-id="a2d6a-139">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a2d6a-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="a2d6a-140">-Tag</span></span>
<span data-ttu-id="a2d6a-141">Marcas.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-141">Tags.</span></span>

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

### <span data-ttu-id="a2d6a-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="a2d6a-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="a2d6a-143">Status de log de IP sem máscara.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-143">Unmasked ip logging status.</span></span>

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

### <span data-ttu-id="a2d6a-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="a2d6a-144">-UserDefinedResource</span></span>
<span data-ttu-id="a2d6a-145">Recursos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-145">User defined resources.</span></span>

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

### <span data-ttu-id="a2d6a-146">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a2d6a-146">-Workspace</span></span>
<span data-ttu-id="a2d6a-147">ID do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-147">Workspace ID.</span></span>

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

### <span data-ttu-id="a2d6a-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a2d6a-148">-Confirm</span></span>
<span data-ttu-id="a2d6a-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d6a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d6a-150">-WhatIf</span></span>
<span data-ttu-id="a2d6a-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d6a-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d6a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d6a-153">CommonParameters</span></span>
<span data-ttu-id="a2d6a-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d6a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d6a-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2d6a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d6a-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2d6a-156">INPUTS</span></span>

### <span data-ttu-id="a2d6a-157">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a2d6a-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="a2d6a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d6a-158">System.String</span></span>

### <span data-ttu-id="a2d6a-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2d6a-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a2d6a-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="a2d6a-160">System.String[]</span></span>

### <span data-ttu-id="a2d6a-161">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="a2d6a-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="a2d6a-162">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="a2d6a-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="a2d6a-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2d6a-163">OUTPUTS</span></span>

### <span data-ttu-id="a2d6a-164">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a2d6a-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="a2d6a-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2d6a-165">NOTES</span></span>

## <span data-ttu-id="a2d6a-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2d6a-166">RELATED LINKS</span></span>
