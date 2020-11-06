---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426341"
---
# <span data-ttu-id="a4814-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a4814-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="a4814-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4814-102">SYNOPSIS</span></span>
<span data-ttu-id="a4814-103">Atualizar um balanceador de carga de porta frontal</span><span class="sxs-lookup"><span data-stu-id="a4814-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4814-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4814-104">SYNTAX</span></span>

### <span data-ttu-id="a4814-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a4814-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4814-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4814-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4814-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4814-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4814-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4814-108">DESCRIPTION</span></span>
<span data-ttu-id="a4814-109">O cmdlet **set-AzureRmFrontDoor** atualiza um balanceador de carga de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="a4814-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="a4814-110">Se os parâmetros de entrada não forem fornecidos, os parâmetros antigos da porta frontal existente serão usados.</span><span class="sxs-lookup"><span data-stu-id="a4814-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="a4814-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4814-111">EXAMPLES</span></span>

### <span data-ttu-id="a4814-112">Exemplo 1: Atualize uma porta frontal existente com o FrontDoorName e o ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a4814-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="a4814-113">atualize um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="a4814-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="a4814-114">Exemplo 2: Atualize uma porta frontal existente com objeto PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="a4814-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="a4814-115">atualize um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="a4814-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="a4814-116">Exemplo 3: atualizar uma porta frontal existente com ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4814-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="a4814-117">atualize um FrontDoor existente.</span><span class="sxs-lookup"><span data-stu-id="a4814-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="a4814-118">OS</span><span class="sxs-lookup"><span data-stu-id="a4814-118">PARAMETERS</span></span>

### <span data-ttu-id="a4814-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="a4814-119">-BackendPool</span></span>
<span data-ttu-id="a4814-120">Backendpools disponível para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="a4814-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="a4814-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4814-121">-DefaultProfile</span></span>
<span data-ttu-id="a4814-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4814-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4814-123">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="a4814-123">-EnabledState</span></span>
<span data-ttu-id="a4814-124">Status operacional do balanceador de carga da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="a4814-124">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="a4814-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a4814-125">-FrontendEndpoint</span></span>
<span data-ttu-id="a4814-126">Pontos de extremidade de front-end disponíveis para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="a4814-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="a4814-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="a4814-127">-HealthProbeSetting</span></span>
<span data-ttu-id="a4814-128">Configurações de investigação de integridade associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="a4814-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="a4814-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4814-129">-InputObject</span></span>
<span data-ttu-id="a4814-130">O objeto da porta frontal a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="a4814-130">The Front Door object to update.</span></span>

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

### <span data-ttu-id="a4814-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="a4814-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="a4814-132">Configurações de balanceamento de carga associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="a4814-132">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="a4814-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4814-133">-Name</span></span>
<span data-ttu-id="a4814-134">O nome da porta frontal a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="a4814-134">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="a4814-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4814-135">-ResourceGroupName</span></span>
<span data-ttu-id="a4814-136">O grupo de recursos ao qual a porta frontal pertence.</span><span class="sxs-lookup"><span data-stu-id="a4814-136">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="a4814-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4814-137">-ResourceId</span></span>
<span data-ttu-id="a4814-138">ID do recurso da porta frontal a ser atualizada</span><span class="sxs-lookup"><span data-stu-id="a4814-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4814-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="a4814-139">-RoutingRule</span></span>
<span data-ttu-id="a4814-140">Regras de roteamento associadas a este FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a4814-140">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="a4814-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="a4814-141">-Tag</span></span>
<span data-ttu-id="a4814-142">As marcas associadas ao FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="a4814-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="a4814-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a4814-143">-Confirm</span></span>
<span data-ttu-id="a4814-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4814-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4814-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4814-145">-WhatIf</span></span>
<span data-ttu-id="a4814-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4814-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4814-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4814-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4814-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4814-148">CommonParameters</span></span>
<span data-ttu-id="a4814-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4814-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4814-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4814-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4814-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4814-151">INPUTS</span></span>

### <span data-ttu-id="a4814-152">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a4814-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="a4814-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a4814-153">System.String</span></span>

## <span data-ttu-id="a4814-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4814-154">OUTPUTS</span></span>

### <span data-ttu-id="a4814-155">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a4814-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="a4814-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4814-156">NOTES</span></span>

## <span data-ttu-id="a4814-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4814-157">RELATED LINKS</span></span>

<span data-ttu-id="a4814-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="a4814-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
