---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431949"
---
# <span data-ttu-id="13033-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="13033-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="13033-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13033-102">SYNOPSIS</span></span>
<span data-ttu-id="13033-103">Criar um PSRoutingRuleObject para a criação de porta frontal</span><span class="sxs-lookup"><span data-stu-id="13033-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13033-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13033-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13033-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13033-105">DESCRIPTION</span></span>
<span data-ttu-id="13033-106">Criar um PSRoutingRuleObject para a criação de porta frontal</span><span class="sxs-lookup"><span data-stu-id="13033-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="13033-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13033-107">EXAMPLES</span></span>

### <span data-ttu-id="13033-108">Exemplo 1: criar um PSRoutingRuleObject para a criação de porta frontal</span><span class="sxs-lookup"><span data-stu-id="13033-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

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

<span data-ttu-id="13033-109">Criar um PSRoutingRuleObject para a criação de porta frontal</span><span class="sxs-lookup"><span data-stu-id="13033-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="13033-110">OS</span><span class="sxs-lookup"><span data-stu-id="13033-110">PARAMETERS</span></span>

### <span data-ttu-id="13033-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="13033-111">-AcceptedProtocol</span></span>
<span data-ttu-id="13033-112">Esquemas de protocolo para corresponder a essa regra.</span><span class="sxs-lookup"><span data-stu-id="13033-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="13033-113">O valor padrão é {https, http}</span><span class="sxs-lookup"><span data-stu-id="13033-113">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="13033-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="13033-114">-BackendPoolName</span></span>
<span data-ttu-id="13033-115">ID do recurso do BackendPool para o qual esta regra roteia</span><span class="sxs-lookup"><span data-stu-id="13033-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="13033-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="13033-116">-CustomForwardingPath</span></span>
<span data-ttu-id="13033-117">O caminho personalizado usado para regravar caminhos de recursos correspondentes a essa regra.</span><span class="sxs-lookup"><span data-stu-id="13033-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="13033-118">Deixe em branco para usar o caminho de entrada.</span><span class="sxs-lookup"><span data-stu-id="13033-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="13033-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13033-119">-DefaultProfile</span></span>
<span data-ttu-id="13033-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13033-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13033-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="13033-121">-DynamicCompression</span></span>
<span data-ttu-id="13033-122">Se a compactação dinâmica será habilitada para conteúdo em cache quando o armazenamento em cache estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="13033-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="13033-123">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="13033-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="13033-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="13033-124">-EnableCaching</span></span>
<span data-ttu-id="13033-125">Se o armazenamento em cache para esta rota deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="13033-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="13033-126">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="13033-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13033-127">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="13033-127">-EnabledState</span></span>
<span data-ttu-id="13033-128">Se o uso dessa regra deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="13033-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="13033-129">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="13033-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="13033-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="13033-130">-ForwardingProtocol</span></span>
<span data-ttu-id="13033-131">O protocolo que essa regra usará ao encaminhar o tráfego para o valor padrão de back-ends é MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="13033-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13033-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="13033-132">-FrontDoorName</span></span>
<span data-ttu-id="13033-133">O nome da porta frontal à qual esta regra de roteamento pertence.</span><span class="sxs-lookup"><span data-stu-id="13033-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="13033-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="13033-134">-FrontendEndpointName</span></span>
<span data-ttu-id="13033-135">Os nomes dos pontos de extremidade de front-end associados a essa regra</span><span class="sxs-lookup"><span data-stu-id="13033-135">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="13033-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="13033-136">-Name</span></span>
<span data-ttu-id="13033-137">Nome do RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="13033-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="13033-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="13033-138">-PatternToMatch</span></span>
<span data-ttu-id="13033-139">Os padrões de rota da regra não devem ter \*, exceto, após o final/no final do caminho.</span><span class="sxs-lookup"><span data-stu-id="13033-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="13033-140">O valor padrão é/\*</span><span class="sxs-lookup"><span data-stu-id="13033-140">Default value is /\*</span></span>

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

### <span data-ttu-id="13033-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="13033-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="13033-142">O tratamento de termos de consulta de URL ao formar a chave de cache.</span><span class="sxs-lookup"><span data-stu-id="13033-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="13033-143">O valor padrão é StripAll</span><span class="sxs-lookup"><span data-stu-id="13033-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13033-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13033-144">-ResourceGroupName</span></span>
<span data-ttu-id="13033-145">O nome do grupo de recursos no qual o RoutingRule será criado.</span><span class="sxs-lookup"><span data-stu-id="13033-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="13033-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13033-146">CommonParameters</span></span>
<span data-ttu-id="13033-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13033-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13033-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13033-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13033-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13033-149">INPUTS</span></span>

### <span data-ttu-id="13033-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="13033-150">None</span></span>

## <span data-ttu-id="13033-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13033-151">OUTPUTS</span></span>

### <span data-ttu-id="13033-152">Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="13033-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="13033-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13033-153">NOTES</span></span>

## <span data-ttu-id="13033-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13033-154">RELATED LINKS</span></span>

<span data-ttu-id="13033-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="13033-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
