---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117412"
---
# <span data-ttu-id="4604d-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="4604d-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="4604d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4604d-102">SYNOPSIS</span></span>
<span data-ttu-id="4604d-103">Crie um objeto PSRulesEngineAction para criar uma regra de mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="4604d-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="4604d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4604d-104">SYNTAX</span></span>

### <span data-ttu-id="4604d-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="4604d-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4604d-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4604d-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4604d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4604d-107">DESCRIPTION</span></span>
<span data-ttu-id="4604d-108">Crie um objeto PSRulesEngineAction para criar uma regra de mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="4604d-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="4604d-109">Use o cmdlet "New-AzFrontDoorHeaderActionObject" para criar PSHeaderObjects para passar para os parâmetros "-RequestHeaderActions" e "-ResponseHeaderActions". "</span><span class="sxs-lookup"><span data-stu-id="4604d-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="4604d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4604d-110">EXAMPLES</span></span>

### <span data-ttu-id="4604d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4604d-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="4604d-112">Criar uma ação de mecanismo de regras e mostrar como exibir as propriedades da ação do mecanismo de regras criada.</span><span class="sxs-lookup"><span data-stu-id="4604d-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="4604d-113">OS</span><span class="sxs-lookup"><span data-stu-id="4604d-113">PARAMETERS</span></span>

### <span data-ttu-id="4604d-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="4604d-114">-BackendPoolName</span></span>
<span data-ttu-id="4604d-115">O nome do BackendPool ao qual esta regra roteia</span><span class="sxs-lookup"><span data-stu-id="4604d-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="4604d-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="4604d-116">-CustomForwardingPath</span></span>
<span data-ttu-id="4604d-117">O caminho personalizado usado para regravar caminhos de recursos correspondentes a essa regra.</span><span class="sxs-lookup"><span data-stu-id="4604d-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="4604d-118">Deixe em branco para usar o caminho de entrada.</span><span class="sxs-lookup"><span data-stu-id="4604d-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="4604d-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="4604d-119">-CustomFragment</span></span>
<span data-ttu-id="4604d-120">Fragmento para adicionar à URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="4604d-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="4604d-121">Fragmento é a parte da URL que vem após #.</span><span class="sxs-lookup"><span data-stu-id="4604d-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="4604d-122">Não inclua o #.</span><span class="sxs-lookup"><span data-stu-id="4604d-122">Do not include the #.</span></span>

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

### <span data-ttu-id="4604d-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="4604d-123">-CustomHost</span></span>
<span data-ttu-id="4604d-124">Host para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="4604d-124">Host to redirect.</span></span>
<span data-ttu-id="4604d-125">Deixe em branco para usar o host de entrada como o host de destino.</span><span class="sxs-lookup"><span data-stu-id="4604d-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="4604d-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="4604d-126">-CustomPath</span></span>
<span data-ttu-id="4604d-127">O caminho completo para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="4604d-127">The full path to redirect.</span></span>
<span data-ttu-id="4604d-128">O caminho não pode estar vazio e deve começar com/.</span><span class="sxs-lookup"><span data-stu-id="4604d-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="4604d-129">Deixe em branco para usar o caminho de entrada como caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="4604d-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="4604d-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="4604d-130">-CustomQueryString</span></span>
<span data-ttu-id="4604d-131">O conjunto de cadeias de caracteres de consulta a serem colocadas na URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="4604d-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="4604d-132">Definir esse valor substituiria qualquer cadeia de caracteres de consulta existente; Deixe em branco para preservar a cadeia de caracteres de consulta recebida.</span><span class="sxs-lookup"><span data-stu-id="4604d-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="4604d-133">A cadeia de caracteres de consulta deve estar no \<key\> = \<value\> formato.</span><span class="sxs-lookup"><span data-stu-id="4604d-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="4604d-134">O primeiro?</span><span class="sxs-lookup"><span data-stu-id="4604d-134">The first ?</span></span>
<span data-ttu-id="4604d-135">e & serão adicionados automaticamente para não incluí-los na frente, mas separe várias cadeias de caracteres de consulta com &.</span><span class="sxs-lookup"><span data-stu-id="4604d-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="4604d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4604d-136">-DefaultProfile</span></span>
<span data-ttu-id="4604d-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4604d-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4604d-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="4604d-138">-DynamicCompression</span></span>
<span data-ttu-id="4604d-139">Se a compactação dinâmica deve ser habilitada para conteúdo em cache.</span><span class="sxs-lookup"><span data-stu-id="4604d-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="4604d-140">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="4604d-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="4604d-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="4604d-141">-EnableCaching</span></span>
<span data-ttu-id="4604d-142">Se o armazenamento em cache para esta rota deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="4604d-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="4604d-143">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="4604d-143">Default value is false</span></span>

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

### <span data-ttu-id="4604d-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="4604d-144">-ForwardingProtocol</span></span>
<span data-ttu-id="4604d-145">O protocolo que essa regra usará ao encaminhar o tráfego para os back-ends.</span><span class="sxs-lookup"><span data-stu-id="4604d-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="4604d-146">O valor padrão é MatchRequest</span><span class="sxs-lookup"><span data-stu-id="4604d-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="4604d-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="4604d-147">-FrontDoorName</span></span>
<span data-ttu-id="4604d-148">O nome da porta frontal à qual esta regra de roteamento pertence.</span><span class="sxs-lookup"><span data-stu-id="4604d-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="4604d-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="4604d-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="4604d-150">O tratamento de termos de consulta de URL ao formar a chave de cache.</span><span class="sxs-lookup"><span data-stu-id="4604d-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="4604d-151">O valor padrão é StripAll</span><span class="sxs-lookup"><span data-stu-id="4604d-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="4604d-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="4604d-152">-RedirectProtocol</span></span>
<span data-ttu-id="4604d-153">O protocolo do destino para o qual o tráfego é redirecionado.</span><span class="sxs-lookup"><span data-stu-id="4604d-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="4604d-154">O valor padrão é MatchRequest</span><span class="sxs-lookup"><span data-stu-id="4604d-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="4604d-155">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="4604d-155">-RedirectType</span></span>
<span data-ttu-id="4604d-156">O tipo de redirecionamento que a regra usará ao redirecionar o tráfego.</span><span class="sxs-lookup"><span data-stu-id="4604d-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="4604d-157">O valor padrão é movido</span><span class="sxs-lookup"><span data-stu-id="4604d-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="4604d-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="4604d-158">-RequestHeaderAction</span></span>
<span data-ttu-id="4604d-159">Uma lista de ações de cabeçalho para aplicar-se da solicitação de AFD à origem.</span><span class="sxs-lookup"><span data-stu-id="4604d-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4604d-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4604d-160">-ResourceGroupName</span></span>
<span data-ttu-id="4604d-161">O nome do grupo de recursos no qual o RoutingRule será criado.</span><span class="sxs-lookup"><span data-stu-id="4604d-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="4604d-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="4604d-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="4604d-163">Uma lista de ações de cabeçalho para aplicar-se da resposta de AFD ao cliente.</span><span class="sxs-lookup"><span data-stu-id="4604d-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4604d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4604d-164">CommonParameters</span></span>
<span data-ttu-id="4604d-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4604d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4604d-166">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4604d-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4604d-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4604d-167">INPUTS</span></span>

### <span data-ttu-id="4604d-168">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4604d-168">None</span></span>

## <span data-ttu-id="4604d-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4604d-169">OUTPUTS</span></span>

### <span data-ttu-id="4604d-170">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="4604d-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="4604d-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4604d-171">NOTES</span></span>

## <span data-ttu-id="4604d-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4604d-172">RELATED LINKS</span></span>
