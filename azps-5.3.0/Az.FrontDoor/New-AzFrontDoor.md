---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426931"
---
# <span data-ttu-id="41611-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="41611-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="41611-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41611-102">SYNOPSIS</span></span>
<span data-ttu-id="41611-103">Criar um novo balanceador de carga da porta frontal do Azure</span><span class="sxs-lookup"><span data-stu-id="41611-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="41611-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41611-104">SYNTAX</span></span>

### <span data-ttu-id="41611-105">ByFieldsWithBackendPoolsSettingParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="41611-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41611-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="41611-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41611-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41611-107">DESCRIPTION</span></span>
<span data-ttu-id="41611-108">O cmdlet **New-AzFrontDoor** cria um novo balanceador de carga de porta frontal do Azure no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="41611-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="41611-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41611-109">EXAMPLES</span></span>

### <span data-ttu-id="41611-110">Exemplo 1: criar uma porta frontal com base em determinados parâmetros.</span><span class="sxs-lookup"><span data-stu-id="41611-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="41611-111">Crie uma porta frontal com base em determinados parâmetros.</span><span class="sxs-lookup"><span data-stu-id="41611-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="41611-112">OS</span><span class="sxs-lookup"><span data-stu-id="41611-112">PARAMETERS</span></span>

### <span data-ttu-id="41611-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="41611-113">-BackendPool</span></span>
<span data-ttu-id="41611-114">Backendpools disponível para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="41611-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="41611-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="41611-116">Configurações para todos os backendPools</span><span class="sxs-lookup"><span data-stu-id="41611-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41611-117">-DefaultProfile</span></span>
<span data-ttu-id="41611-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41611-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41611-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="41611-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="41611-120">Se a verificação de nome do certificado deve ser desabilitada em solicitações HTTPS para todos os pools back-end.</span><span class="sxs-lookup"><span data-stu-id="41611-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="41611-121">Nenhum efeito em solicitações não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="41611-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-122">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="41611-122">-EnabledState</span></span>
<span data-ttu-id="41611-123">Enabledstate do balanceador de carga da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="41611-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="41611-124">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="41611-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="41611-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="41611-125">-FrontendEndpoint</span></span>
<span data-ttu-id="41611-126">Pontos de extremidade de front-end disponíveis para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="41611-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="41611-127">-HealthProbeSetting</span></span>
<span data-ttu-id="41611-128">Configurações de investigação de integridade associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="41611-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="41611-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="41611-130">Configurações de balanceamento de carga associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="41611-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="41611-131">-Name</span></span>
<span data-ttu-id="41611-132">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="41611-132">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41611-133">-ResourceGroupName</span></span>
<span data-ttu-id="41611-134">O nome do grupo de recursos no qual a porta frontal será criada.</span><span class="sxs-lookup"><span data-stu-id="41611-134">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="41611-135">-RoutingRule</span></span>
<span data-ttu-id="41611-136">Regras de roteamento associadas a este FrontDoor</span><span class="sxs-lookup"><span data-stu-id="41611-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41611-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="41611-137">-Tag</span></span>
<span data-ttu-id="41611-138">As marcas associadas ao FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="41611-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="41611-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41611-139">-Confirm</span></span>
<span data-ttu-id="41611-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41611-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41611-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41611-141">-WhatIf</span></span>
<span data-ttu-id="41611-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41611-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41611-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41611-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41611-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41611-144">CommonParameters</span></span>
<span data-ttu-id="41611-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41611-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41611-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41611-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41611-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41611-147">INPUTS</span></span>

### <span data-ttu-id="41611-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="41611-148">None</span></span>
## <span data-ttu-id="41611-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41611-149">OUTPUTS</span></span>

### <span data-ttu-id="41611-150">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="41611-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="41611-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41611-151">NOTES</span></span>

## <span data-ttu-id="41611-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41611-152">RELATED LINKS</span></span>

<span data-ttu-id="41611-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="41611-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>