---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f815994a6f60490bd930a17748cd00167c2b52ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257304"
---
# <span data-ttu-id="f7088-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7088-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f7088-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7088-102">SYNOPSIS</span></span>
<span data-ttu-id="f7088-103">Modifica uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7088-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="f7088-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7088-104">SYNTAX</span></span>

### <span data-ttu-id="f7088-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7088-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7088-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f7088-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7088-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7088-107">DESCRIPTION</span></span>
<span data-ttu-id="f7088-108">O cmdlet **set-AzApplicationGatewayRequestRoutingRule** modifica uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="f7088-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="f7088-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7088-109">EXAMPLES</span></span>

### <span data-ttu-id="f7088-110">Exemplo 1: atualizar uma regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="f7088-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="f7088-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f7088-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f7088-112">O segundo comando modifica a regra de roteamento de solicitação do Application Gateway para usar as configurações HTTP de back-end especificadas na variável $Setting, um ouvinte HTTP especificado na variável $Listener e um pool de endereços back-end especificado na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="f7088-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="f7088-113">OS</span><span class="sxs-lookup"><span data-stu-id="f7088-113">PARAMETERS</span></span>

### <span data-ttu-id="f7088-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7088-114">-ApplicationGateway</span></span>
<span data-ttu-id="f7088-115">Especifica o objeto do gateway do aplicativo com o qual esse cmdlet associa uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="f7088-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="f7088-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7088-116">-BackendAddressPool</span></span>
<span data-ttu-id="f7088-117">Especifica o pool de endereços back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7088-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="f7088-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f7088-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="f7088-119">Especifica a ID do pool de endereços de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7088-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="f7088-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f7088-120">-BackendHttpSettings</span></span>
<span data-ttu-id="f7088-121">Especifica as configurações HTTP de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7088-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="f7088-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f7088-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="f7088-123">Especifica a ID de configurações HTTP de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7088-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="f7088-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7088-124">-DefaultProfile</span></span>
<span data-ttu-id="f7088-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7088-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7088-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f7088-126">-HttpListener</span></span>
<span data-ttu-id="f7088-127">Especifica o ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f7088-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="f7088-128">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="f7088-128">-HttpListenerId</span></span>
<span data-ttu-id="f7088-129">Especifica a ID do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f7088-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="f7088-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7088-130">-Name</span></span>
<span data-ttu-id="f7088-131">Especifica o nome da regra de roteamento de solicitação que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f7088-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f7088-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="f7088-132">-Priority</span></span>
<span data-ttu-id="f7088-133">A prioridade da regra</span><span class="sxs-lookup"><span data-stu-id="f7088-133">The priority of the rule</span></span>

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

### <span data-ttu-id="f7088-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7088-134">-RedirectConfiguration</span></span>
<span data-ttu-id="f7088-135">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="f7088-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f7088-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f7088-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="f7088-137">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7088-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f7088-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7088-138">-RewriteRuleSet</span></span>
<span data-ttu-id="f7088-139">RewriteRuleSet do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="f7088-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f7088-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="f7088-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="f7088-141">ID do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7088-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f7088-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="f7088-142">-RuleType</span></span>
<span data-ttu-id="f7088-143">Especifica o tipo de regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="f7088-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="f7088-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f7088-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="f7088-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="f7088-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="f7088-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7088-146">CommonParameters</span></span>
<span data-ttu-id="f7088-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7088-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7088-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7088-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7088-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7088-149">INPUTS</span></span>

### <span data-ttu-id="f7088-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7088-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7088-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7088-151">OUTPUTS</span></span>

### <span data-ttu-id="f7088-152">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7088-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7088-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7088-153">NOTES</span></span>

## <span data-ttu-id="f7088-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7088-154">RELATED LINKS</span></span>

[<span data-ttu-id="f7088-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7088-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f7088-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7088-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f7088-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7088-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f7088-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7088-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


