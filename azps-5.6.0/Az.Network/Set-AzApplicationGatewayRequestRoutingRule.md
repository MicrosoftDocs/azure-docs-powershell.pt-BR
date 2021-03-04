---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 832fd96f34e18413bfd72e1a05826954f3ae58e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892388"
---
# <span data-ttu-id="c44be-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c44be-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c44be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c44be-102">SYNOPSIS</span></span>
<span data-ttu-id="c44be-103">Modifica uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44be-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="c44be-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c44be-104">SYNTAX</span></span>

### <span data-ttu-id="c44be-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c44be-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c44be-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c44be-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c44be-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c44be-107">DESCRIPTION</span></span>
<span data-ttu-id="c44be-108">O cmdlet **Set-AzApplicationGatewayRequestRoutingRule** modifica uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="c44be-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="c44be-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c44be-109">EXAMPLES</span></span>

### <span data-ttu-id="c44be-110">Exemplo 1: atualizar uma regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="c44be-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c44be-111">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c44be-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c44be-112">O segundo comando modifica a regra de roteamento de solicitação para o gateway de aplicativo usar configurações HTTP back-end especificadas na variável $Setting, um ouvinte HTTP especificado na variável $Listener e um pool de endereços back-end especificado na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="c44be-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="c44be-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c44be-113">PARAMETERS</span></span>

### <span data-ttu-id="c44be-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c44be-114">-ApplicationGateway</span></span>
<span data-ttu-id="c44be-115">Especifica o objeto gateway de aplicativo com o qual esse cmdlet associa uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="c44be-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="c44be-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c44be-116">-BackendAddressPool</span></span>
<span data-ttu-id="c44be-117">Especifica o pool de endereços back-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44be-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="c44be-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c44be-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c44be-119">Especifica a ID do pool de endereços back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44be-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="c44be-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c44be-120">-BackendHttpSettings</span></span>
<span data-ttu-id="c44be-121">Especifica as configurações HTTP de back-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44be-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="c44be-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c44be-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c44be-123">Especifica a ID de configurações HTTP back-end do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44be-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="c44be-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44be-124">-DefaultProfile</span></span>
<span data-ttu-id="c44be-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c44be-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c44be-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c44be-126">-HttpListener</span></span>
<span data-ttu-id="c44be-127">Especifica o ouvinte HTTP do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44be-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="c44be-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="c44be-128">-HttpListenerId</span></span>
<span data-ttu-id="c44be-129">Especifica a ID do ouvinte HTTP do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44be-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="c44be-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c44be-130">-Name</span></span>
<span data-ttu-id="c44be-131">Especifica o nome da regra de roteamento de solicitação que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="c44be-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c44be-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="c44be-132">-Priority</span></span>
<span data-ttu-id="c44be-133">A prioridade da regra</span><span class="sxs-lookup"><span data-stu-id="c44be-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44be-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c44be-134">-RedirectConfiguration</span></span>
<span data-ttu-id="c44be-135">RedirectConfiguration do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c44be-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c44be-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c44be-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="c44be-137">ID do gateway de aplicativo RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c44be-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c44be-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c44be-138">-RewriteRuleSet</span></span>
<span data-ttu-id="c44be-139">Reescrita do gateway de aplicativoRuleSet</span><span class="sxs-lookup"><span data-stu-id="c44be-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c44be-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c44be-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="c44be-141">ID do gateway de aplicativos RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c44be-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c44be-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c44be-142">-RuleType</span></span>
<span data-ttu-id="c44be-143">Especifica o tipo de regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="c44be-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="c44be-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c44be-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="c44be-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="c44be-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="c44be-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44be-146">CommonParameters</span></span>
<span data-ttu-id="c44be-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c44be-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44be-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c44be-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44be-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c44be-149">INPUTS</span></span>

### <span data-ttu-id="c44be-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c44be-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c44be-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c44be-151">OUTPUTS</span></span>

### <span data-ttu-id="c44be-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c44be-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c44be-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="c44be-153">NOTES</span></span>

## <span data-ttu-id="c44be-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c44be-154">RELATED LINKS</span></span>

[<span data-ttu-id="c44be-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c44be-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c44be-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c44be-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c44be-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c44be-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c44be-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c44be-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


