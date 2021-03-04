---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: f3a5b61561b0886af32aa13103f3234098c76357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888526"
---
# <span data-ttu-id="68fe3-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="68fe3-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="68fe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="68fe3-103">Criar um novo balanceador de carga da Porta Frontal do Azure</span><span class="sxs-lookup"><span data-stu-id="68fe3-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="68fe3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="68fe3-104">SYNTAX</span></span>

### <span data-ttu-id="68fe3-105">ByFieldsWithBackendPoolsSettingParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="68fe3-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fe3-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="68fe3-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68fe3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="68fe3-107">DESCRIPTION</span></span>
<span data-ttu-id="68fe3-108">O cmdlet **New-AzFrontDoor** cria um novo balanceador de carga da Porta Frontal do Azure no grupo de recursos especificado sob assinatura atual</span><span class="sxs-lookup"><span data-stu-id="68fe3-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="68fe3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68fe3-109">EXAMPLES</span></span>

### <span data-ttu-id="68fe3-110">Exemplo 1: Criar uma Porta Da Frente com base em determinados parâmetros.</span><span class="sxs-lookup"><span data-stu-id="68fe3-110">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="68fe3-111">Crie uma Porta Da Frente com base nos parâmetros determinados.</span><span class="sxs-lookup"><span data-stu-id="68fe3-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="68fe3-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="68fe3-112">PARAMETERS</span></span>

### <span data-ttu-id="68fe3-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="68fe3-113">-BackendPool</span></span>
<span data-ttu-id="68fe3-114">Backendpools disponíveis para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="68fe3-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="68fe3-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="68fe3-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="68fe3-116">Configurações para todos os backendPools</span><span class="sxs-lookup"><span data-stu-id="68fe3-116">Settings for all backendPools</span></span>

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

### <span data-ttu-id="68fe3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fe3-117">-DefaultProfile</span></span>
<span data-ttu-id="68fe3-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68fe3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68fe3-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="68fe3-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="68fe3-120">Se deve desabilitar a verificação do nome do certificado em solicitações HTTPS para todos os pools de back-end.</span><span class="sxs-lookup"><span data-stu-id="68fe3-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="68fe3-121">Não há efeito em solicitações que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="68fe3-121">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="68fe3-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="68fe3-122">-EnabledState</span></span>
<span data-ttu-id="68fe3-123">EnabledState do balanceador de carga da Porta Da Frente.</span><span class="sxs-lookup"><span data-stu-id="68fe3-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="68fe3-124">O valor padrão é Habilitado</span><span class="sxs-lookup"><span data-stu-id="68fe3-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="68fe3-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="68fe3-125">-FrontendEndpoint</span></span>
<span data-ttu-id="68fe3-126">Pontos de extremidade frontend disponíveis para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="68fe3-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="68fe3-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="68fe3-127">-HealthProbeSetting</span></span>
<span data-ttu-id="68fe3-128">Configurações da sonda de saúde associadas a essa instância da Porta Da Frente.</span><span class="sxs-lookup"><span data-stu-id="68fe3-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="68fe3-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="68fe3-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="68fe3-130">Configurações de balanceamento de carga associadas a essa instância da Porta Da Frente.</span><span class="sxs-lookup"><span data-stu-id="68fe3-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="68fe3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="68fe3-131">-Name</span></span>
<span data-ttu-id="68fe3-132">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="68fe3-132">Front Door name.</span></span>

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

### <span data-ttu-id="68fe3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68fe3-133">-ResourceGroupName</span></span>
<span data-ttu-id="68fe3-134">O nome do grupo de recursos em que a Porta da Frente será criada.</span><span class="sxs-lookup"><span data-stu-id="68fe3-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="68fe3-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="68fe3-135">-RoutingRule</span></span>
<span data-ttu-id="68fe3-136">Regras de roteamento associadas a esse FrontDoor</span><span class="sxs-lookup"><span data-stu-id="68fe3-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="68fe3-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="68fe3-137">-Tag</span></span>
<span data-ttu-id="68fe3-138">As marcas associadas ao FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="68fe3-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="68fe3-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68fe3-139">-Confirm</span></span>
<span data-ttu-id="68fe3-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68fe3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68fe3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68fe3-141">-WhatIf</span></span>
<span data-ttu-id="68fe3-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68fe3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68fe3-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68fe3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68fe3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fe3-144">CommonParameters</span></span>
<span data-ttu-id="68fe3-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68fe3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fe3-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68fe3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fe3-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68fe3-147">INPUTS</span></span>

### <span data-ttu-id="68fe3-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="68fe3-148">None</span></span>
## <span data-ttu-id="68fe3-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="68fe3-149">OUTPUTS</span></span>

### <span data-ttu-id="68fe3-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="68fe3-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="68fe3-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="68fe3-151">NOTES</span></span>

## <span data-ttu-id="68fe3-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68fe3-152">RELATED LINKS</span></span>

<span data-ttu-id="68fe3-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="68fe3-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>