---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261656"
---
# <span data-ttu-id="f11dc-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f11dc-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="f11dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f11dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f11dc-103">Atualizar uma ou mais das seguintes propriedades na solução de segurança da IoT: marcas, configuração de recomendação, recursos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="f11dc-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="f11dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f11dc-104">SYNTAX</span></span>

### <span data-ttu-id="f11dc-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f11dc-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f11dc-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="f11dc-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f11dc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f11dc-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f11dc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f11dc-108">DESCRIPTION</span></span>
<span data-ttu-id="f11dc-109">O cmdlet Update-AzIotSecuritySolution updayes uma ou mais das seguintes propriedades em uma solução de segurança IoT específica: marcas, configuração de recomendação, recursos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f11dc-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="f11dc-110">Somente as propriedades especificadas serão atualizadas dentro da solução de segurança da IOT.</span><span class="sxs-lookup"><span data-stu-id="f11dc-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="f11dc-111">A solução de segurança da IoT coleta dados de segurança e eventos de dispositivos IOT e Hub IOT para ajudar a prevenir e a detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="f11dc-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="f11dc-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f11dc-112">EXAMPLES</span></span>

### <span data-ttu-id="f11dc-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f11dc-113">Example 1</span></span>
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

<span data-ttu-id="f11dc-114">Atualizar a solução de segurança IOT "MySample" do grupo de recursos "MyResource Group" com configuração de recomendação e recursos definidos pelo usuário</span><span class="sxs-lookup"><span data-stu-id="f11dc-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="f11dc-115">OS</span><span class="sxs-lookup"><span data-stu-id="f11dc-115">PARAMETERS</span></span>

### <span data-ttu-id="f11dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11dc-116">-DefaultProfile</span></span>
<span data-ttu-id="f11dc-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f11dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f11dc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f11dc-118">-InputObject</span></span>
<span data-ttu-id="f11dc-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="f11dc-119">Input Object.</span></span>

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

### <span data-ttu-id="f11dc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f11dc-120">-Name</span></span>
<span data-ttu-id="f11dc-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f11dc-121">Resource name.</span></span>

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

### <span data-ttu-id="f11dc-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="f11dc-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="f11dc-123">Configuração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="f11dc-123">Recommendations configuration.</span></span>

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

### <span data-ttu-id="f11dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f11dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="f11dc-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f11dc-125">Resource group name.</span></span>

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

### <span data-ttu-id="f11dc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f11dc-126">-ResourceId</span></span>
<span data-ttu-id="f11dc-127">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="f11dc-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f11dc-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="f11dc-128">-Tag</span></span>
<span data-ttu-id="f11dc-129">Marcas.</span><span class="sxs-lookup"><span data-stu-id="f11dc-129">Tags.</span></span>

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

### <span data-ttu-id="f11dc-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="f11dc-130">-UserDefinedResource</span></span>
<span data-ttu-id="f11dc-131">Recursos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f11dc-131">User defined resources.</span></span>

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

### <span data-ttu-id="f11dc-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f11dc-132">-Confirm</span></span>
<span data-ttu-id="f11dc-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f11dc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f11dc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f11dc-134">-WhatIf</span></span>
<span data-ttu-id="f11dc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f11dc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f11dc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f11dc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f11dc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11dc-137">CommonParameters</span></span>
<span data-ttu-id="f11dc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f11dc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11dc-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f11dc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11dc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f11dc-140">INPUTS</span></span>

### <span data-ttu-id="f11dc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f11dc-141">System.String</span></span>

### <span data-ttu-id="f11dc-142">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f11dc-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="f11dc-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f11dc-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f11dc-144">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="f11dc-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="f11dc-145">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f11dc-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="f11dc-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f11dc-146">OUTPUTS</span></span>

### <span data-ttu-id="f11dc-147">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f11dc-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="f11dc-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f11dc-148">NOTES</span></span>

## <span data-ttu-id="f11dc-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f11dc-149">RELATED LINKS</span></span>
