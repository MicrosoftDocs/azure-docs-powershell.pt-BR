---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 344041291f0d7f52aeebb0c968e99268ac042188
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126949"
---
# <span data-ttu-id="e8125-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8125-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="e8125-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8125-102">SYNOPSIS</span></span>
<span data-ttu-id="e8125-103">Atualizar um balanceador de carga da porta da frente</span><span class="sxs-lookup"><span data-stu-id="e8125-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="e8125-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8125-104">SYNTAX</span></span>

### <span data-ttu-id="e8125-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8125-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8125-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8125-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8125-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8125-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8125-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8125-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8125-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8125-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8125-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8125-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8125-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8125-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8125-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8125-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8125-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8125-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8125-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8125-114">DESCRIPTION</span></span>
<span data-ttu-id="e8125-115">O **cmdlet Set-AzFrontDoor** atualiza um balanceador de carga porta da frente.</span><span class="sxs-lookup"><span data-stu-id="e8125-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="e8125-116">Se os parâmetros de entrada não são fornecidos, parâmetros antigos da Porta Da Frente existente serão usados.</span><span class="sxs-lookup"><span data-stu-id="e8125-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="e8125-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e8125-117">EXAMPLES</span></span>

### <span data-ttu-id="e8125-118">Exemplo 1: atualize uma Porta da Frente existente com o NomeDoorDoOr e o ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e8125-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="e8125-119">atualizar um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="e8125-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="e8125-120">Exemplo 2: atualizar uma Porta Da Frente existente com objeto PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e8125-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e8125-121">atualizar um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="e8125-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="e8125-122">Exemplo 3: atualizar uma Porta da Frente existente com ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8125-122">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e8125-123">atualizar um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="e8125-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="e8125-124">Exemplo 4: atualizar a propriedade BackendPoolSetting EnforceCertificateNameCheck de um parâmetro de opção da opção -DisableCertificateNameCheck com -DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="e8125-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="e8125-125">O Front Door a ser atualizado pode ser identificado usando FrontoorName e ResourceGroupName, objeto PSFrontDoor ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e8125-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="e8125-126">(Veja acima 3 exemplos, por exemplo) O exemplo a seguir usa o objeto PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e8125-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -DisableCertificateNameCheck

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {PSBackendPoolsSetting object with EnforceCertificateNameCheck is set to Disabled}
EnforceCertificateNameCheck : Disabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e8125-127">atualizar um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="e8125-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="e8125-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8125-128">PARAMETERS</span></span>

### <span data-ttu-id="e8125-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="e8125-129">-BackendPool</span></span>
<span data-ttu-id="e8125-130">Backendpools disponíveis para regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e8125-130">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="e8125-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="e8125-132">Configurações para todos os backendPools.</span><span class="sxs-lookup"><span data-stu-id="e8125-132">Settings for all backendPools.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet, ByObjectWithBackendPoolsSettingParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8125-133">-DefaultProfile</span></span>
<span data-ttu-id="e8125-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8125-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8125-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="e8125-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="e8125-136">Se você desabilitar a verificação de nome do certificado em solicitações HTTPS para todos os pools de back-end.</span><span class="sxs-lookup"><span data-stu-id="e8125-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="e8125-137">Não há efeito em solicitações que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e8125-137">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByResourceIdWithCertificateNameCheckParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e8125-138">-EnabledState</span></span>
<span data-ttu-id="e8125-139">Status operacional do balanceador de carga porta da frente.</span><span class="sxs-lookup"><span data-stu-id="e8125-139">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8125-140">-FrontendEndpoint</span></span>
<span data-ttu-id="e8125-141">Pontos de extremidade frontend disponíveis para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e8125-141">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="e8125-142">-HealthProbeSetting</span></span>
<span data-ttu-id="e8125-143">Configurações de desassociação de saúde associadas a esta instância porta da frente.</span><span class="sxs-lookup"><span data-stu-id="e8125-143">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8125-144">-InputObject</span></span>
<span data-ttu-id="e8125-145">O objeto Front Door a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e8125-145">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByObjectWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-146">-Load ComncingSetting</span><span class="sxs-lookup"><span data-stu-id="e8125-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="e8125-147">Configurações de balanceamento de carga associadas a esta instância porta da frente.</span><span class="sxs-lookup"><span data-stu-id="e8125-147">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8125-148">-Name</span></span>
<span data-ttu-id="e8125-149">O nome da Porta da Frente a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e8125-149">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8125-150">-ResourceGroupName</span></span>
<span data-ttu-id="e8125-151">O grupo de recursos ao qual a Porta da Frente pertence.</span><span class="sxs-lookup"><span data-stu-id="e8125-151">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8125-152">-ResourceId</span></span>
<span data-ttu-id="e8125-153">ID do Recurso da Porta da Frente para atualizar</span><span class="sxs-lookup"><span data-stu-id="e8125-153">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithCertificateNameCheckParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8125-154">-RoutingRule</span></span>
<span data-ttu-id="e8125-155">Regras de roteamento associadas a este FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8125-155">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8125-156">-Tag</span></span>
<span data-ttu-id="e8125-157">As marcas associadas ao FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e8125-157">The tags associate with the FrontDoor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8125-158">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e8125-158">-Confirm</span></span>
<span data-ttu-id="e8125-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8125-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8125-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8125-160">-WhatIf</span></span>
<span data-ttu-id="e8125-161">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e8125-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8125-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8125-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8125-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8125-163">CommonParameters</span></span>
<span data-ttu-id="e8125-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8125-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8125-165">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8125-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8125-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="e8125-166">INPUTS</span></span>

### <span data-ttu-id="e8125-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8125-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="e8125-168">System.String</span><span class="sxs-lookup"><span data-stu-id="e8125-168">System.String</span></span>
## <span data-ttu-id="e8125-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="e8125-169">OUTPUTS</span></span>

### <span data-ttu-id="e8125-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8125-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="e8125-171">Notas</span><span class="sxs-lookup"><span data-stu-id="e8125-171">NOTES</span></span>

## <span data-ttu-id="e8125-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8125-172">RELATED LINKS</span></span>

<span data-ttu-id="e8125-173">[Novo-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoad QuencingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="e8125-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
