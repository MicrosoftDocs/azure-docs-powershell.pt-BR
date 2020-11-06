---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596428"
---
# <span data-ttu-id="2e04e-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2e04e-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="2e04e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e04e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e04e-103">Criar um novo balanceador de carga da porta frontal do Azure</span><span class="sxs-lookup"><span data-stu-id="2e04e-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="2e04e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e04e-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e04e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e04e-105">DESCRIPTION</span></span>
<span data-ttu-id="2e04e-106">O cmdlet **New-AzFrontDoor** cria um novo balanceador de carga de porta frontal do Azure no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="2e04e-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="2e04e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e04e-107">EXAMPLES</span></span>

### <span data-ttu-id="2e04e-108">Exemplo 1: criar uma porta frontal com base em determinados parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2e04e-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="2e04e-109">Crie uma porta frontal com base em determinados parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2e04e-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="2e04e-110">OS</span><span class="sxs-lookup"><span data-stu-id="2e04e-110">PARAMETERS</span></span>

### <span data-ttu-id="2e04e-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="2e04e-111">-BackendPool</span></span>
<span data-ttu-id="2e04e-112">Backendpools disponível para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="2e04e-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="2e04e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e04e-113">-DefaultProfile</span></span>
<span data-ttu-id="2e04e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e04e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e04e-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="2e04e-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="2e04e-116">Se a verificação de nome do certificado deve ser desabilitada em solicitações HTTPS para todos os pools back-end.</span><span class="sxs-lookup"><span data-stu-id="2e04e-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="2e04e-117">Nenhum efeito em solicitações não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2e04e-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="2e04e-118">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="2e04e-118">-EnabledState</span></span>
<span data-ttu-id="2e04e-119">Enabledstate do balanceador de carga da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="2e04e-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="2e04e-120">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="2e04e-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="2e04e-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e04e-121">-FrontendEndpoint</span></span>
<span data-ttu-id="2e04e-122">Pontos de extremidade de front-end disponíveis para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="2e04e-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="2e04e-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="2e04e-123">-HealthProbeSetting</span></span>
<span data-ttu-id="2e04e-124">Configurações de investigação de integridade associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="2e04e-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="2e04e-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="2e04e-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="2e04e-126">Configurações de balanceamento de carga associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="2e04e-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="2e04e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e04e-127">-Name</span></span>
<span data-ttu-id="2e04e-128">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="2e04e-128">Front Door name.</span></span>

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

### <span data-ttu-id="2e04e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e04e-129">-ResourceGroupName</span></span>
<span data-ttu-id="2e04e-130">O nome do grupo de recursos no qual a porta frontal será criada.</span><span class="sxs-lookup"><span data-stu-id="2e04e-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="2e04e-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="2e04e-131">-RoutingRule</span></span>
<span data-ttu-id="2e04e-132">Regras de roteamento associadas a este FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2e04e-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="2e04e-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="2e04e-133">-Tag</span></span>
<span data-ttu-id="2e04e-134">As marcas associadas ao FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="2e04e-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="2e04e-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e04e-135">-Confirm</span></span>
<span data-ttu-id="2e04e-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e04e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e04e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e04e-137">-WhatIf</span></span>
<span data-ttu-id="2e04e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e04e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e04e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e04e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e04e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e04e-140">CommonParameters</span></span>
<span data-ttu-id="2e04e-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e04e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e04e-142">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e04e-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e04e-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e04e-143">INPUTS</span></span>

### <span data-ttu-id="2e04e-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2e04e-144">None</span></span>

## <span data-ttu-id="2e04e-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e04e-145">OUTPUTS</span></span>

### <span data-ttu-id="2e04e-146">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2e04e-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="2e04e-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e04e-147">NOTES</span></span>

## <span data-ttu-id="2e04e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e04e-148">RELATED LINKS</span></span>

<span data-ttu-id="2e04e-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="2e04e-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>