---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770848"
---
# <span data-ttu-id="d7165-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="d7165-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="d7165-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7165-102">SYNOPSIS</span></span>
<span data-ttu-id="d7165-103">Criar um PSRoutingRuleObject para a criação de porta frontal</span><span class="sxs-lookup"><span data-stu-id="d7165-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="d7165-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7165-104">SYNTAX</span></span>

### <span data-ttu-id="d7165-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7165-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7165-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7165-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7165-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7165-107">DESCRIPTION</span></span>
<span data-ttu-id="d7165-108">Criar um PSRoutingRuleObject para a criação de porta frontal</span><span class="sxs-lookup"><span data-stu-id="d7165-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="d7165-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7165-109">EXAMPLES</span></span>

### <span data-ttu-id="d7165-110">Exemplo 1: criar um PSRoutingRuleObject para a criação de porta frontal</span><span class="sxs-lookup"><span data-stu-id="d7165-110">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="d7165-111">Criar um PSRoutingRuleObject para a criação de porta frontal</span><span class="sxs-lookup"><span data-stu-id="d7165-111">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="d7165-112">OS</span><span class="sxs-lookup"><span data-stu-id="d7165-112">PARAMETERS</span></span>

### <span data-ttu-id="d7165-113">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="d7165-113">-AcceptedProtocol</span></span>
<span data-ttu-id="d7165-114">Esquemas de protocolo para corresponder a essa regra.</span><span class="sxs-lookup"><span data-stu-id="d7165-114">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="d7165-115">O valor padrão é {https, http}</span><span class="sxs-lookup"><span data-stu-id="d7165-115">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="d7165-116">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="d7165-116">-BackendPoolName</span></span>
<span data-ttu-id="d7165-117">ID do recurso do BackendPool para o qual esta regra roteia</span><span class="sxs-lookup"><span data-stu-id="d7165-117">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="d7165-118">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="d7165-118">-CustomForwardingPath</span></span>
<span data-ttu-id="d7165-119">O caminho personalizado usado para regravar caminhos de recursos correspondentes a essa regra.</span><span class="sxs-lookup"><span data-stu-id="d7165-119">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="d7165-120">Deixe em branco para usar o caminho de entrada.</span><span class="sxs-lookup"><span data-stu-id="d7165-120">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="d7165-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="d7165-121">-CustomFragment</span></span>
<span data-ttu-id="d7165-122">Fragmento para adicionar à URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="d7165-122">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="d7165-123">Fragmento é a parte da URL que vem após #.</span><span class="sxs-lookup"><span data-stu-id="d7165-123">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="d7165-124">Não inclua o #.</span><span class="sxs-lookup"><span data-stu-id="d7165-124">Do not include the #.</span></span>

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

### <span data-ttu-id="d7165-125">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="d7165-125">-CustomHost</span></span>
<span data-ttu-id="d7165-126">Host para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="d7165-126">Host to redirect.</span></span> <span data-ttu-id="d7165-127">Deixe em branco para usar o host de entrada como o host de destino.</span><span class="sxs-lookup"><span data-stu-id="d7165-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="d7165-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="d7165-128">-CustomPath</span></span>
<span data-ttu-id="d7165-129">O caminho completo para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="d7165-129">The full path to redirect.</span></span> <span data-ttu-id="d7165-130">O caminho não pode estar vazio e deve começar com/.</span><span class="sxs-lookup"><span data-stu-id="d7165-130">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="d7165-131">Deixe em branco para usar o caminho de entrada como caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="d7165-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="d7165-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="d7165-132">-CustomQueryString</span></span>
<span data-ttu-id="d7165-133">O conjunto de cadeias de caracteres de consulta a serem colocadas na URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="d7165-133">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="d7165-134">Definir esse valor substituiria qualquer cadeia de caracteres de consulta existente; Deixe em branco para preservar a cadeia de caracteres de consulta recebida.</span><span class="sxs-lookup"><span data-stu-id="d7165-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="d7165-135">A cadeia de consulta deve estar em <key>=</span><span class="sxs-lookup"><span data-stu-id="d7165-135">Query string must be in <key>=</span></span><value> <span data-ttu-id="d7165-136">Format.</span><span class="sxs-lookup"><span data-stu-id="d7165-136">format.</span></span> <span data-ttu-id="d7165-137">O primeiro?</span><span class="sxs-lookup"><span data-stu-id="d7165-137">The first ?</span></span> <span data-ttu-id="d7165-138">e & serão adicionados automaticamente para não incluí-los na frente, mas separe várias cadeias de caracteres de consulta com &.</span><span class="sxs-lookup"><span data-stu-id="d7165-138">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="d7165-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7165-139">-DefaultProfile</span></span>
<span data-ttu-id="d7165-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7165-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7165-141">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="d7165-141">-DynamicCompression</span></span>
<span data-ttu-id="d7165-142">Se a compactação dinâmica será habilitada para conteúdo em cache quando o armazenamento em cache estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="d7165-142">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="d7165-143">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="d7165-143">Default value is Enabled</span></span>

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

### <span data-ttu-id="d7165-144">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="d7165-144">-EnableCaching</span></span>
<span data-ttu-id="d7165-145">Se o armazenamento em cache para esta rota deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="d7165-145">Whether to enable caching for this route.</span></span> <span data-ttu-id="d7165-146">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="d7165-146">Default value is false</span></span>

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

### <span data-ttu-id="d7165-147">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="d7165-147">-EnabledState</span></span>
<span data-ttu-id="d7165-148">Se o uso dessa regra deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="d7165-148">Whether to enable use of this rule.</span></span>
<span data-ttu-id="d7165-149">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="d7165-149">Default value is Enabled</span></span>

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

### <span data-ttu-id="d7165-150">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="d7165-150">-ForwardingProtocol</span></span>
<span data-ttu-id="d7165-151">O protocolo que essa regra usará ao encaminhar o tráfego para o valor padrão de back-ends é MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="d7165-151">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7165-152">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="d7165-152">-FrontDoorName</span></span>
<span data-ttu-id="d7165-153">O nome da porta frontal à qual esta regra de roteamento pertence.</span><span class="sxs-lookup"><span data-stu-id="d7165-153">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="d7165-154">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="d7165-154">-FrontendEndpointName</span></span>
<span data-ttu-id="d7165-155">Os nomes dos pontos de extremidade de front-end associados a essa regra</span><span class="sxs-lookup"><span data-stu-id="d7165-155">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="d7165-156">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7165-156">-Name</span></span>
<span data-ttu-id="d7165-157">Nome do RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="d7165-157">RoutingRule name.</span></span>

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

### <span data-ttu-id="d7165-158">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="d7165-158">-PatternToMatch</span></span>
<span data-ttu-id="d7165-159">Os padrões de rota da regra não devem ter \*, exceto, após o final/no final do caminho.</span><span class="sxs-lookup"><span data-stu-id="d7165-159">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="d7165-160">O valor padrão é/\*</span><span class="sxs-lookup"><span data-stu-id="d7165-160">Default value is /\*</span></span>

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

### <span data-ttu-id="d7165-161">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="d7165-161">-QueryParameterStripDirective</span></span>
<span data-ttu-id="d7165-162">O tratamento de termos de consulta de URL ao formar a chave de cache.</span><span class="sxs-lookup"><span data-stu-id="d7165-162">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="d7165-163">O valor padrão é StripAll</span><span class="sxs-lookup"><span data-stu-id="d7165-163">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7165-164">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="d7165-164">-RedirectProtocol</span></span>
<span data-ttu-id="d7165-165">O protocolo do destino para o qual o tráfego é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="d7165-165">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="d7165-166">O valor padrão é MatchRequest</span><span class="sxs-lookup"><span data-stu-id="d7165-166">Default value is MatchRequest</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7165-167">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="d7165-167">-RedirectType</span></span>
<span data-ttu-id="d7165-168">O tipo de redirecionamento que a regra usará ao redirecionar o tráfego.</span><span class="sxs-lookup"><span data-stu-id="d7165-168">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="d7165-169">O valor padrão é movido</span><span class="sxs-lookup"><span data-stu-id="d7165-169">Default Value is Moved</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7165-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7165-170">-ResourceGroupName</span></span>
<span data-ttu-id="d7165-171">O nome do grupo de recursos no qual o RoutingRule será criado.</span><span class="sxs-lookup"><span data-stu-id="d7165-171">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="d7165-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7165-172">CommonParameters</span></span>
<span data-ttu-id="d7165-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7165-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7165-174">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7165-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7165-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7165-175">INPUTS</span></span>

### <span data-ttu-id="d7165-176">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d7165-176">None</span></span>

## <span data-ttu-id="d7165-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7165-177">OUTPUTS</span></span>

### <span data-ttu-id="d7165-178">Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d7165-178">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="d7165-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7165-179">NOTES</span></span>

## <span data-ttu-id="d7165-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7165-180">RELATED LINKS</span></span>

<span data-ttu-id="d7165-181">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d7165-181">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
