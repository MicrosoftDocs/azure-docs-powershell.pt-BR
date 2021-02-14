---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117160"
---
# <span data-ttu-id="c0363-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="c0363-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="c0363-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0363-102">SYNOPSIS</span></span>
<span data-ttu-id="c0363-103">Atualizar uma ou mais das seguintes propriedades na solução de segurança de IoT: marcas, configuração de recomendação, recursos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="c0363-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="c0363-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0363-104">SYNTAX</span></span>

### <span data-ttu-id="c0363-105">ResourceGroupLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c0363-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0363-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="c0363-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0363-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="c0363-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0363-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0363-108">DESCRIPTION</span></span>
<span data-ttu-id="c0363-109">O Update-AzIotSecuritySolution cmdlet de hoje em dia uma ou mais das seguintes propriedades em uma solução de segurança de IoT específica: marcas, configuração de recomendação, recursos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c0363-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="c0363-110">Somente as propriedades especificadas serão atualizadas dentro da solução de segurança iot.</span><span class="sxs-lookup"><span data-stu-id="c0363-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="c0363-111">A solução de segurança de IoT coleta dados e eventos de segurança de dispositivos iot e hub iot para ajudar a evitar e detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="c0363-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="c0363-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0363-112">EXAMPLES</span></span>

### <span data-ttu-id="c0363-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0363-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

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
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="c0363-114">Atualizar a solução de segurança iot "MySample" do grupo de recursos "MyResourceGroup" com configuração de recomendação e recursos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="c0363-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="c0363-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0363-115">PARAMETERS</span></span>

### <span data-ttu-id="c0363-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0363-116">-DefaultProfile</span></span>
<span data-ttu-id="c0363-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0363-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0363-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0363-118">-InputObject</span></span>
<span data-ttu-id="c0363-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0363-119">Input Object.</span></span>

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

### <span data-ttu-id="c0363-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0363-120">-Name</span></span>
<span data-ttu-id="c0363-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c0363-121">Resource name.</span></span>

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

### <span data-ttu-id="c0363-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0363-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="c0363-123">Configuração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="c0363-123">Recommendations configuration.</span></span>

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

### <span data-ttu-id="c0363-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0363-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0363-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0363-125">Resource group name.</span></span>

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

### <span data-ttu-id="c0363-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0363-126">-ResourceId</span></span>
<span data-ttu-id="c0363-127">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="c0363-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c0363-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0363-128">-Tag</span></span>
<span data-ttu-id="c0363-129">Tags.</span><span class="sxs-lookup"><span data-stu-id="c0363-129">Tags.</span></span>

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

### <span data-ttu-id="c0363-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="c0363-130">-UserDefinedResource</span></span>
<span data-ttu-id="c0363-131">Recursos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c0363-131">User defined resources.</span></span>

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

### <span data-ttu-id="c0363-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c0363-132">-Confirm</span></span>
<span data-ttu-id="c0363-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0363-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0363-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0363-134">-WhatIf</span></span>
<span data-ttu-id="c0363-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c0363-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0363-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0363-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0363-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0363-137">CommonParameters</span></span>
<span data-ttu-id="c0363-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0363-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0363-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0363-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0363-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="c0363-140">INPUTS</span></span>

### <span data-ttu-id="c0363-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c0363-141">System.String</span></span>

### <span data-ttu-id="c0363-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="c0363-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="c0363-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0363-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c0363-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="c0363-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="c0363-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c0363-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="c0363-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="c0363-146">OUTPUTS</span></span>

### <span data-ttu-id="c0363-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="c0363-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="c0363-148">Notas</span><span class="sxs-lookup"><span data-stu-id="c0363-148">NOTES</span></span>

## <span data-ttu-id="c0363-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0363-149">RELATED LINKS</span></span>
