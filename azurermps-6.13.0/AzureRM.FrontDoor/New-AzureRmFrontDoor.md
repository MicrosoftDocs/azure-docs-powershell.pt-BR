---
<span data-ttu-id="40c1f-101">arquivo de ajuda externo: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml nome do módulo: AzureRM. FrontDoor versão online: a URL correspondente deve ser a seguinte: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor Schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="40c1f-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="40c1f-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="40c1f-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="40c1f-103">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40c1f-103">SYNOPSIS</span></span>
<span data-ttu-id="40c1f-104">Criar um novo balanceador de carga da porta frontal do Azure</span><span class="sxs-lookup"><span data-stu-id="40c1f-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="40c1f-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40c1f-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="40c1f-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40c1f-106">DESCRIPTION</span></span>
<span data-ttu-id="40c1f-107">O cmdlet **New-AzureRmFrontDoor** cria um novo balanceador de carga de porta frontal do Azure no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="40c1f-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="40c1f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40c1f-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="40c1f-109">Exemplo 1: criar uma porta frontal com base em determinados parâmetros.</span><span class="sxs-lookup"><span data-stu-id="40c1f-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="40c1f-110">Crie uma porta frontal com base em determinados parâmetros.</span><span class="sxs-lookup"><span data-stu-id="40c1f-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="40c1f-111">OS</span><span class="sxs-lookup"><span data-stu-id="40c1f-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="40c1f-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="40c1f-112">-BackendPool</span></span>
<span data-ttu-id="40c1f-113">Backendpools disponível para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="40c1f-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="40c1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c1f-114">-DefaultProfile</span></span>
<span data-ttu-id="40c1f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40c1f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="40c1f-116">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="40c1f-116">-EnabledState</span></span>
<span data-ttu-id="40c1f-117">Enabledstate do balanceador de carga da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="40c1f-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="40c1f-118">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="40c1f-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="40c1f-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="40c1f-119">-FrontendEndpoint</span></span>
<span data-ttu-id="40c1f-120">Pontos de extremidade de front-end disponíveis para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="40c1f-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="40c1f-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="40c1f-121">-HealthProbeSetting</span></span>
<span data-ttu-id="40c1f-122">Configurações de investigação de integridade associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="40c1f-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="40c1f-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="40c1f-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="40c1f-124">Configurações de balanceamento de carga associadas a esta instância de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="40c1f-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="40c1f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="40c1f-125">-Name</span></span>
<span data-ttu-id="40c1f-126">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="40c1f-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="40c1f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c1f-127">-ResourceGroupName</span></span>
<span data-ttu-id="40c1f-128">O nome do grupo de recursos no qual a porta frontal será criada.</span><span class="sxs-lookup"><span data-stu-id="40c1f-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="40c1f-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="40c1f-129">-RoutingRule</span></span>
<span data-ttu-id="40c1f-130">Regras de roteamento associadas a este FrontDoor</span><span class="sxs-lookup"><span data-stu-id="40c1f-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="40c1f-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="40c1f-131">-Tag</span></span>
<span data-ttu-id="40c1f-132">As marcas associadas ao FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="40c1f-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="40c1f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40c1f-133">-Confirm</span></span>
<span data-ttu-id="40c1f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40c1f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="40c1f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c1f-135">-WhatIf</span></span>
<span data-ttu-id="40c1f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40c1f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c1f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40c1f-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="40c1f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c1f-138">CommonParameters</span></span>
<span data-ttu-id="40c1f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c1f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c1f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c1f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="40c1f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40c1f-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="40c1f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="40c1f-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="40c1f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40c1f-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="40c1f-144">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="40c1f-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="40c1f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40c1f-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="40c1f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40c1f-146">RELATED LINKS</span></span>

<span data-ttu-id="40c1f-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="40c1f-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
