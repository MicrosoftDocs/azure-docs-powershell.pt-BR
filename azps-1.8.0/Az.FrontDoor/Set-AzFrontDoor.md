---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770834"
---
# <span data-ttu-id="0cf0d-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0cf0d-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="0cf0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cf0d-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf0d-103">Atualizar um balanceador de carga de porta frontal</span><span class="sxs-lookup"><span data-stu-id="0cf0d-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="0cf0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cf0d-104">SYNTAX</span></span>

### <span data-ttu-id="0cf0d-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0cf0d-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cf0d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cf0d-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0cf0d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cf0d-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cf0d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cf0d-108">DESCRIPTION</span></span>
<span data-ttu-id="0cf0d-109">O cmdlet **set-AzFrontDoor** atualiza um balanceador de carga de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="0cf0d-110">Se os parâmetros de entrada não forem fornecidos, os parâmetros antigos da porta frontal existente serão usados.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="0cf0d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cf0d-111">EXAMPLES</span></span>

### <span data-ttu-id="0cf0d-112">Exemplo 1: Atualize uma porta frontal existente com o FrontDoorName e o ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="0cf0d-113">atualize um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="0cf0d-114">Exemplo 2: Atualize uma porta frontal existente com objeto PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="0cf0d-115">atualize um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="0cf0d-116">Exemplo 3: atualizar uma porta frontal existente com ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf0d-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="0cf0d-117">atualize um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="0cf0d-118">OS</span><span class="sxs-lookup"><span data-stu-id="0cf0d-118">PARAMETERS</span></span>

### <span data-ttu-id="0cf0d-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="0cf0d-119">-BackendPool</span></span>
<span data-ttu-id="0cf0d-120">Backendpools disponível para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="0cf0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf0d-121">-DefaultProfile</span></span>
<span data-ttu-id="0cf0d-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cf0d-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="0cf0d-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="0cf0d-124">Se a verificação de nome do certificado deve ser desabilitada em solicitações HTTPS para todos os pools back-end.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="0cf0d-125">Nenhum efeito em solicitações não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-125">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-126">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="0cf0d-126">-EnabledState</span></span>
<span data-ttu-id="0cf0d-127">Status operacional do balanceador de carga da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-127">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="0cf0d-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="0cf0d-128">-FrontendEndpoint</span></span>
<span data-ttu-id="0cf0d-129">Pontos de extremidade de front-end disponíveis para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-129">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="0cf0d-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="0cf0d-130">-HealthProbeSetting</span></span>
<span data-ttu-id="0cf0d-131">Configurações de investigação de integridade associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-131">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="0cf0d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cf0d-132">-InputObject</span></span>
<span data-ttu-id="0cf0d-133">O objeto da porta frontal a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-133">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="0cf0d-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="0cf0d-135">Configurações de balanceamento de carga associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-135">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="0cf0d-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="0cf0d-136">-Name</span></span>
<span data-ttu-id="0cf0d-137">O nome da porta frontal a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-137">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf0d-138">-ResourceGroupName</span></span>
<span data-ttu-id="0cf0d-139">O grupo de recursos ao qual a porta frontal pertence.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-139">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf0d-140">-ResourceId</span></span>
<span data-ttu-id="0cf0d-141">ID do recurso da porta frontal a ser atualizada</span><span class="sxs-lookup"><span data-stu-id="0cf0d-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf0d-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="0cf0d-142">-RoutingRule</span></span>
<span data-ttu-id="0cf0d-143">Regras de roteamento associadas a este FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0cf0d-143">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="0cf0d-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="0cf0d-144">-Tag</span></span>
<span data-ttu-id="0cf0d-145">As marcas associadas ao FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="0cf0d-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0cf0d-146">-Confirm</span></span>
<span data-ttu-id="0cf0d-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf0d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf0d-148">-WhatIf</span></span>
<span data-ttu-id="0cf0d-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cf0d-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf0d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf0d-151">CommonParameters</span></span>
<span data-ttu-id="0cf0d-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf0d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf0d-153">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cf0d-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf0d-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cf0d-154">INPUTS</span></span>

### <span data-ttu-id="0cf0d-155">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0cf0d-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="0cf0d-156">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf0d-156">System.String</span></span>

## <span data-ttu-id="0cf0d-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cf0d-157">OUTPUTS</span></span>

### <span data-ttu-id="0cf0d-158">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0cf0d-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="0cf0d-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cf0d-159">NOTES</span></span>

## <span data-ttu-id="0cf0d-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cf0d-160">RELATED LINKS</span></span>

<span data-ttu-id="0cf0d-161">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="0cf0d-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
