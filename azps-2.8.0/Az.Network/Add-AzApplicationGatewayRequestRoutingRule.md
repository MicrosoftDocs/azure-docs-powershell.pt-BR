---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ffd65085cba383556f4c749c8b7e2b915bb0071c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771837"
---
# <span data-ttu-id="c23b5-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c23b5-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c23b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c23b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c23b5-103">Adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c23b5-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="c23b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c23b5-104">SYNTAX</span></span>

### <span data-ttu-id="c23b5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c23b5-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c23b5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c23b5-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c23b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c23b5-107">DESCRIPTION</span></span>
<span data-ttu-id="c23b5-108">O cmdlet **Add-AzApplicationGatewayRequestRoutingRule** adiciona uma regra de roteamento de solicitação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c23b5-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="c23b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c23b5-109">EXAMPLES</span></span>

### <span data-ttu-id="c23b5-110">Exemplo 1: adicionar uma regra de roteamento de solicitação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c23b5-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c23b5-111">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c23b5-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c23b5-112">O segundo comando adiciona a regra de roteamento de solicitação ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c23b5-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="c23b5-113">OS</span><span class="sxs-lookup"><span data-stu-id="c23b5-113">PARAMETERS</span></span>

### <span data-ttu-id="c23b5-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c23b5-114">-ApplicationGateway</span></span>
<span data-ttu-id="c23b5-115">Especifica um gateway de aplicativo para o qual esse cmdlet adiciona uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="c23b5-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c23b5-116">-BackendAddressPool</span></span>
<span data-ttu-id="c23b5-117">Especifica um objeto de pool de endereços back-end do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c23b5-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c23b5-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c23b5-119">Especifica uma ID do pool de endereços back-end do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="c23b5-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c23b5-120">-BackendHttpSettings</span></span>
<span data-ttu-id="c23b5-121">Especifica um objeto de configurações HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c23b5-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c23b5-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c23b5-123">Especifica uma ID de configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c23b5-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c23b5-124">-DefaultProfile</span></span>
<span data-ttu-id="c23b5-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c23b5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c23b5-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c23b5-126">-HttpListener</span></span>
<span data-ttu-id="c23b5-127">Especifica o objeto ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c23b5-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-128">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="c23b5-128">-HttpListenerId</span></span>
<span data-ttu-id="c23b5-129">Especifica a ID do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c23b5-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="c23b5-130">-Name</span></span>
<span data-ttu-id="c23b5-131">Especifica o nome da regra de roteamento de solicitação que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="c23b5-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="c23b5-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c23b5-132">-RedirectConfiguration</span></span>
<span data-ttu-id="c23b5-133">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c23b5-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c23b5-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="c23b5-135">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c23b5-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c23b5-136">-RewriteRuleSet</span></span>
<span data-ttu-id="c23b5-137">RewriteRuleSet do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c23b5-137">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c23b5-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="c23b5-139">ID do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c23b5-139">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c23b5-140">-RuleType</span></span>
<span data-ttu-id="c23b5-141">Especifica o tipo de regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="c23b5-141">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c23b5-142">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="c23b5-143">-UrlPathMapId</span></span>
<span data-ttu-id="c23b5-144">Especifica a ID do mapa de caminho da URL para a regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="c23b5-144">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23b5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23b5-145">CommonParameters</span></span>
<span data-ttu-id="c23b5-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23b5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23b5-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c23b5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23b5-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c23b5-148">INPUTS</span></span>

### <span data-ttu-id="c23b5-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c23b5-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c23b5-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c23b5-150">OUTPUTS</span></span>

### <span data-ttu-id="c23b5-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c23b5-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c23b5-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c23b5-152">NOTES</span></span>

## <span data-ttu-id="c23b5-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c23b5-153">RELATED LINKS</span></span>

[<span data-ttu-id="c23b5-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c23b5-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c23b5-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c23b5-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c23b5-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c23b5-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c23b5-157">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c23b5-157">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


