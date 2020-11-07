---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 2e323170bac22950b9a6ca479e8470630741c2bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944825"
---
# <span data-ttu-id="97755-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97755-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="97755-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97755-102">SYNOPSIS</span></span>
<span data-ttu-id="97755-103">Modifica uma regra de roteamento de solicitação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97755-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="97755-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97755-104">SYNTAX</span></span>

### <span data-ttu-id="97755-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="97755-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97755-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="97755-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97755-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97755-107">DESCRIPTION</span></span>
<span data-ttu-id="97755-108">O cmdlet **set-AzApplicationGatewayRequestRoutingRule** modifica uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="97755-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="97755-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97755-109">EXAMPLES</span></span>

### <span data-ttu-id="97755-110">Exemplo 1: atualizar uma regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="97755-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="97755-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="97755-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="97755-112">O segundo comando modifica a regra de roteamento de solicitação do Application Gateway para usar as configurações HTTP de back-end especificadas na variável $Setting, um ouvinte HTTP especificado na variável $Listener e um pool de endereços back-end especificado na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="97755-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="97755-113">OS</span><span class="sxs-lookup"><span data-stu-id="97755-113">PARAMETERS</span></span>

### <span data-ttu-id="97755-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97755-114">-ApplicationGateway</span></span>
<span data-ttu-id="97755-115">Especifica o objeto do gateway do aplicativo com o qual esse cmdlet associa uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="97755-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="97755-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97755-116">-BackendAddressPool</span></span>
<span data-ttu-id="97755-117">Especifica o pool de endereços back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97755-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="97755-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="97755-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="97755-119">Especifica a ID do pool de endereços de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97755-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="97755-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="97755-120">-BackendHttpSettings</span></span>
<span data-ttu-id="97755-121">Especifica as configurações HTTP de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97755-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="97755-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="97755-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="97755-123">Especifica a ID de configurações HTTP de back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97755-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="97755-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97755-124">-DefaultProfile</span></span>
<span data-ttu-id="97755-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97755-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97755-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="97755-126">-HttpListener</span></span>
<span data-ttu-id="97755-127">Especifica o ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="97755-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="97755-128">-HttpListenerid</span><span class="sxs-lookup"><span data-stu-id="97755-128">-HttpListenerId</span></span>
<span data-ttu-id="97755-129">Especifica a ID do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="97755-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="97755-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="97755-130">-Name</span></span>
<span data-ttu-id="97755-131">Especifica o nome da regra de roteamento de solicitação que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="97755-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="97755-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="97755-132">-RedirectConfiguration</span></span>
<span data-ttu-id="97755-133">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="97755-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="97755-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="97755-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="97755-135">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="97755-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="97755-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="97755-136">-RewriteRuleSet</span></span>
<span data-ttu-id="97755-137">RewriteRuleSet do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="97755-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="97755-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="97755-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="97755-139">ID do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="97755-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="97755-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="97755-140">-RuleType</span></span>
<span data-ttu-id="97755-141">Especifica o tipo de regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="97755-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="97755-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="97755-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="97755-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="97755-143">-UrlPathMapId</span></span>
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

### <span data-ttu-id="97755-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97755-144">CommonParameters</span></span>
<span data-ttu-id="97755-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97755-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97755-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97755-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97755-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97755-147">INPUTS</span></span>

### <span data-ttu-id="97755-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97755-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97755-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97755-149">OUTPUTS</span></span>

### <span data-ttu-id="97755-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97755-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97755-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97755-151">NOTES</span></span>

## <span data-ttu-id="97755-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97755-152">RELATED LINKS</span></span>

[<span data-ttu-id="97755-153">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97755-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="97755-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97755-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="97755-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97755-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="97755-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97755-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


