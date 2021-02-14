---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116792"
---
# <span data-ttu-id="c2796-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="c2796-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="c2796-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2796-102">SYNOPSIS</span></span>
<span data-ttu-id="c2796-103">Criar um PSRoutingRuleObject para criação de Porta Da Frente</span><span class="sxs-lookup"><span data-stu-id="c2796-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c2796-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2796-104">SYNTAX</span></span>

### <span data-ttu-id="c2796-105">ByFieldsWithForwardingParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c2796-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2796-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2796-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2796-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2796-107">DESCRIPTION</span></span>
<span data-ttu-id="c2796-108">Criar um PSRoutingRuleObject para criação de Porta Da Frente</span><span class="sxs-lookup"><span data-stu-id="c2796-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c2796-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2796-109">EXAMPLES</span></span>

### <span data-ttu-id="c2796-110">Exemplo 1: Criar uma criação de PSRoutingRuleObject para porta da frente com uma regra de encaminhamento</span><span class="sxs-lookup"><span data-stu-id="c2796-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="c2796-111">Exemplo 2: Criar um PSRoutingRuleObject para criação de porta da frente com uma regra de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="c2796-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="c2796-112">Criar um PSRoutingRuleObject para criação de Porta Da Frente</span><span class="sxs-lookup"><span data-stu-id="c2796-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="c2796-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2796-113">PARAMETERS</span></span>

### <span data-ttu-id="c2796-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="c2796-114">-AcceptedProtocol</span></span>
<span data-ttu-id="c2796-115">Esquemas de protocolo correspondentes a esta regra.</span><span class="sxs-lookup"><span data-stu-id="c2796-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="c2796-116">O valor padrão é {https, http}</span><span class="sxs-lookup"><span data-stu-id="c2796-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="c2796-117">-BackendPoolName</span></span>
<span data-ttu-id="c2796-118">ID do recurso do BackendPool para o qual esta regra é encaminhada</span><span class="sxs-lookup"><span data-stu-id="c2796-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="c2796-119">-CustomForwardingPath</span></span>
<span data-ttu-id="c2796-120">O caminho personalizado usado para reescrever caminhos de recursos de acordo com essa regra.</span><span class="sxs-lookup"><span data-stu-id="c2796-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="c2796-121">Deixe vazia para usar o caminho de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2796-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="c2796-122">-CustomFragment</span></span>
<span data-ttu-id="c2796-123">Fragmente para adicionar à URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="c2796-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="c2796-124">Fragmentar é a parte da URL que vem depois de #.</span><span class="sxs-lookup"><span data-stu-id="c2796-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="c2796-125">Não inclua o #.</span><span class="sxs-lookup"><span data-stu-id="c2796-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="c2796-126">-CustomHost</span></span>
<span data-ttu-id="c2796-127">Hospede para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="c2796-127">Host to redirect.</span></span> <span data-ttu-id="c2796-128">Deixe vazia para usar o host de entrada como host de destino.</span><span class="sxs-lookup"><span data-stu-id="c2796-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="c2796-129">-CustomPath</span></span>
<span data-ttu-id="c2796-130">O caminho completo para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="c2796-130">The full path to redirect.</span></span> <span data-ttu-id="c2796-131">O caminho não pode estar vazio e deve começar com /.</span><span class="sxs-lookup"><span data-stu-id="c2796-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="c2796-132">Deixe vazia para usar o caminho de entrada como caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="c2796-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="c2796-133">-CustomQueryString</span></span>
<span data-ttu-id="c2796-134">O conjunto de cadeias de caracteres de consulta a ser colocado na URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="c2796-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="c2796-135">Definir esse valor substituiria qualquer cadeia de caracteres de consulta existente; deixe vazia para preservar a cadeia de caracteres de consulta de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2796-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="c2796-136">A cadeia de caracteres de consulta deve estar em <key>=</span><span class="sxs-lookup"><span data-stu-id="c2796-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="c2796-137">Formato.</span><span class="sxs-lookup"><span data-stu-id="c2796-137">format.</span></span> <span data-ttu-id="c2796-138">O primeiro?</span><span class="sxs-lookup"><span data-stu-id="c2796-138">The first ?</span></span> <span data-ttu-id="c2796-139">e & serão adicionados automaticamente, portanto, não as inclua na frente, mas separe várias cadeias de caracteres de consulta com &.</span><span class="sxs-lookup"><span data-stu-id="c2796-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2796-140">-DefaultProfile</span></span>
<span data-ttu-id="c2796-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2796-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2796-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="c2796-142">-DynamicCompression</span></span>
<span data-ttu-id="c2796-143">Se você quer habilitar a compactação dinâmica para conteúdo armazenado em cache quando o cache estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="c2796-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="c2796-144">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="c2796-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="c2796-145">-EnableCaching</span></span>
<span data-ttu-id="c2796-146">Se você quer habilitar o cache para essa rota.</span><span class="sxs-lookup"><span data-stu-id="c2796-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="c2796-147">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="c2796-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c2796-148">-EnabledState</span></span>
<span data-ttu-id="c2796-149">Se você quer habilitar o uso dessa regra.</span><span class="sxs-lookup"><span data-stu-id="c2796-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="c2796-150">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="c2796-150">Default value is Enabled</span></span>

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

### <span data-ttu-id="c2796-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="c2796-151">-ForwardingProtocol</span></span>
<span data-ttu-id="c2796-152">O protocolo que essa regra usará ao encaminhar o tráfego para backends O valor padrão é MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="c2796-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c2796-153">-FrontDoorName</span></span>
<span data-ttu-id="c2796-154">O nome da Porta da Frente à qual esta regra de roteamento pertence.</span><span class="sxs-lookup"><span data-stu-id="c2796-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="c2796-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="c2796-155">-FrontendEndpointName</span></span>
<span data-ttu-id="c2796-156">Os nomes dos pontos de extremidade Frontend associados a esta regra</span><span class="sxs-lookup"><span data-stu-id="c2796-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2796-157">-Name</span></span>
<span data-ttu-id="c2796-158">Nome routingRule.</span><span class="sxs-lookup"><span data-stu-id="c2796-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="c2796-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="c2796-159">-PatternToMatch</span></span>
<span data-ttu-id="c2796-160">Os padrões de rota da regra não devem ter \* exceto possivelmente após a final/no final do caminho.</span><span class="sxs-lookup"><span data-stu-id="c2796-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="c2796-161">O valor padrão é /\*</span><span class="sxs-lookup"><span data-stu-id="c2796-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="c2796-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="c2796-163">O tratamento dos termos de consulta de URL ao formar a chave do cache.</span><span class="sxs-lookup"><span data-stu-id="c2796-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="c2796-164">O valor padrão é StripAll</span><span class="sxs-lookup"><span data-stu-id="c2796-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="c2796-165">-RedirectProtocol</span></span>
<span data-ttu-id="c2796-166">O protocolo do destino para onde o tráfego é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="c2796-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="c2796-167">O valor padrão é MatchRequest</span><span class="sxs-lookup"><span data-stu-id="c2796-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="c2796-168">-RedirectType</span></span>
<span data-ttu-id="c2796-169">O tipo de redirecionamento que a regra usará ao redirecionar o tráfego.</span><span class="sxs-lookup"><span data-stu-id="c2796-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="c2796-170">Valor Padrão é Movido</span><span class="sxs-lookup"><span data-stu-id="c2796-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2796-171">-ResourceGroupName</span></span>
<span data-ttu-id="c2796-172">O nome do grupo de recursos em que a RoteamentoRule será criada.</span><span class="sxs-lookup"><span data-stu-id="c2796-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="c2796-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="c2796-173">-RulesEngineName</span></span>
<span data-ttu-id="c2796-174">Uma referência a uma Configuração específica do Mecanismo de Regras a ser aplicada a essa rota.</span><span class="sxs-lookup"><span data-stu-id="c2796-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2796-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2796-175">CommonParameters</span></span>
<span data-ttu-id="c2796-176">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2796-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2796-177">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2796-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2796-178">Entradas</span><span class="sxs-lookup"><span data-stu-id="c2796-178">INPUTS</span></span>

### <span data-ttu-id="c2796-179">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c2796-179">None</span></span>

## <span data-ttu-id="c2796-180">Saídas</span><span class="sxs-lookup"><span data-stu-id="c2796-180">OUTPUTS</span></span>

### <span data-ttu-id="c2796-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c2796-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="c2796-182">Notas</span><span class="sxs-lookup"><span data-stu-id="c2796-182">NOTES</span></span>

## <span data-ttu-id="c2796-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2796-183">RELATED LINKS</span></span>

<span data-ttu-id="c2796-184">[Novo-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="c2796-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
